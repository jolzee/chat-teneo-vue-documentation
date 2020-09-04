---
description: Leopard has a tight integration with LiveChat.inc
---

# Live Chat

## Screenshots

![](../.gitbook/assets/livechat-screenshot.jpg)

## Setup and Configuration

### LiveChat Account Setup

You will need to have an account at LiveChat.inc

{% embed url="https://www.livechatinc.com/" %}

### LiveChat Key for Leopard

You will then need to configure Leopard with your LiveChat key that points at your account. This key can be found on `/settings/chat-link` . It's a numerical number. 

![Key found in page link url](../.gitbook/assets/livechat.png)

{% hint style="info" %}
Leopard's [build variables](../installation/build-variables.md) control access to the integration with LiveChat. 
{% endhint %}

```javascript
const config = {
  ...,
  /**
   * https://www.livechat.com/ integration - live chat handover
   */
  liveChatInc: {
    agentAssist: {
      /**
       * Server URL for creating agent assist canned responses -
       * https://github.com/jolzee/agent-assist-livechat-server-leopard
       */
      serverUrl: ""
    },
    key: "" // livechat.com license key
  },
  ...
};

module.exports = config;

```

### LiveChat API Key

You will also need to acquire the LiveChat Personal Access Token \(PAT\) so that an Integration in Teneo can be created. This integration will be responsible for checking to see if there is a live agent currently available before initiating a handover.

Login to LiveChat's web interface and head over to the LiveChat Deverloper Console - [https://developers.livechat.com/console/tools/personal-access-tokens](https://developers.livechat.com/console/tools/personal-access-tokens) . Create a new token. 

You can control you authorization scopes. Here's the ones I use:

```groovy
access_rules:ro, access_rules:rw, accounts--all:ro, accounts--all:rw, accounts--my:ro, accounts--my:rw, agents--my:rw, agents-bot--all:ro, agents-bot--all:rw, agents-bot--my:ro, agents-bot--my:rw, agents_read, agents_write, archives_read, archives_write, buttons_manage, canned_responses_read, canned_responses_write, tags_read, tags_write, chats--access:ro, chats--access:rw, chats--all:ro, chats--all:rw, chats--my:ro, chats--my:rw, chats.conversation--access:rw, chats.conversation--all:rw, chats.conversation--my:rw, customers:ro, customers:rw, greetings_read, greetings_write, in_app_msg_manage, multicast:rw, properties--all:ro, properties--my:ro, properties--my:rw, properties_manage, webhooks--all:ro, webhooks--all:rw, webhooks--my:ro, webhooks--my:rw, webhooks_manage, webhooks_write, sessions--all:rw, sessions--my:rw, visitors_read, agents--all:rw
```

## Studio

### Integration

When a user explicitly asks to speak to a human or some other handover rule has been triggered you will want to first check to see if there's a live agent available. This can be done using a custom integration in Teneo Studio. 

![Integration in Studio](../.gitbook/assets/livechat-integration.jpg)

```groovy
def addr = "https://api.livechatinc.com/agents"
def authString = "email@address.com:personal-access-token".getBytes().encodeBase64().toString()

def result = new groovy.json.JsonSlurper().parseText(addr.toURL().getText(connectTimeout: 2000, readTimeout: 3000,requestProperties: ['X-API-VERSION': '2','Authorization':'Basic ' + authString]));
def availableAgents = result.findAll { it.status == "accepting chats" }

agentAvailable = false
if (availableAgents.size() > 0) {
    agentAvailable = true
}
```

### Trigger Handover

The handover in Teneo is triggered by adding an output parameter to any output node.

```groovy
liveChat = ${dialogTranscript}
```

### Building the Dialog Transcript

Create a global variable called `dialogTranscript` 

#### Pre-processing Script

```groovy
if (_.userInputText) {
	dialogTranscript += "Visitor: " + _.userInputText + "\n";
}
```

#### Post-processing Script

```groovy
if (_.getOutputText()) {
	dialogTranscript += "Bot: " + _.getOutputText() + "\n";
}
```

### Example Flow

![Live Chat Handover in Studio](../.gitbook/assets/live-chat-handover.jpg)

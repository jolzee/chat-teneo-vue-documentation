---
description: >-
  Code is stored in a Github and linked to at the top of this documentation. You
  will need to have Node.js and Git installed to be able to clone the repository
  and to build and deploy Leopard.
---

# Installation

## Code

### Github

The latest code is stored in Github.

[**https://github.com/jolzee/chat-teneo-vue**](https://github.com/jolzee/chat-teneo-vue)\*\*\*\*

### Clone the Repository

```bash
git clone https://github.com/jolzee/chat-teneo-vue
```

 Next navigate into the cloned project

```bash
cd chat-teneo-vue
```

### Project setup

This command will inspect the dependencies in the project's **package.json** file and will download them locally.

```bash
npm install
```

### Compiles and hot-reloads for development

To run a local version of Leopard for testing and development run the following.

```bash
npm run serve
```

The browser should automatically open to [http://localhost:8080/](http://localhost:8080/) once compiling has finished. You can change code in the project and the Website should automatically reload. 

### Build

The following command will compile and minify all the code for production. The resulting HTML, CSS and JS code in the `/dist` folder can then be deployed to any web server.

```bash
npm run build
```

## Studio

Disable the following flow from the TDR's - `The user continues conversation after Timeout`  This flow is located in `Dialogue » Non-conversational » Timeout`

Capture the `command` request parameter. Leopard sends a `?command=login` whenever the chat window is opened. You will want to trigger the greeting message when this request parameter is present.

{% code-tabs %}
{% code-tabs-item title="Pre-processing Script" %}
```groovy
if (engineEnvironment.getParameter("command")) {
	command = engineEnvironment.getParameter("command")
} else {
	command = ""
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

In your greeting flow you will want to add a syntax trigger with the following condition

{% code-tabs %}
{% code-tabs-item title="Trigger Condition in Greeting Flow" %}
```groovy
{command == "login"}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## ExtensionHelper

### Explanation

ExtensionHelper is a Groovy Class that needs to be added to your Teneo solution. You can either add it to Solution Loaded or as a .groovy file into Resources

The purpose of ExtensionHelpder is to provide some helpful methods that can be called from output parameters in your flow nodes within Teneo. The methods will allow your solution to produce a JSON response that can be correctly interpreted by the Leopard UI. 

Some methods in ExtensionHelper do accept a channel as a method option. The available channels are:

* **webview**
  * Used by the web based Leopard UI. Make sure that your solution configurations in Leopard send a `channel=webview` either at login or with every request. All new solutions have this added automatically. Just know not to delete it. 
  * Make sure you are storing the channel as a global variable in your Teneo Solution. A `Pre-processing script` can extract it from the in coming request.
    * `if (engineEnvironment.getParameter("channel")) { channel = engineEnvironment.getParameter("channel") }`
* **facebook**
  * Creates the JSON that FB messenger expects for certain UI components
* **slack**
  * Creates the JSON that Slack expects for certain UI components

{% hint style="warning" %}
The Facebook and Slack have not been updated in a while and might fall behind some of the functionality for the webview.
{% endhint %}

### Download

You can always get the latest version of ExtensionHelper here:  

[**https://github.com/jolzee/chat-teneo-vue/blob/master/src/teneo-assets/ExtensionHelper.groovy**](https://raw.githubusercontent.com/jolzee/chat-teneo-vue/master/src/teneo-assets/ExtensionHelper.groovy)\*\*\*\*

### Installation

Add the ExtensionHelper as a Class within your Teneo Solution Loaded scripts or as a `.groovy` file in your solution's resources   `/script_lib` ****. 

### Usage

To use some of the methods in ExtensionHelper you will need to add an **output parameter** called `extensions` to the output where you want to show an extended view. The value would be one of the methods in ExtensionHelper. 

For example to show an image modal in the Leopard UI you would have a value of:

```groovy
${ExtensionHelper.displayImage(imageUrl,channel)}
```

All the different modals are listed in the documentation.

{% page-ref page="configuration/components/modals/" %}

{% page-ref page="configuration/components/" %}

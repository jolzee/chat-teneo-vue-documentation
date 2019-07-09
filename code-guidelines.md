---
description: Describes the project's file structure
---

# Code Guidelines

## Environment Variables

In the root folder of the project. Called either `.env` or `.env.local`

{% code-tabs %}
{% code-tabs-item title=".env" %}
```text
VUE_APP_HIDE_CONFIG_MENU=false
VUE_APP_LIVE_CHAT_INC_KEY=
VUE_APP_PUSHER_KEY=
VUE_APP_LOCATION_IQ_KEY=
VUE_APP_LONG_PRESS_LENGTH=1000
VUE_APP_FIREBASE_API_KEY=
VUE_APP_FIREBASE_AUTH_DOMAIN=
VUE_APP_FIREBASE_DATABASE_URL=
VUE_APP_FIREBASE_PROJECT_ID=
VUE_APP_FIREBASE_STORAGE_BUCKET=
VUE_APP_FIREBASE_MESSAGING_SENDER_ID=
VUE_APP_GET_STATIC_DEFAULT_CONFIG=true
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You can define global variables here. To reference one of these variables you should prefix the key with `process.env.`

For example:

```javascript
const liveChatIncLicense = process.env.VUE_APP_LIVE_CHAT_INC_KEY;
```

{% hint style="info" %}
Use `.env.local` for anything you don't want to be committed to git.
{% endhint %}

## Routes

Located in `/src/router.js`

Contains all the routing information for the [views](code-guidelines.md#views). More documentation on how Vue Router works can be found here:

{% embed url="https://router.vuejs.org/" %}

## Vuex Store

Located in `/src/store.js`

The Vuex Store is where most of the conditional logic happens. It provides global access to shared variables \(the model\) and methods throughout the Vue application. The store deals with all requests to Teneo for login, sending user input and end sessions. 

More information about Vuex Store and how to access and manipulate the model  can be found here:

{% embed url="https://vuex.vuejs.org/" %}

## Views

Located in `/src/views/*`

You can think of views as discreet pages that can be navigated to with the help of [Vue Router](code-guidelines.md#routes)

## Components

Located in `/src/components/*`

Custom components are located in this folder.  Components can reference other components and components can also be added to any Vue.js template.

## Constants

Located in `/src/constants/*`

Contains a few files that help configure some of Leopard's functionality.

* \`\`[`asr-corrections.js`](configuration/asr-and-tts.md#asr-corrections)\`\`
  * Allows for ASR issues to be fixed before getting to Teneo
* `color-names.js`
  * Used by the configuration UI of Leopard to validate custom theme color names. You shouldn't need to touch this file.
* `solution-config-default.js`
  * This is the default config for new solutions created in the Leopard UI
* \`\`[`translations.js`](configuration/asr-and-tts.md#supported-languages)\`\`
  * If you wanted to change some of the i18n labels for the various supported languages then this is the place to go.

## Public Assets

Located in `/public/*`

You can put any static assets in here if you want to link to them. These assets are not processed by the build script and will be placed directly in a `/public/` folder within the final build.


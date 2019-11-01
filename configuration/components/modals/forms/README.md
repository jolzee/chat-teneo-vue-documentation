---
description: >-
  Create and display custom forms in Leopard for any Teneo response. It's highly
  configurable with sensible defaults (look & feel, icons, validations, selects,
  combo boxes, images, headers & html)
---

# Forms

## Introduction

Although you can capture any input via dialog through the course of conversation it can be more familiar and user friendly to display a traditional form to a user at a key point of a conversation. Having this option in Leopard doesn't force the use or display of custom forms in any solution but rather provides flexibility in confirming or capturing information outside of lengthy conversations.

You have great control of the form structure, appearance, behavior, initial values and validation rules. 

{% hint style="success" %}
`ExtensionHelper` is **NOT** currently used to provide helper functions to generate the JSON structure needed by Leopard to render forms. **You are more than welcome to create and contribute some if you're up for it.**

It should however be straight forward to construct your necessary JSON based form config using the guidance and examples provided. 

Sensible defaults are set for the bulk of the form config options so the final JSON can be very slim if you are happy with the defaults.

It's worth while to use a online [JSON validator](https://jsonformatter.org/) before committing your final "`formConfig`" JSON in Teneo.
{% endhint %}

## Behavior

A custom form is currently tied directly to the respective output node that returned the "formConfig" as an output parameter.

This means that the form button against that response will be displayed in the chat dialog until the user completes the form and submits it back to Teneo. At that point the form button in the chat UI is removed from that particular response.

!!!! Current configuration is that the same form and button can be displayed in new responses if new dialog takes you there. If you want to prevent the offer of a custom form that has already been submitted then that logic needs to be engineered server side in Teneo around the "postback" data that is posted back to Teneo on a successful submission.

The form button can remain visible in the dialog until it's completed and submitted back. Therefore you should configure the "postback" information of the form to align with your flow strategy for capturing and responding to the data posted back Teneo.

At present a user isn't forced to complete a form in the current turn of the active conversation. Therefore you should plan accordingly in Teneo.

{% hint style="warning" %}
Custom Forms will operate both in "**Demo**" mode as well as "**Production**" embedded mode. 

Due to the current implementation of Leopard in production the form will only be overlaid over the chat UI area of the chat client. 

It will not be centered and wide as it is in development mode. Therefore if you plan to use custom forms in a production install of Leopard you should expect your form to render in a smaller and narrower area.
{% endhint %}

## Screenshot

![Render of custom form](../../../../.gitbook/assets/form.jpg)

## Output Parameter

```javascript
formConfig = {
   "title": "My Custom Form",
   "fields": [
      {
         "fieldType": "header",
         "label": "Please enter in your email address"
      },
      {
         "name": "username",
         "fieldType": "text",
         "label": "Email",
         "validations": "required"
      },
      {
         .. other fields
      }
   ]
}
```

{% hint style="info" %}
A more comprehensive example can be [found here](example-config.md)
{% endhint %}

## Component Configuration



| Element | Required/Optional | Default Value | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| title | required |  | String | The form's title |
| validationFailedMessage | optional | Please complete all required fields | String | A custom message to be displayed once a user submits the form and there are validation errors |
| openAutomatically | optional | false | Boolean | Controls if the form should automatically open for the Teneo response that contains the formConfig |
| openFormButtonText | optional | Form | String | Set the button text to open the form. Seen just below the answer text. |
| postback | optional |  | Object | Controls what is send back to Teneo on a successful submission of the form  |
| button | optional |  | Object | Controls the display of the button used in the form to complete the form submission |
| [fields](field-types.md) | required |  | Array of Field Type Objects | Allows you to add as many of the available [fields](field-types.md) in a specific order  |

## 

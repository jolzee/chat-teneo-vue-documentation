---
description: A working JSON config to explore
---

# Example Config

{% code-tabs %}
{% code-tabs-item title="formConfig =" %}
```javascript
{
   "title": "My Custom Form",
   "validationFailedMessage": "There are some required fields you still haven't completed.",
   "openAutomatically": true,
   "openFormButtonText": "Fill Form",
   "postback": {
      "formDataUrlParam": "formData",
      "userInput": "Thanks, I've completed the form",
      "confirmationAlert": "Thanks we have received your form"
   },
   "button": {
      "text": "Send",
      "icon": "send-circle",
      "color": "secondary",
      "clearButtonText": "Clear"
   },
   "fields": [
      {
         "fieldType": "alert",
         "text": "Donec elit libero, sodales nec, volutpat a, suscipit non, turpis. In auctor lobortis lacus.",
         "type": "success",
         "border": "left",
         "elevation": 2,
         "coloredBorder": true,
         "dense": false,
         "prominent": false,
         "outlined": false,
         "tile": false,
         "mdiIcon": "account-edit"
      },
      {
         "fieldType": "header",
         "label": "Please enter in your email address"
      },
      {
         "name": "username",
         "fieldType": "text",
         "label": "Email",
         "hint": "Just the username part please",
         "initialValue": "jolzee",
         "placeHolder": "username",
         "type": "solo",
         "clearable": true,
         "persistentHint": true,
         "dense": false,
         "counter": 12,
         "icons": {
            "prepend": "",
            "prependInner": "",
            "append": "",
            "appendOuter": "email-edit"
         },
         "prefix": "",
         "suffix": "@gmail.com",
         "validations": "required"
      },
      {
         "name": "bio",
         "fieldType": "textarea",
         "label": "Write a bio for yourself",
         "hint": "Keep it brief and to the point",
         "initialValue": "Bacon ipsum dolor amet rump ham hock sirloin doner fatback beef kielbasa picanha leberkas sausage buffalo capicola. Shoulder tail pancetta tenderloin. ",
         "autoGrow": true,
         "placeHolder": "Peter Joles is a Sales Engineer at Artificial Solutions...",
         "type": "solo",
         "clearable": true,
         "persistentHint": true,
         "rows": 5,
         "dense": false,
         "counter": 12,
         "prefix": "",
         "suffix": "",
         "icons": {
            "prepend": "",
            "prependInner": "",
            "append": "",
            "appendOuter": "file-document-edit"
         },
         "validations": "required"
      },
      {
         "name": "skills",
         "fieldType": "comboBox",
         "label": "What programming skill do you have?",
         "hint": "Don't worry if we don't have a skill listed",
         "chips": true,
         "multiple": true,
         "hideSelected": false,
         "deletableChips": true,
         "clearable": true,
         "dense": false,
         "items": [
            {
               "text": "Java",
               "value": "java"
            },
            {
               "text": "Node JS",
               "value": "nodejs"
            }
         ],
         "type": "solo",
         "openOnClear": false,
         "icons": {
            "prepend": "",
            "prependInner": "",
            "append": "",
            "appendOuter": "code-braces"
         },
         "validations": "required"
      },
      {
         "fieldType": "divider"
      },
      {
         "fieldType": "header",
         "label": "Rugby Time",
         "classes": [
            "headline",
            "font-weight-bold"
         ]
      },
      {
         "fieldType": "html",
         "label": "<p>To install Vuetify, type <kbd>npm install vuetify<\/kbd> into your console. Once complete, type <kbd>cd <code>&lt;project name&gt;<\/code><\/kbd> and run <kbd>npm install<\/kbd><\/p>",
         "classes": [
            "body-2",
            "font-weight-regular"
         ]
      },
      {
         "name": "favoriteRugbyTeam",
         "fieldType": "select",
         "label": "What's your favorite Rugby Team",
         "hint": "Go with the Green and Gold",
         "initialValue": [
            "South Africa"
         ],
         "chips": true,
         "deletableChips": false,
         "persistentHint": true,
         "clearable": true,
         "multiple": false,
         "dense": false,
         "hideSelected": true,
         "items": [
            "England",
            "South Africa",
            "New Zealand"
         ],
         "type": "solo",
         "icons": {
            "prepend": "",
            "prependInner": "",
            "append": "",
            "appendOuter": "football-australian"
         },
         "validations": "required"
      },
      {
         "fieldType": "switch",
         "name": "newsLetter",
         "label": "Do you want to receive our monthly newsletter?",
         "persistentHint": false,
         "dense": false,
         "hint": "We won't spam - ever!",
         "initialValue": true,
         "inset": false
      },
      {
         "fieldType": "radio",
         "name": "ageRange",
         "label": "What's you age range?",
         "dense": false,
         "hint": "Please don't lie 😁",
         "persistentHint": true,
         "mandatory": true,
         "multiple": false,
         "row": false,
         "items": [
            {
               "label": "18-25",
               "value": "18to25"
            },
            {
               "label": "26-45",
               "value": "26to45"
            }
         ],
         "icons": {
            "prepend": "gesture-tap-hold",
            "append": ""
         }
      },
      {
         "fieldType": "image",
         "alt": "RWC 2019",
         "src": "http://sportforbusiness.com/wp-content/uploads/JP-Rugby-worldcup-01.jpg",
         "maxWidth": "100%",
         "maxHeight": "600"
      },
      {
         "fieldType": "checkbox",
         "name": "agreedToTerms",
         "label": "Do you agree to our terms and conditions?",
         "hint": "You have to agree before submitting this form",
         "persistentHint": true,
         "dense": false,
         "initialValue": false,
         "validations": "required"
      }
   ]
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}


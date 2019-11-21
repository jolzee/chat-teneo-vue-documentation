---
description: A working JSON config to explore
---

# Example Config

{% code title="formConfig =" %}
```javascript
{
  "title": "My Custom Form",
  "validationFailedMessage": "There are some required fields you still haven't completed.",
  "openAutomatically": true,
  "openFormButtonText": "Fill Form",
  "maxWidth": "600",
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
      "alert": {
        "text": "Donec elit libero, sodales nec, volutpat a, suscipit non, turpis. In auctor lobortis lacus.",
        "type": "success",
        "border": "left",
        "elevation": 2,
        "coloredBorder": true,
        "dense": false,
        "prominent": false,
        "outlined": false,
        "tile": false,
        "icon": "account-edit"
      }
    },
    {
      "header": {
        "label": "Please enter in your email address"
      }
    },
    {
      "textInput": {
        "name": "username",
        "label": "Email",
        "hint": "Just the username part please",
        "initialValue": "jolzee",
        "placeHolder": "username",
        "style": {
          "solo": true,
          "outlined": false,
          "flat": false,
          "filled": false,
          "rounded": false,
          "shaped": false,
          "soloInverted": false
        },
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
      }
    },
    {
      "textarea": {
        "name": "bio",
        "label": "Write a bio for yourself",
        "description": "Please write a Bio about yourself.",
        "hint": "Keep it brief and to the point",
        "initialValue": "Bacon ipsum dolor amet rump ham hock sirloin doner fatback beef kielbasa picanha leberkas sausage buffalo capicola. Shoulder tail pancetta tenderloin. ",
        "autoGrow": true,
        "placeHolder": "Peter Joles is a Sales Engineer at Artificial Solutions...",
        "style": {
          "solo": false,
          "outlined": false,
          "flat": false,
          "filled": true,
          "rounded": false,
          "shaped": false,
          "soloInverted": false
        },
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
      }
    },
    {
      "comboBox": {
        "name": "skills",
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
        "style": {
          "solo": true,
          "outlined": false,
          "flat": false,
          "filled": false,
          "rounded": false,
          "shaped": false,
          "soloInverted": false
        },
        "openOnClear": false,
        "icons": {
          "prepend": "",
          "prependInner": "",
          "append": "",
          "appendOuter": "code-braces"
        },
        "validations": "required"
      }
    },
    {
      "divider": true
    },
    {
      "header": {
        "label": "Rugby Time",
        "classes": ["headline", "font-weight-bold"]
      }
    },
    {
      "html": {
        "label": "<p>To install Vuetify, type <kbd>npm install vuetify</kbd> into your console. Once complete, type <kbd>cd <code>&lt;project name&gt;</code></kbd> and run <kbd>npm install</kbd></p>",
        "classes": ["body-2", "font-weight-regular"]
      }
    },
    {
      "select": {
        "name": "favoriteRugbyTeam",
        "label": "What's your favorite Rugby Team",
        "hint": "Go with the Green and Gold",
        "initialValue": "South Africa",
        "chips": true,
        "deletableChips": false,
        "persistentHint": true,
        "clearable": true,
        "multiple": false,
        "dense": false,
        "hideSelected": true,
        "items": ["England", "South Africa", "New Zealand"],
        "style": {
          "solo": true,
          "outlined": false,
          "flat": false,
          "filled": false,
          "rounded": false,
          "shaped": false,
          "soloInverted": false
        },
        "icons": {
          "prepend": "",
          "prependInner": "",
          "append": "",
          "appendOuter": "football-australian"
        },
        "validations": "required"
      }
    },
    {
      "switch": {
        "name": "newsLetter",
        "label": "Do you want to receive our monthly newsletter?",
        "persistentHint": false,
        "dense": false,
        "hint": "We won't spam - ever!",
        "initialValue": true,
        "inset": false
      }
    },
    {
      "radio": {
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
      }
    },
    {
      "image": {
        "alt": "RWC 2019",
        "src": "http://sportforbusiness.com/wp-content/uploads/JP-Rugby-worldcup-01.jpg",
        "maxWidth": "100%",
        "maxHeight": "600"
      }
    },
    {
      "slider": {
        "name": "musicVolume",
        "label": "Volume",
        "hint": "Louder is better 😉",
        "persistentHint": true,
        "color": "success",
        "dense": false,
        "prependIcon": "volume-low",
        "appendIcon": "volume-high",
        "initialValue": "50",
        "range": false,
        "min": 0,
        "max": 100,
        "step": 2,
        "thumbColor": "primary",
        "thumbLabel": true,
        "thumbSize": 32,
        "ticks": true,
        "tickLabels": [],
        "trackColor": "error",
        "trackFillColor": "success",
        "validations": "required"
      }
    },
    {
      "slider": {
        "name": "musicRangeVolume",
        "label": "Range",
        "hint": "Louder is better 😉",
        "persistentHint": true,
        "color": "success",
        "dense": false,
        "prependIcon": "volume-low",
        "appendIcon": "volume-high",
        "initialValue": ["20", "80"],
        "range": true,
        "min": 0,
        "max": 100,
        "step": 2,
        "thumbColor": "primary",
        "thumbLabel": true,
        "thumbSize": 32,
        "ticks": true,
        "tickLabels": [],
        "trackColor": "error",
        "trackFillColor": "success",
        "validations": "required"
      }
    },
    {
      "checkbox": {
        "name": "agreedToTerms",
        "label": "Do you agree to our terms and conditions?",
        "hint": "You have to agree before submitting this form",
        "persistentHint": true,
        "dense": false,
        "initialValue": false,
        "mustBeChecked": true
      }
    }
  ]
}

```
{% endcode %}


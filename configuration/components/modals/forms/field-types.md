---
description: >-
  Headers, HTML, Alerts, Images, Input Fields, Text Areas, Selects, Combo Boxes,
  Check Boxes, Switches and Radio Buttons.
---

# Field Types

## Header

Simple header component `<header/>`. This component can be used to separate and announce different form elements or sections. You can pass in an array of css content classes that Vuetify makes available - more information on the available classes available here.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | header | String |  |
| label | required |  | String | Text you want to display as a header |
| classes | optional |  | Array of Strings | Any of the classes minus the preceding period sign - [https://vuetifyjs.com/en/styles/typography](https://vuetifyjs.com/en/styles/typography) |

### JSON

```javascript
{
    "fieldType": "header",
    "label": "This is a header",
    "classes": [
        "headline",
        "font-weight-bold"
    ]
}
```

## HTML

Simple component to add any ad hoc html to your form. You can pass in an array of css content classes that Vuetify makes available - more information on the available classes available here.

Make sure your HTML is escaped correctly so that it's still valid JSON that is being passed to the "formConfig" output parameter.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | html | String |  |
| label | required |  | String | HTML content |
| classes | optional |  | Array of Strings | Any of the classes minus the preceding period sign - [https://vuetifyjs.com/en/styles/typography](https://vuetifyjs.com/en/styles/typography) |

### JSON

```javascript
{
    "fieldType": "html",
    "label": "<p>To install Vuetify, type <kbd>npm install vuetify<\/kbd> into your console. Once complete, type <kbd>cd <code>&lt;project name&gt;<\/code><\/kbd> and run <kbd>npm install<\/kbd><\/p>",
    "classes": [
        "body-2",
        "font-weight-regular"
    ]
}
```

## Divider

Simple component that adds a `<hr/>` that can be used to separate fields or logically separate sections of your form.

### Screenshot

![](../../../../.gitbook/assets/divider.jpg)

### Config Options

| Element | Required/Optional | Value | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | divider | String |  |

### JSON

```javascript
{
    "fieldType": "divider"
}
```

## Alert

![](../../../../.gitbook/assets/alert.jpg)

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | alert | String |  |
| text | required |  | String | The message you want to display in the alert box |
| type | optional |  | String |  Specify a **success**, **info**, **warning** or **error** alert |
| border | optional |  | String |  Puts a border on the alert. Accepts **top** \| **right** \| **bottom** \| **left** |
| elevation | optional |  | Integer | Designates an elevation applied to the component between 0 and 24 |
| coloredBorder | optional |  | Boolean |  Applies the **color** defined by the type to the alert's border |
| dense | optional |  | Boolean | Decreases the alerts height |
| prominent | optional |  | Boolean | Displays a larger vertically centered icon to draw more attention |
| outlined | optional |  | Boolean | Makes the background transparent and applies a thin border |
| tile | optional |  | Boolean | Removes the component's border-radius |
| mdiIcon | optional |  | String | Any icon name from [https://materialdesignicons.com/](https://materialdesignicons.com/) |

### JSON

```javascript
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
}
```

## Image

Simple image component. You can control the image url, alt text, and max width and max height. The max width and max height can accept a pixel input and a percentage input.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | image | String |  |
| alt | optional |  | String | Alternate text for screen readers. Leave empty for decorative images |
| src | required |  | String | The image URL |
| maxWidth | optional |  | String | Sets the maximum width for the image. Can be pixels or percentage  |
| maxHeight | optional |  | String | Sets the maximum height for the image. Can be pixels or percentage  |

### JSON

```javascript
{
    "fieldType": "image",
    "alt": "RWC 2019",
    "src": "http://sportforbusiness.com/wp-content/uploads/JP-Rugby-worldcup-01.jpg",
    "maxWidth": "100%",
    "maxHeight": "600"
}
```

## Input Field

Configurable text input field. You can control the initial value, styling, icon selection and placement, masking, validations, hints, counters, placeholder text, prefix/append text and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

![](../../../../.gitbook/assets/text-field.jpg)

### Config Options

| Element | Required/Optional | Value | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | required | text | String |  |
| name | required |  | String |  |
| label | required |  | String |  |
| hint | optional |  | String |  |
| initialValue | optional |  | String |  |
| placeHolder | optional |  | String |  |
| type | optional |  | String |  |
| clearable | optional |  | Boolean |  |
| persistentHint | optional |  | Boolean |  |
| dense | optional |  | Boolean |  |
| counter | optional |  | Integer |  |
| icons | optional |  | Object |  |
| prefix | optional |  | String |  |
| suffix | optional |  | String |  |
| validations | optional |  | String |  |

### JSON

```javascript
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
    "icons":
    {
        "prepend": "",
        "prependInner": "",
        "append": "",
        "appendOuter": "email-edit"
    },
    "prefix": "",
    "suffix": "@gmail.com",
    "validations": "required"
}
```

## Text Area

Configurable text area field. You can control the initial value, styling, icon selection and placement, masking, validations, hints, placeholder text, counters, rows, auto grow, prefix/append text and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

![](../../../../.gitbook/assets/text-area.jpg)

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | textarea | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| hint | optional |  | String |  |
| initialValue | optional |  | String |  |
| autoGrow | optional |  | Boolean |  |
| placeHolder | optional |  | String |  |
| type | optional |  | String |  |
| clearable | optional |  | Boolean |  |
| persistentHint | optional |  | Boolean |  |
| rows | optional |  | Integer |  |
| dense | optional |  | Boolean |  |
| counter | optional |  | Integer |  |
| prefix | optional |  | String |  |
| suffix | optional |  | String |  |
| icons | optional |  | Object |  |
| validations | optional |  | String |  |

### JSON

```javascript
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
    "icons":
    {
        "prepend": "",
        "prependInner": "",
        "append": "",
        "appendOuter": "file-document-edit"
    },
    "validations": "required"
}
```

## Select

Configurable select field. You can control the initial value, options, styling, icon selection and placement, validations, hints, placeholder text and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | select | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| hint | optional |  | String |  |
| initialValue | optional |  | String |  |
| chips | optional |  | Boolean |  |
| deletableChips | optional |  | Boolean |  |
| persistentHint | optional |  | Boolean |  |
| clearable | optional |  | Boolean |  |
| multiple | optional |  | Boolean |  |
| dense | optional |  | Boolean |  |
| hideSelected | optional |  | Boolean |  |
| items | optional |  | Array of Strings |  |
| type | optional |  | String |  |
| icons | optional |  | Object |  |
| validations | optional |  | String |  |

### JSON

```javascript
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
    "icons":
    {
        "prepend": "",
        "prependInner": "",
        "append": "",
        "appendOuter": "football-australian"
    },
    "validations": "required"
}
```

## Combo Box

Configurable combo box field. This field can allow multiple items to be selected. You can control the initial selections, selectable options, styling, icon selection, validations, hints, placeholder text and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | comboBox | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| hint | optional |  | String |  |
| persistentHint | optional |  | Boolean |  |
| chips | optional |  | Boolean |  |
| multiple | optional |  | Boolean |  |
| hideSelected | optional |  | Boolean |  |
| deletableChips | optional |  | Boolean |  |
| clearable | optional |  | Boolean |  |
| dense | optional |  | Boolean |  |
| items | optional |  | Array of Objects |  |
| type | optional |  | String |  |
| openOnClear | optional |  | Boolean |  |
| icons | optional |  | Object |  |
| validations | optional |  | String |  |

### JSON

```javascript
{
    "name": "skills",
    "fieldType": "comboBox",
    "label": "What programming skill do you have?",
    "hint": "Don't worry if we don't have a skill listed",
    "persistentHint": true,
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
    "icons":
    {
        "prepend": "",
        "prependInner": "",
        "append": "",
        "appendOuter": "code-braces"
    },
    "validations": "required"
}
```

## Check Box

Configurable checkbox field. You can control the label, styling, icon selection, validations and hints

Many of the options are optional and sensible defaults are used.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | checkbox | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| hint | optional |  | String |  |
| persistentHint | optional |  | Boolean |  |
| dense | optional |  | Boolean |  |
| initialValue | optional |  | String |  |
| validations | optional |  | String |  |

### JSON

```javascript
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
```

## Switch

Configurable switch field that returns either true or false based on the operation on the switch. You can control the styling, icon selection, validations, hints, placeholder text and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | switch | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| persistentHint | optional |  | Boolean |  |
| dense | optional |  | Boolean |  |
| hint | optional |  | String |  |
| initialValue | optional |  | String |  |
| inset | optional |  | Boolean |  |
| validations | optional |  | String |  |

### JSON

```javascript
{
    "fieldType": "switch",
    "name": "newsLetter",
    "label": "Do you want to receive our monthly newsletter?",
    "persistantHint": false,
    "dense": false,
    "hint": "We won't spam - ever!",
    "initialValue": true,
    "inset": false
}
```

## Radio Buttons

Configurable radio button group field. You can control the options, styling, icon selection, validations, hints and more.

Many of the options are optional and sensible defaults are used.

### Screenshot

### Config Options

| Element | Required/Optional | Default | Type | Notes |
| :--- | :--- | :--- | :--- | :--- |
| fieldType | `required` | radio | String |  |
| name | `required` |  | String |  |
| label | `required` |  | String |  |
| dense | optional |  | Boolean |  |
| hint | optional |  | String |  |
| persistentHint | optional |  | Boolean |  |
| mandatory | optional |  | Boolean |  |
| multiple | optional |  | Boolean |  |
| row | optional |  | Integer |  |
| items | optional |  | Array of Objects |  |
| icons | optional |  | Object |  |
| validations | optional |  | String |  |

### JSON

```javascript
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
    "icons":
    {
        "prepend": "gesture-tap-hold",
        "append": ""
    }
}
```




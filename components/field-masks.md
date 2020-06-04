---
description: >-
  An input mask refers to a string expression, defined by a developer, that
  constrains user input. It can be said to be a template, or set format that
  entered data must conform to.
---

# Field Masks

## Mask Legend

| Character | Description |
| :--- | :--- |
| \# | Any digit |
| A | Any capital letter |
| a | Any small letter |
| N | Any capital alphanumeric character |
| n | Any small alphanumeric character |
| X | Any special symbol \(-!$%^&\*\(\)\_+\|~=\`{}\[\]:";'&lt;&gt;?,./\) or space |

## Examples

| Type | Mask |
| :--- | :--- |
| credit-card | \#\#\#\# - \#\#\#\# - \#\#\#\# - \#\#\#\# |
| date-with-time | \#\#/\#\#/\#\#\#\# \#\#:\#\# |
| phone | \(\#\#\#\) \#\#\# - \#\#\#\# |
| social | \#\#\#-\#\#-\#\#\#\# |
| time | \#\#:\#\# |
| time-with-seconds | \#\#:\#\#:\#\# |

## Output Parameters

Just add the following as an output parameter to a node which is asking for a user input where a mask is required.

{% code title="Will force the UI to accept a phone number" %}
```text
inputMask = (###) ### - ####
```
{% endcode %}

{% hint style="info" %}
You can also override the help text that is shown in the input field. 

## Output Parameter

```text
inputHelpText = Enter a phone number
```
{% endhint %}


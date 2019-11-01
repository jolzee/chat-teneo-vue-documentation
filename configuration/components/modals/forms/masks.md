---
description: >-
  Applying a mask to a field, forces the user to enter in their input in a
  specific way. This could be forcing a format for a postcode, zip, phone
  number, credit card, tracking number etc.
---

# Masks

More information on the acceptable mask formatting can be found here: [The Mask for Vue.js](https://vuejs-tips.github.io/vue-the-mask/)

## Tokens

```text
'#': {pattern: /\d/},
'X': {pattern: /[0-9a-zA-Z]/},
'S': {pattern: /[a-zA-Z]/},
'A': {pattern: /[a-zA-Z]/, transform: v => v.toLocaleUpperCase()},
'a': {pattern: /[a-zA-Z]/, transform: v => v.toLocaleLowerCase()},
'!': {escape: true}
```

## Examples

```text
##/##/####  < Date dd/mm/yyyy
##:##:##    < Time hh:mm:ss
##/##/#### ##:##:##    < Date Time dd/mm/yyyy hh:mm:ss
AA## #### #### #### #### #### ###    < IBAN Number
#####    < US ZIP such as 98075
+1 (###) ###-####    < US Phone Number
#### #### #### ####    < Credit Card Number
```


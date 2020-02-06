---
description: >-
  You can apply a set of custom validations against any of the form fields that
  accept input.
---

# Validation

You can apply a set of custom validations against any of the form fields that accept input. The validation rules are provided by VeeValidate and there are a large set of available validations that can be chained together. To chain validations together separate them with a pipe sign \|

## VeeValidate

[VeeValidate](https://logaretm.github.io/vee-validate/) is used for validations. You have a wealth of configurable validations that can be chained together. A full listing of validations can be [`found here`](https://logaretm.github.io/vee-validate/api/rules.html).

## Example Rules

| Rule | Description |
| :--- | :--- |
| `required|min:5` |  |
| `required|between:1,11` | Required and the field under validation must have a numeric value bounded by a minimum value and a maximum value. |
| `digits:3` | The field under validation must be numeric and have the specified number of digits. |
| `email` | The field under validation must be a valid email. |
| `oneOf:1,2,3`  |  The field under validation must have a value that is in the specified list. **Uses double equals** for checks. |
| `is:CONFIRM` |  The field under validation must be equal to the first argument passed, uses `===` for equality checks. Note that using the string format will cause any arguments to be parsed as strings, so use the object format when using this rule. |
| `max:4` | The field under validation length may not exceed the specified length. |
| `max_value:4` | The field under validation must be a numeric value and must not be greater than the specified value. |
| `min:4` | The field under validation length should not be less than the specified length. |
| `min_value:4` | The field under validation must be a numeric value and must not be less than the specified value. |
| `numeric` | The field under validation must only consist of numbers. |
| `regex: /^[0-9]+$/` | The field under validation must match the specified regular expression. |
| `required` | The field under validation must have a non-empty value. By default, all validators pass the validation if they have "empty values" unless they are required. Those empty values are: empty strings, undefined, null, empty arrays. |
| `required_if:country,US` | The field under validation must have a non-empty value **only if** the target field \(first argument\) is set to one of the specified values \(other arguments\). |

![](../../../../.gitbook/assets/image%20%283%29.png)


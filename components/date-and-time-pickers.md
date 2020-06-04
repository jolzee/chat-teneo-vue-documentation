---
description: >-
  These components capture user input. They are displayed inline as an icon
  within the chat message response. Clicking the icon opens up the full
  component in the middle of the page.
---

# Date & Time Pickers

## Date Picker

### Format

If you need to capture a date you can present the option to display a date picker to the user. The format of the date is currently `dd month yyyy`

![Date Format](../.gitbook/assets/date-picker-format.jpg)

### Screenshots

![](../.gitbook/assets/leopard-09%20%281%29.png)

![](../.gitbook/assets/leopard-06.png)

### Output Parameter

Showing the Date Picker is an exception to using the [ExtensionHelper](). It doesn't rely on the Extension Helper.

```groovy
datePicker = true
```

## Time Picker

### Format

The time picker uses a 24 hour format so a selection of 4am would be `04:00` and 4:35 pm would be `16:35`

### Screenshots

![](../.gitbook/assets/leopard-11.png)

![](../.gitbook/assets/leopard-10%20%281%29.png)

### Output Parameter

Showing the Time Picker is an exception to using the ExtensionHelper. It doesn't reply on the Extension Helper.

```groovy
timePicker = true
```




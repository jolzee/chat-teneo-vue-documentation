---
description: You can signal Leopard to display toasts.
---

# Toasts

![green = success / blue = info / error = red / warning = orange](../../.gitbook/assets/toast%20%281%29.png)

### Output Parameter

```groovy
toast = 
{
  "type"   :  "success", // [simple/success/info/warning/error]
  "title"  :  "Success", // optional
  "body"   :  "You successfully triggered a snotify alert",
  "config" :  {
    "timeout"         :  5000, // default: 2000 = 2 seconds
    "showProgressBar" :  true, // default: true
    "closeOnClick"    :  true, // default: true
    "pauseOnHover"    :  true, // default: true
    "icon"            :  "https://wi.presales.artificial-solutions.com/media/bulb.svg", // optional - type already defines icons
    "position"        :  "leftBottom" // [leftBottom, leftTop, leftCenterm rightTop, rightCenter, rightBottom, centerTop, centerCenter, centerBottom]
  }
}
```


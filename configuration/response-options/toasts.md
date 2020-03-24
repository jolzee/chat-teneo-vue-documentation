---
description: You can signal Leopard to display toasts.
---

# Toasts

![green = success / blue = info / red = error / orange = warning](../../.gitbook/assets/toast%20%281%29.png)

### Output Parameter

> Display a single Toast

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

Display multiple Toasts - displayed 2 seconds apart

```javascript
toast =

[ { "type"   : "success",
    "title"  : "Success",
    "body"   : "This is a success toast",
    "config" : { "timeout"         : 5000,
                 "showProgressBar" : true,
                 "closeOnClick"    : true,
                 "pauseOnHover"    : true,
                 "position"        : "leftBottom" } },
  { "type"   : "info",
    "title"  : "Information",
    "body"   : "This is an info toast",
    "config" : { "timeout"         : 5000,
                 "showProgressBar" : true,
                 "closeOnClick"    : true,
                 "pauseOnHover"    : true,
                 "position"        : "leftBottom" } },
  { "type"   : "warning",
    "title"  : "Warning",
    "body"   : "This is an warning toast",
    "config" : { "timeout"         : 5000,
                 "showProgressBar" : true,
                 "closeOnClick"    : true,
                 "pauseOnHover"    : true,
                 "position"        : "leftBottom" } },
  { "type"   : "error",
    "title"  : "Error",
    "body"   : "This is an warning toast",
    "config" : { "timeout"         : 5000,
                 "showProgressBar" : true,
                 "closeOnClick"    : true,
                 "pauseOnHover"    : true,
                 "position"        : "leftBottom" } } ]
```

![](../../.gitbook/assets/toasts-min.gif)


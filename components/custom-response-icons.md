---
description: >-
  Control the icons that are displayed in Leopard on a individual response
  basis.
---

# Response Icons

## Custom Icon Color

You can override the default response icon's color by specifying an "`iconColor`" **output parameter** with with a hex color code. 

```javascript
iconColor = #E0427E
```

## Quick Custom Icon

You can override the default response icon by specifying an "`icon`" **output parameter** with the name of the icon. Icon names can be found on [Material Design Icons](https://materialdesignicons.com/)

```javascript
icon = comment-alert-outline
```

## Leverage "emotion" in Studio for Custom Response Icons

This option leverages the "emotion" functionality in Teneo Studio. 

Just construct your emotions in a format where there a pipe sign \| and the icon name after the pipe sign. Add the emotion to any response node and you should see the custom icon being displayed in the response.

Any icon from here should work.

{% embed url="https://materialdesignicons.com/" %}

![](../.gitbook/assets/image%20%2824%29.png)

### Teneo Studio Setup

![Solution &#xBB; Globals &#xBB; Emotions](../.gitbook/assets/image%20%288%29.png)

![Assign emotion on output nodes](../.gitbook/assets/image%20%281%29.png)


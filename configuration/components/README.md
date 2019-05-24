---
description: >-
  Details how to use Date and Time Pickers and other modals such as Video,
  Audio, Images, Carousels, HTML and Tables.
---

# Components

{% hint style="info" %}
If you requires two components outputted inline for example **you can append a numerical ordering** to the **`extensions`** output parameter. 

For example you might want to show some button options along with an inline carousel.

```groovy
extensions1 = ${ExtensionHelper.displayClickableList(yesNoMaybeOptions,channel)}
```

```groovy
extensions2 = ${ExtensionHelper.displayImageCarousel(imageUrlArray,channel)}
```
{% endhint %}


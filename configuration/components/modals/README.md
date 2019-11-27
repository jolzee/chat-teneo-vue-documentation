---
description: >-
  Teneo responses with the help of the ExtensionHelper can send back custom
  MetaData to the front-end so that a variety of modals or inline components can
  be displayed in the respective view.
---

# Modal or Inline Components

## Positioning

By default all modals are shown in the middle of the page and they are rendered in their small sizing. To override this behavior on a modal basis just add an extra Output Parameter to the node containing the instructions to show a modal. 

```text
modalPosition = left/center/right/fullscreen
```

## Size

By default all modals are shown in their small size. To override this sizing on a modal basis just add an extra Output Parameter to the node containing the instructions to show a modal. 

```text
modalSize = small/medium/large/x-large
```

## Displaying multiple components

{% hint style="info" %}
If you require _**two or more**_ components outputted inline for example **you can append a numerical ordering** to the **`extensions`** output parameter. 
{% endhint %}

For example you might want to show some button options along with an inline carousel.

```groovy
extensions1 = ${ExtensionHelper.displayClickableList(yesNoMaybeOptions,channel)}
```

```groovy
extensions2 = ${ExtensionHelper.displayImageCarousel(imageUrlArray,channel)}
```

{% page-ref page="image.md" %}

{% page-ref page="image-carousel.md" %}

{% page-ref page="video.md" %}

{% page-ref page="audio.md" %}

{% page-ref page="table.md" %}

{% page-ref page="maps.md" %}

{% page-ref page="html.md" %}

{% page-ref page="forms/" %}

{% page-ref page="custom.md" %}




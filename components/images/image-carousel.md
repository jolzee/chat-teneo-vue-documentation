---
description: >-
  Display an array of Images in a modal as a set of carousel images. This modal
  will also contain the answer text.
---

# Image Carousel

## Modal

### Screenshot

![](../../.gitbook/assets/image-carousel.jpg)

### Output Parameter

```groovy
extensions = ${ExtensionHelper.displayImageCarousel(imageUrlArray,channel)}
```

### JSON

```javascript
{
	"name": "displayImageCarousel",
	"parameters": {
		"images": ["http://placeimg.com/640/360/any", "http://placeimg.com/640/360/any?u=2"]
	},
	"inline": false
}
```

## Inline



### Screenshot

![](../../.gitbook/assets/inline-carousel.jpg)

### Output Parameter

```groovy
extensions = ${ExtensionHelper.displayImageCarousel(imageUrlArray,channel,true)}
```

### JSON

```javascript
{
	"name": "displayImageCarousel",
	"parameters": {
		"images": ["http://placeimg.com/640/360/any", "http://placeimg.com/640/360/any?u=2"]
	},
	"inline": true
}
```


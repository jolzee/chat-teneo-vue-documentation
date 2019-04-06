---
description: Single image modal with accompanied answer text
---

# Image

## Modal

### Screenshot

![](../../../.gitbook/assets/image-modal.jpg)

### Output Parameter

```groovy
extensions = ${ExtensionHelper.displayImage(imageUrl,channel)}
```

### JSON

```javascript
{
	"name": "displayImage",
	"parameters": {
		"image_url": "https://www.fillmurray.com/640/360"
	},
	"inline": false
}
```

## Inline

### Screenshot

![](../../../.gitbook/assets/inline-image.jpg)

### Output Parameter

```groovy
extensions = ${ExtensionHelper.displayImage(imageUrl,channel,true)}
```

### JSON

```javascript
{
	"name": "displayImage",
	"parameters": {
		"image_url": "https://www.fillmurray.com/640/360"
	},
	"inline": true
}
```


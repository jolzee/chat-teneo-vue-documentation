# Multiple Components - Same Response

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


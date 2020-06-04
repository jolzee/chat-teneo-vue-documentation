---
description: >-
  In your answer you can embed links. You have some degree of control over what
  happens once that link is clicked.
---

# Hyperlinks

{% hint style="warning" %}
I know some works needs to be done to have these types of hyperlinks work in Modals. This was working but it looks to have been broken at some point. 
{% endhint %}

## Links that send text back to Teneo as a user input

### Answer Text in Output Node

You can output links in html or answer text that are then fed back into Teneo as user input.

```markup
<a href="#" class="sendInput">This will be sent to Teneo</a>
```

Alternatively:

```markup
<a href="#" class="sendInput" data-input="This will be sent to Teneo">This is just the anchor text</a>
```

## Links that open an link in an iframe when in Demo mode

### Answer Text in Output Node

```markup
<a href="https://somewebsite.com" class="openInIframe">This will open the page https://somewebsite.com in an iframe once clicked.</a>
```




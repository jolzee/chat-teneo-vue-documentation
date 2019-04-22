---
description: >-
  In your answer you can embed links that once clicked send back a user input to
  Teneo.
---

# Hyperlinks

{% hint style="warning" %}
I know some works needs to be done to have these types of hyperlinks work in Modals. This was working but it looks to have been broken at some point. 
{% endhint %}

## Studio

### Answer Text in Output Node

You can output links in html or answer text that are then fed back into Teneo as user input.

```markup
<a href="#" class="sendInput">This will be sent to Teneo</a>
```

Alternatively:

```markup
<a href="#" class="sendInput" data-input="This will be sent to Teneo">This is just the anchor text</a>
```


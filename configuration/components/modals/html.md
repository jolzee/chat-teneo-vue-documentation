---
description: Modal with custom HTML and accompanied answer text as the title
---

# HTML

## Output Parameter

```groovy
extensions = ${ExtensionHelper.displayPanel(htmlContent,channel)}
```

## JSON

```javascript
{
  "name"       : "displayPanelCard",
  "parameters" : {
    "content" : "<h1>My Custom HTML</h1>"
  }
}
```


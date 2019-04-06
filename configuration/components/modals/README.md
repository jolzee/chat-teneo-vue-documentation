---
description: >-
  Teneo responses with the help of the ExtensionHelper can send back custom
  MetaData to the front-end so that a variety of modals or inline components can
  be displayed in the respective view.
---

# Modal or Inline

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




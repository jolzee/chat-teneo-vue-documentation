---
description: You can have the UI present either a password or email field
---

# Field Types

## Email Field

The email field applies email validation against what's input. You will not be able to proceed until the validation completes. 

{% hint style="info" %}
You could probably bypass the email validation by using an ASR input..
{% endhint %}

### Screenshots

![](../../.gitbook/assets/e1.jpg)

![](../../.gitbook/assets/e2.jpg)

![](../../.gitbook/assets/e3.jpg)

### Output Parameter

```text
inputType = email
```

## Password Field

The password field will mask the users password as they enter it in. It will also ensure that once the password is sent to Teneo that the user's password is masked in the chat UI.

### Screenshots

![](../../.gitbook/assets/p3.jpg)

![](../../.gitbook/assets/p1.jpg)

![](../../.gitbook/assets/p2.jpg)

### Output Parameter

```text
inputType = password
```

## 


# Channel

Leopard sends `channel=webview` to Teneo along with every request. You will want to define a global variable in Teneo and populate it based off the value of this request parameter.

```groovy
if (engineEnvironment.getParameter("channel")) { 
    channel = engineEnvironment.getParameter("channel") 
}
```


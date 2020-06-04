# User's Time Zone

## Capture the User's Time Zone

Leopard automatically sends the user's time zone as a request parameter  \(`timeZone`\) to Teneo. This is useful in that you might want to properly greet the user based on the time of day. 

To capture the time zone in Teneo add this script to Pre-processing.

```groovy
if (engineEnvironment.getParameter("timeZone")){
	Lib_sUserTimeZone = engineEnvironment.getParameter("timeZone")
}
```

Alter the `On top` script in the default Teneo TDR `Greeting` flow to the following. The user then will be correctly greeted based off the time of day.

```groovy
TimeZone timeZone = TimeZone.getTimeZone(Lib_sUserTimeZone);
iHour = Integer.parseInt(String.format('%tH', new GregorianCalendar(timeZone)));
```

![Greeting Message](../../.gitbook/assets/greeting.png)


---
description: >-
  Leopard sends a bunch of useful request parameters to Teneo that can be used
  to personalize responses.
---

# Context Parameters

To have the location information sent to Teneo you must enable the following environment variable in you .env file. By default it is set to true.

```text
VUE_APP_SEND_LOCATION_LOGIN=true
```

### Variables Sent

The values will differ based off the location of the user chatting with Teneo via Leopard. You can access these variables in a pre-processing script from within Teneo Studio. 

```text
timeZone: America/Los_Angeles
city: Sammamish
continentCode: NA
continentName: North America
countryCode: US
countryName: United States
currencySymbol: $
currencyCode: USD
latitude: 47.5857
longitude: -122.0345
regionCode: WA
regionName: Washington
```


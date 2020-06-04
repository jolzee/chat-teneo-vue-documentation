---
description: >-
  Leopard sends a bunch of useful request parameters to Teneo that can be used
  to personalize responses.
---

# Location Context Parameters

To have the location information sent to Teneo you must enable the following [build configuration](../build-variables.md) variable. 

```text
location.login.sendAtLogin = true
```

### Variables Sent

The values will differ based off the location of the user chatting with Teneo via Leopard. You can access these variables in a pre-processing script from within Teneo Studio. 

```text
timeZone        : America/Los_Angeles  
city            : Sammamish            
continentCode   : NA                   
continentName   : North America        
countryCode     : US                   
countryName     : United States        
currencySymbol  : $                    
currencyCode    : USD                  
latitude        : 47.5857              
longitude       : -122.0345            
regionCode      : WA                   
regionName      : Washington           
```

### Retrieving in Pre-Processing within Teneo

```java
if (engineEnvironment.getParameter("timeZone")) { 
    timeZone = engineEnvironment.getParameter("timeZone") 
}

if (engineEnvironment.getParameter("city")) { 
    city = engineEnvironment.getParameter("city") 
}

if (engineEnvironment.getParameter("continentCode")) { 
    continentCode = engineEnvironment.getParameter("continentCode") 
}

if (engineEnvironment.getParameter("continentName")) { 
    continentName = engineEnvironment.getParameter("continentName") 
}

if (engineEnvironment.getParameter("countryCode")) { 
    countryCode = engineEnvironment.getParameter("countryCode") 
}

if (engineEnvironment.getParameter("currencySymbol")) { 
    currencySymbol = engineEnvironment.getParameter("currencySymbol") 
}

if (engineEnvironment.getParameter("currencyCode")) { 
    currencyCode = engineEnvironment.getParameter("currencyCode") 
}

if (engineEnvironment.getParameter("latitude")) { 
    latitude = engineEnvironment.getParameter("latitude") 
}

if (engineEnvironment.getParameter("longitude")) { 
    longitude = engineEnvironment.getParameter("longitude") 
}

if (engineEnvironment.getParameter("regionCode")) { 
    regionCode = engineEnvironment.getParameter("regionCode") 
}

if (engineEnvironment.getParameter("regionName")) { 
    regionName = engineEnvironment.getParameter("regionName") 
}
```


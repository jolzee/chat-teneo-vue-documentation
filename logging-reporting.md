---
description: >-
  Leopard can be configured to send front end activity logs to both Sentry
  (sentry.io) and/or LogRocket (logrocket.com)
---

# Logging / Reporting

{% embed url="https://logrocket.com/" caption="LogRocket" %}

{% embed url="https://sentry.io/" caption="Sentry" %}

To use either or both of these services you will need to sign up for an account and then populate the values for the following environmental variables.

| Key | Value |
| :--- | :--- |
| VUE\_APP\_SENTRY\_DSN | https://xxxxxxxxxxxxxxxxxx@sentry.io/xxxxxxxx |
| VUE\_APP\_LOG\_ROCKET | xxxxxx/projectname |

Depending on your build and requirements these keys can be in either `.env` `.env.development` `.env.development.local` `.env.qa` `.env.production` `.env.production.local`

More information of the hierarchy that Vue uses when referencing environment files can be found here:

{% embed url="https://cli.vuejs.org/guide/mode-and-env.html\#environment-variables" caption="Vue CLI" %}


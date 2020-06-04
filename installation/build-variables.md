---
description: >-
  Leopard's build process can be controlled though a commented JavaScript
  module.
---

# Build Variables

 Leopard is configured using **`/config/default.js`** which is a **commented** JavaScript module. You can either directly add your configuration to `default.js` or to an adjacent `local.js` which takes precedence and is added to `.gitignore`. The conversational solutions are configured through the [`.env.solution.json`](https://jolzee.gitbook.io/leopard/configuration/leopard-config-page#default-configuration) file in the root of the project. These changes are picked up if you run either `npm run serve` or `npm run build` .

## Leopard Environment Variables

If you would like to leverage [Live Chat](../integrations/live-chat.md), [Location Detection](../components/field-types.md#location-information), [Pusher Messaging]() or [Social Authentication](../integrations/social-authentication.md) then you will need to update your license keys in the `.env` properties file.  Know that you can define a `.env.local` file within the same directory. This file will be used for local builds. `.env.local` files are added to `.gitignore` so that your licence keys and config isn't publicly exposed.

```javascript
const config = {
  assets: {
    compressCss: true, // gzip and brotli compress CSS
    compressJavascript: true, // gzip and brotli compress JavaScript
    produceSourceMap: false // in production you probably want to disable
  },
  demoMode: true, // true = stores configs in local storage. In production it should be false
  /**
   * https://www.livechat.com/ integration - live chat handover
   */
  liveChatInc: {
    agentAssist: {
      /**
       * Server URL for creating agent assist canned responses -
       * https://github.com/jolzee/agent-assist-livechat-server-leopard
       */
      serverUrl: ""
    },
    key: "" // livechat.com license key
  },
  location: {
    /**
     * if you want to capture location information from the user then
     * provide a https://locationiq.com/ api key
     * https://jolzee.gitbook.io/leopard/configuration/response-options/field-types#location-information
     */
    locationIq: {
      key: ""
    },
    login: {
      /**
       * Capture and send geo location information at login.
       * Uses both https://ipapi.co/ip/ & http://www.geoplugin.net
       * This setting can be costly on first run.
       */
      sendAtLogin: false, // false = disabled, true = tries to obtain geo before greeting
      /**
       * Jaguar provides rest endpoint to proxy both the acquisition of the user's
       * IP and their geo location. This speeds up the whole process and deals with
       * any potential CORS issues.
       * https://github.com/jolzee/jaguar
       */
      serviceUrls: {
        geo: "", // https://my-jaguar.com/utils/geo
        ip: "" // https://my-jaguar.com/utils/ip
      }
    }
  },
  /**
   * Leopard can send debug information to both Log Rocket and Sentry.
   * If let absent nothing is sent.
   */
  logging: {
    logRocket: {
      key: "" // https://logrocket.com/
    },
    sentry: {
      key: "" // https://sentry.io/
    }
  },
  /**
   * Only applies when Leopard is embedded in production:
   * https://jolzee.gitbook.io/leopard/embedding
   */
  productionEmbed: {
    initialStateOpen: false, // should leopard automatically open on first load
    killSessionWhenClosed: false, // should the conversational session be closed when x is clicked
    showCloseButton: true, // allows you to hide the close button
    leopardTrustedDomains: [], // empty array = trust all domains // array of trusted domains - eg: ["https://my-domain.com", "https://my-other-domain.com"]
    enableScriptEval: false // this disabled the sending of JavaScript from Teneo Responses in production
  },
  /**
   * Social Authentication is provided through https://firebase.google.com/
   * Empty values signals no authentication
   */
  socialAuthentication: {
    firebase: {
      apiKey: "",
      authDomain: "",
      databaseUrl: "", // Firebase Realtime Database
      messagingSenderId: "",
      microsoft: {
        domainHint: "", // my-domain.com
        tenant: "" // Azure AD Tenant ID
      },
      projectId: "", // firebase project id
      providers: ["microsoft", "facebook", "google", "github"], // login and register will only show buttons for these providers
      storageBucket: ""
    }
  },
  solution: {
    location: {
      placeInStaticFolder: false, // false = loaded client side via JavaScript ; true = .env.solution.json is placed in /static/config.json
      sourceFile: ".env.solution.json" // relative path to your solution(s) config file - probably don't need to change
    }
  },
  ui: {
    configArea: {
      shareLink: {
        kuttItApiKey: "" // Optional - URL Shortener https://kutt.it/ can shortener shared links generated in the config area
      }
    },
    hideConfigMenu: false, // true = Set in production | false when in demo/development mode
    hideTeneoBranding: false // optionally hide Teneo Branding
  }
};

module.exports = config;

```

### Important Notes on Some Variables

<table>
  <thead>
    <tr>
      <th style="text-align:center">Environment Variable</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center"><code>solution.location.placeInStaticFolder</code>
      </td>
      <td style="text-align:left">
        <p>If set to <b><code>true</code></b> then the build process will place copy
          the <code>env.solution.json</code>to<code>/dist/static/config.json</code>.
          It will then make an AJAX request to load in your solution(s) settings.
          If you add a <code>.env.solution.json.token</code> file adjacent to the <code>.env.solution.json</code> file
          then that token file will also be copied as <code>/dist/static/config.json.token</code> file
          after the build completes. This is useful for those that might need to
          perform variable substitution prior to deployment in tools such as <b>Octopus Deploy</b>.</p>
        <p></p>
        <p>If set to <b><code>false</code></b> then instead of making an ajax request
          to load the default solution config from the static directory the configuration
          file located in <code>.env.solution.json </code>is moved into a <code>leopardConfig.*.js</code> file
          in <code>/dist/assets/js/</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>


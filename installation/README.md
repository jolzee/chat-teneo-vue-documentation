---
description: >-
  Code is stored in a Github and linked to at the top of this documentation. You
  will need to have Node.js and Git installed to be able to clone the repository
  and to build and deploy Leopard.
---

# Setup

{% tabs %}
{% tab title="Check List ✅" %}
<table>
  <thead>
    <tr>
      <th style="text-align:left">Steps</th>
      <th style="text-align:left">Where</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="extension-helper.md">Extension Helper</a>
      </td>
      <td style="text-align:left">Studio</td>
      <td style="text-align:left">Add the <a href="extension-helper.md">Extension Helper</a> groovy script
        to Teneo Studio as either a resource or to the Global Scripts</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="context-variables/">Global Variables &amp; Pre-processing Scripts</a>
      </td>
      <td style="text-align:left">Studio</td>
      <td style="text-align:left">In Teneo Studio you will want to define a number of global variables and
        pre-processing scripts</td>
    </tr>
    <tr>
      <td style="text-align:left">Install Prerequisites</td>
      <td style="text-align:left">Operating System</td>
      <td style="text-align:left"><a href="https://git-scm.com/downloads">Git</a>, <a href="https://nodejs.org/en/download/">Node.js</a>,
        <a
        href="https://cli.vuejs.org/">Vue CLI</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Clone Leopard</td>
      <td style="text-align:left">Operating System</td>
      <td style="text-align:left">
        <p><code>git clone </code><a href="https://github.com/jolzee/leopard-chat-ui-teneo"><code>https://github.com/jolzee/leopard-chat-ui-teneo</code></a>&lt;code&gt;&lt;/code&gt;</p>
        <p><code>cd leopard-chat-ui-teneo</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="build-variables.md">Build Variables</a>
      </td>
      <td style="text-align:left">Operating System</td>
      <td style="text-align:left">You can control various build aspects of Leopard through build variables.</td>
    </tr>
    <tr>
      <td style="text-align:left">Run Leopard</td>
      <td style="text-align:left">Operating System</td>
      <td style="text-align:left"><code>npm run serve</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Build for Production</td>
      <td style="text-align:left">Operating System</td>
      <td style="text-align:left"><code>npm run build</code>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Prerequisites" %}
The following tools need to be installed before you clone the code and try and build Leopard:

| Tool |  |
| :--- | :--- |
| [Git](https://git-scm.com/downloads) | [https://git-scm.com/downloads](https://git-scm.com/downloads) |
| [Node](https://nodejs.org/en/download/).js | [https://nodejs.org/en/download/](https://nodejs.org/en/download/) |
| [Vue CLI](https://cli.vuejs.org/) | `npm install -g @vue/cli` |
{% endtab %}
{% endtabs %}

### Windows Users

You will need to install `node-gyp` globally.  This is needed because some native node modules need to be compiled.  

#### **Start PowerShell as Administrator and run:**

{% hint style="info" %}
Only run this once Node.js is installed. The command below will take a while to complete but it only has to be run once. 
{% endhint %}

```bash
npm install --global windows-build-tools
```

## Code

The latest code is stored in [`GitHub`](https://github.com/jolzee/leopard-chat-ui-teneo).

{% embed url="https://github.com/jolzee/leopard-chat-ui-teneo" %}

## Clone Repository

```bash
git clone https://github.com/jolzee/leopard-chat-ui-teneo leopard
cd leopard
```

## Install Dependencies

This command will inspect the dependencies in the project's **package.json** file and will download them locally.

```bash
npm install
```

If you are on a version of **npm &gt; 6.0.0** you should preferably install dependencies using:

```groovy
npm ci
```

## Run Locally in Development Mode

To run a local version of Leopard for testing and development run the following.

```bash
npm run serve
```

The browser should automatically open to [http://localhost:8080/](http://localhost:8080/) once compiled. You can change code in the project and the Website should automatically reload. 

## Build for Production

The following command will compile, compress and minify all the code for production. The resulting HTML, CSS and JS code in the **`/dist`**folder can then be deployed to any web server.

```bash
npm run build
```


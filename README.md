# BoldBI Embedding Angular with NodeJS Sample

This project demonstrates how to render dashboards from your Bold BI server using an Angular frontend and a NodeJS backend.

## Dashboard view

![Dashboard View](/images/angular-dashboard.png)

## Requirements / Prerequisites

* [Node.js](https://nodejs.org/en/)
* [Visual Studio Code](https://code.visualstudio.com/download)

> **NOTE:** Node.js v18.18 to v20.20 are supported.

### Supported browsers

* Google Chrome, Microsoft Edge, and Mozilla Firefox.

## Configuration

* Ensure embed authentication is enabled on the `embed settings` page. If it is not enabled, follow these [instructions](https://help.boldbi.com/site-administration/embed-settings/#get-embed-secret-code?utm_source=github&utm_medium=backlinks) to enable it.

    ![Embed Settings](/images/enable-embedsecretkey.png)

* To download the `embedConfig.json` file, follow this [link](https://help.boldbi.com/site-administration/embed-settings/#get-embed-configuration-file?utm_source=github&utm_medium=backlinks). See the images below for guidance.

    ![Embed Settings Download](/images/download-embedsecretkey.png)
    ![EmbedConfig Properties](/images/embedconfig-file.png)

* Copy the downloaded `embedConfig.json` into the project at the expected location (the sample's `angular` and `nodejs` folders include examples of where to place it). 

    ![EmbedConfig image](/images/embedconfig-location.png)

## Run the Sample via Command Line

### NodeJS backend (API)

1. Open a terminal and navigate to the `nodejs` folder.
2. Install dependencies:

```bash
cd nodejs
npm install
```

3. Start the NodeJS server (the server entry is `embed.js`):

```bash
node embed.js
```

The server will listen on the port configured in `embed.js` and expose the embedding API used by the Angular frontend.

### Angular frontend

1. Open a terminal and navigate to the `Angular` folder.
2. Install dependencies:

```bash
cd angular
npm install
```

3. Start the Angular development server:

```bash
npm start
```

The Angular app typically runs at `http://localhost:4200` — open that URL in your browser.

## Run Using Visual Studio Code

* Open the workspace in Visual Studio Code.

### NodeJS backend via VS Code

1. Open the integrated terminal, navigate to `nodejs`, and run `npm install`.
2. Start the server with `node embed.js`.

### Angular frontend via VS Code

1. Open the integrated terminal, navigate to `angular`, and run `npm install`.
2. Start the frontend with `npm start`.

## Important notes

Do not store passwords or other sensitive information in configuration files in production. Use a secure secret store (for example, Key Vault) to protect credentials.
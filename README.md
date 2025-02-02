# Kentico Cloud sample Vue.js single-page application
[![Build Status](https://api.travis-ci.com/Kentico/cloud-sample-app-vue.svg?branch=master)](https://travis-ci.com/Kentico/cloud-sample-app-vue)
[![Live Demo](https://img.shields.io/badge/live-demo-brightgreen.svg)](http://kentico-cloud-sample-app-vue.surge.sh)
[![Stack Overflow](https://img.shields.io/badge/Stack%20Overflow-ASK%20NOW-FE7A16.svg?logo=stackoverflow&logoColor=white)](https://stackoverflow.com/tags/kentico-cloud)

This is a sample website written in JavaScript utilizing the Kentico Cloud Delivery API to manage and retrieve content. You can register your account for free at <https://app.kenticocloud.com>.

## Application setup

1. Install the latest version of NodeJS and npm. You can download both at <https://nodejs.org/en/download/>.
2. Clone the sample application repository.
3. Navigate to the root folder of the application in the command line.
4. Type `npm install` to install required npm packages.
5. Type `npm run serve` to start a development server.
6. The application opens in your browser at <http://localhost:8080>.

### Connecting to your sample project

At the first run of the app, you'll be presented with a configuration page. It will allow you to connect the app to your Kentico Cloud sample project or create a new one. You'll also be able to start a trial and convert to a free plan when the trial expires.

* If you want to open the configuration page after the project is already connected to the app. Just open url <http://localhost:8080/Admin/Configuration>.

Alternatively, you can connect your project manually as per the chapter below.

#### Connecting to your project manually

If you want to change the source Kentico Cloud project, follow these steps:

1. In Kentico Cloud, choose Project settings from the app menu.
2. Under Development, choose API keys.
3. Copy your Project ID.
4. Create and open a `.env.local` file in the sample application folder.
5. On the first line, add your Project ID constant using the format `VUE_APP_PROJECT_ID=00000000-0000-0000-0000-000000000000`.
6. Save the file.
7. Then u can run it.

When you now run the application, it will retrieve the content from your sample project. This set up has higher priority then [setting your sample project by the Configuration page](#connecting-to-your-sample-project).

## Previewing content from your project

To preview unpublished content in the sample application, follow these steps:

1. In Kentico Cloud, choose Project settings from the app menu.
2. Under Development, choose API keys.
3. Copy your Project ID and Preview API key.
4. Create and open a `.env.local` file in the sample application folder.
5. On the first line, add your Project ID constant using the format `VUE_APP_PROJECT_ID=00000000-0000-0000-0000-000000000000`.
6. On the next line, add your Preview API key using the format `VUE_APP_PREVIEW_API_KEY=00000000-0000-0000-0000-000000000000`.
7. Save the file.

When you now run the application, you will see all project content including the unpublished version of content items.

## Content administration

1. Navigate to <https://app.kenticocloud.com> in your browser.
2. Sign in with your credentials.
3. Manage content in the content administration interface of your sample project.

You can learn more about content editing with Kentico Cloud in the [documentation](http://help.kenticocloud.com/).

## Content delivery

You can retrieve content either through the Kentico Cloud Delivery SDKs or the `Kentico Cloud Delivery` API:

* For published content, use `https://deliver.kenticocloud.com/PROJECT_ID/items`.
* For unpublished content, use `https://preview-deliver.kenticocloud.com/PROJECT_ID/items`.

For more info about the API, see the [API reference](https://developer.kenticocloud.com/reference).

You can find the Delivery and other SDKs at <https://github.com/Kentico>.

## Deployment

You can use, for example, [surge](http://surge.sh/) to deploy your app live. Check out the step-by-step guide on our [blog](https://kenticocloud.com/blog/3-steps-to-rapidly-deploy-headless-single-page-app).

![Analytics](https://kentico-ga-beacon.azurewebsites.net/api/UA-69014260-4/Kentico/cloud-sample-app-vue?pixel)

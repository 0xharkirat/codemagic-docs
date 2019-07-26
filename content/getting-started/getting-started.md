---
categories:
  - Getting started with Codemagic CI/CD
description: Running the first build on Codemagic without any configuration
facebook_description: ''
facebook_image: ''
facebook_title: ''
thumbnail: ''
title: Running the first build
twitter_image: ''
twitter_title: ''
twitterDescription: ''
weight: 2
---

Upon login, Codemagic will automatically display the list of apps in your repository. Select a Flutter app and start the very first build with preconfigured defaults by clicking **Start your first build**.

{{< figure size="" src="/uploads/2019/07/app_dashboard.PNG" caption="Codemagic Applications page" >}}

Codemagic will then fetch your app sources, create **webhooks** for automatic building and run a debug build of your master branch for both iOS and Android using the latest stable version of Flutter. If you have any **tests** in your project, these will be run too. All the while, you can monitor the build progress step by step right in your browser and expand each step for more details.

{{< figure size="" src="/uploads/2019/07/build_log_publishing.png" caption="Overview of a successful build" >}}

After the build has finished successfully, you will immediately have **artifacts** available for download which you will also receive on the email that was configured for the app repository.

You can then continue to customize how you want Codemagic to build, test and publish your app in **App settings**.

{{< figure size="" src="/uploads/2019/07/app_settings.png" caption="App settings page" >}}

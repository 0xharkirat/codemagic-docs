---
categories:
  - Custom script examples
date: '2019-04-07T12:57:59+03:00'
description: Create a Git tag referencing your app version
menu:
  docs_sidebar:
    weight: 1
title: Add a Git tag with app version
weight: 2
---

You can use this **pre-publish** script to create a Git tag referencing your app version. The script will check if the build was successful before updating the app version.

1. Save your Git service username and email address as [environment variables](https://docs.codemagic.io/building/environment-variables/) (e.g. `GIT_USERNAME` and `GIT_EMAIL`).
2. Add the following **pre-publish** script.

```
       #!/usr/bin/env sh

       set -e # exit on first failed commandset
       set -x # print all executed commands to the log

       if [ "$FCI_BUILD_STEP_STATUS" == "success" ]
       then
         new_version=v1.0.$BUILD_NUMBER
         git config --global user.name $GIT_USERNAME
         git config --global user.email $GIT_EMAIL
         git tag $new_version
         git push --tags
       fi
```

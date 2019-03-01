# Changelog

## 4333796-alpha02
* Pre-update the Android SDK tools, platform tools, platforms and build tools 27 & 28, extra repositories
* Make the Android SDK directory a Docker volume for it to be writable

## 4333796-alpha01
* Remove all the extra stuff from thyrlian's original project (Publish scripts, static assets, miscellaneous scripts, gradle-server docker image, ssh related files for the android-sdk docker image, vnc related files for the android-sdk docker image and supervisord related files from android-sdk docker image)
* Remove everything from the Dockerfile but the SDK downloading and license accepter
* Remove the extra license hashes (only accept the SDK's targetted revision's licenses)
* Change the base image to jenkins/ssh-slave

## Anterior changes
The changelog of Jing Li's original AndroidSDK docker image can be found [on its repository](https://github.com/thyrlian/AndroidSDK/blob/master/CHANGELOG.md).
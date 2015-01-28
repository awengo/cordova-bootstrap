# cordova-bootstrap

A web app that can be run in the browser or deployed to a hybrid app.

The following technologies are used in the app:
* Apache Cordova `http://cordova.apache.org/`
* Twitter Bootstrap `http://getbootstrap.com/`
* FT Fastclick `https://github.com/ftlabs/fastclick`

## Installation and running tasks

Install [Apache Cordova](http://cordova.apache.org/) or using the npm command:

    npm install cordova

## Running the app during development

To run as a webpage, navigate to the folder and open the first page in your web browser. 

    www/index.html

## Running the app on a device

Install xCode from Apple developer tools and ensure you have logged into an Apple Developer Account. Connect your device to xCode beforehand to ensure the device is recognised as a development device and the keys are signed. Then prepare and run the app using:

    cordova prepare
    cordova run

If your device is connected it should copy it across and launch automatically on the device. Otherwise it will default to the iOS simulator that comes with xCode. If you have multiple devices connected you can target a build/run command using

    cordova run ios
    cordova emulate ios --target="iPad"
    
Cordova caches plugins, So if you make any changes to a plugins code you can force a reset using the following command:

    cordova platform remove ios; cordova platform add ios; cordova run ios
    
If you have issues with cordova not opening the app automatically or not exiting after quitting, you can use the following command in your terminal to force quit all cordova processes:

    killall ios-deploy
    
To publish the app for distribution on a remote device follow these guides:

    http://stackoverflow.com/questions/20487074/can-we-install-an-unpublished-ios-app-on-a-remote-device
    https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/TestingYouriOSApp/TestingYouriOSApp.html

## Directory Layout

    www/                --> Static html templates
      css/              --> Stylesheet files
      img/              --> Image files
      index.html        --> Homepage
      js/               --> Javascript functionality

## Contact

For more information please contact kmturley.
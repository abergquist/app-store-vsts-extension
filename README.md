<table style="width: 100%; border-style: none;"><tr>
<td width="140px" style="text-align: center;"><img src="apple_default.png" style="max-width:100%" /></td>
<td><strong>Visual Studio Team Services Extension for the App Store</strong><br />
<i>Provides build/release tasks that enable performing continuous delivery to Apple's App Store from an automated VSTS build or release definition</i><br />
<a href="#">Install now!</a>
</td>
</tr></table>

# Visual Studio Team Services Extension for the App Store

This extension contains a set of deployment tasks which allow you to automate the release and promotion app updates to Apple's App Store from your CI environment. This can reduce the effort needed to keep your beta and production deployments up-to-date, since you can simply push changes to the configured source control branches, and let your automated build take care of the rest.

## Prerequisites

In order to automate the release of app updates to the App Store, you need to have manually released at least one version of the app beforehand.

## Quick Start

Once you have created or retrieved credentials for your App Store account, then perform the following steps to automate releasing updates from a VSTS build or release definition:

1. Install the App Store extension from the [VSTS Marketplace](https://marketplace.visualstudio.com/items/ms-vsclient.app-store)

2. Go to your Visual Studio Team Services or TFS project, click on the **Build** tab, and create a new build definition (the "+" icon) that is hooked up to your project's appropriate source repo

3. Click **Add build step...** and select the neccessary tasks to generate your release assets (e.g. **Gulp**, **Cordova Build**)

4. Click **Add build step...** and select **App Store - Release** from the **Deploy** category

5. Configure the **App Store - Release** task with the desired authentication method, the generated IPA file path, and the desired release track.

6. Click the **Queue Build** button or push a change to your configured repo in order to run the newly defined build pipeline

7. Your app changes will now be automatically published to the App Store!

## Configuring Your App Store Publisher Credentials

In addition to specifying your publisher credentials directly within each build task, you can also configure your credentials globally and refer to them within each build or release definition as needed. To do this, perform the following steps:

1. Setup an Apple developer account (https://developer.apple.com/)

2. Go into your Visual Studio Team Services or TFS project and click on the gear icon in the upper right corner

3. Click on the **Services** tab

4. Click on **New Service Endpoint** and select **Apple App Store**

5. Give the new endpoint a name and enter the credentials for the developer account you generated in step#1.

6. Select this endpoint via the name you chose in #5 whenever you add either the **App Store - Release** or **App Store - Promote** tasks to a build or release definition 

## Contact Us

[Report an issue](https://github.com/Microsoft/app-store-vsts-extension/issues)


Apple and the Apple logo are trademarks of Apple Inc., registered in the U.S. and other countries. App Store is a service mark of Apple Inc.
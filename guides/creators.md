---
description: Monetize your space.
---

# Creators

This guide will show you how to create an ad space step-by-step. Before proceeding, make sure you've got MetaMask installed and set to the correct network (currently Rinkeby). See our MetaMask guide for further instructions.

## Make an Ad Space

The first thing you want to do is create the ad space. To begin creating an ad space, click on "Ad Spaces" in the top left.

![](<../.gitbook/assets/creator flow 1.png>)

When you're first starting out, you won't have any ad spaces. That's okay, we'll create a new one now.

![](<../.gitbook/assets/creator flow 2.png>)

Give your ad space a name, like "Alice's Gaming Stream". For the location URL, use your Twitch profile URL if you're going to be using OBS, or use the URL of your WebXR experience if you're going to be using Zesty's A-Frame/react-three-fiber/three.js SDKs. Give a simple description and an image for advertisers to be able to get a sense of what your space looks like (since our example space doesn't exist, we'll just use a placeholder logo).

![](<../.gitbook/assets/creator flow 3.png>)

When making your ad space image, you'll want to get a good shot with where the ad will eventually be in your space. To do this, you can integrate the base component into your scene with some default values.

{% tabs %}
{% tab title="A-Frame" %}
1a) If you want to import the  tag, copy and paste this into the \<head>:\
`<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-aframe-sdk.js"></script>`

1b) If you are using it in an NPM project, install it like so:\
`npm install '@zestymarket/aframe-sdk'`\
Once installed, import the ZestyAd component:\
`import * as Zesty from '@zestymarket/aframe-sdk';`

2\) In the \<a-scene>, copy and paste:\
`<a-entity visible="true" zesty-ad="adSpace: 0; creator: 0x0000000000000000000000000000000000000000; adFormat: tall" position="0 2 0"></a-entity>`
{% endtab %}

{% tab title="babylon.js" %}
1a) If you want to import the  tag, copy and paste this into the \<head>:\
`<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-babylonjs-sdk.js"></script>`

1b) If you are using it in an NPM project, install it like so:\
`npm install '@zestymarket/babylonjs-sdk'`\
Once installed, import the ZestyAd component:\
`import ZestyAd from '@zestymarket/babylonjs-sdk';`

2\) Make sure you have a reference to your scene and WebXRHelper (if applicable), then copy and paste:\
`const zestyAd = new ZestyAd("0", "0x0000000000000000000000000000000000000000", "tall", 3, scene, xrHelper);`\
Substitute variable names as needed. The last parameter for the WebXRHelper is optional.
{% endtab %}

{% tab title="react-three-fiber" %}
1a) If you want to import the  tag, copy and paste this into the \<head>:\
`<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-r3f-sdk.js"></script>`

1b) If you are using it in an NPM project, install it like so:\
`npm install '@zestymarket/r3f-sdk'`\
Once installed, import the ZestyAd component:\
`import ZestyAd from '@zestymarket/r3f-sdk';`

2\) In the \<a-scene>, copy and paste:\
`<ZestyAd adSpace={'0'} creator={'0x0000000000000000000000000000000000000000'} adFormat={'tall'} position={[0, 2, 0]} />`
{% endtab %}

{% tab title="three.js" %}
1a) If you want to import the  tag, copy and paste this into the \<head>:\
`<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-threejs-sdk.js"></script>`

1b) If you are using it in an NPM project, install it like so:\
`npm install '@zestymarket/threejs-sdk'`\
Once installed, import the ZestyAd component:\
`import ZestyAd from '@zestymarket/threejs-sdk';`

2\) In the your scene setup, copy and paste:`const zestyAd = new ZestyAd("0", "0x0000000000000000000000000000000000000000", "tall", 3);`\
`scene.add(zestyAd);`
{% endtab %}

{% tab title="Wonderland Engine" %}
1a) To just use the bundled file, download it by right-clicking this link and saving it into your project folder: [https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js](https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js).

1b) If you are using NPM in your Wonderland project, install it like so:\
`npm install '@zestymarket/wonderland-sdk'`

2\) In your Wonderland project, open your Project Settings view and make sure that the SDK is being included in your JavaScript source paths.

3\) Create a new mesh, set its type to PrimitivePlane, and create a new material for it as well. Set the pipeline to either "Phong Opaque Textured" or "Flat Opaque Textured."

4\) Add the zesty-ad component to your mesh's object and fill in the following fields as such:\
**creator**\
`0x0000000000000000000000000000000000000000`\
**adSpace**\
****`0`\
**adFormat**\
****`tall`
{% endtab %}

{% tab title="OBS" %}
Add a browser source, then copy and paste the following url:\
[https://www.zesty.games/obs?creator=0x0000000000000000000000000000000000000000\&adSpace=0](https://www.zesty.games/obs?creator=0x0000000000000000000000000000000000000000\&adSpace=0)
{% endtab %}

{% tab title="Web" %}
1a) If you want to import the  tag, copy and paste this into the \<head>:\
`<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-web-sdk.js"></script>`

1b) If you are using it in an NPM project, install it like so:\
`npm install '@zestymarket/web-sdk'`

2\) In your page's \<body>, copy and paste:\
`<zesty-web adspace="0" creator="0x0000000000000000000000000000000000000000" width="100px"></zesty-web>`
{% endtab %}
{% endtabs %}

You can adjust the ad format to "tall", "wide", or "square" depending on your needs.

After you've filled out all of the necessary information, click "Done". You will then receive a notification from MetaMask to confirm a transaction. By creating this ad space, you are minting an NFT that will be used for Zesty Market auctions, so it will require some gas. Press "Confirm" and wait for the token to be minted.

![](<../.gitbook/assets/creator flow 4.png>)

After all necessary information is uploaded to IPFS (our storage protocol), you'll be redirected to view all of your ad spaces!

![](<../.gitbook/assets/creator flow 5.png>)

## Integrating Zesty

Now that you've created an ad space, click on the ad space and go to the "Integration" tab.

![](<../.gitbook/assets/creator flow 6.png>)

Here you'll find the instructions for integrating the ad space into all of our supported platforms. Zesty currently supports integrations with A-Frame, react-three-fiber, three.js, and OBS.

## Make an Auction

Now that you have an ad space which represents your digital space, you can create auctions to be bid on by an advertiser/sponsor. You'll start with none, but click on the "Auctions" tab and then the "Create Auction" button to get started.

![](<../.gitbook/assets/creator flow 7.png>)

You'll be presented with an "Approve" and "Deposit" button. In the same way that creating an ad space created an NFT, creating an auction also involves depositing a Zesty NFT into the marketplace. Click "Approve" and then "Confirm" in MetaMask. This will incur a small fee.

![](<../.gitbook/assets/creator flow 8.png>)

Once you've approved the transaction, click "Deposit" to deposit the NFT and create a new auction. This step will require a small amount of gas.

![](<../.gitbook/assets/creator flow 9.png>)

Click on a calendar day to start configuring a timeslot, where you can select a start price, start date, and end date for your auction, then hit confirm. You can bring this window up again by clicking the timeslot on the calendar, or simply adjust the time period by dragging either the left or right handles on the timeslot.

![](<../.gitbook/assets/creator flow 10.png>)

After you've selected the desired date range and starting price, click on "Confirm". This is the last step that will require gas.

![](<../.gitbook/assets/creator flow 11.png>)

Once the transaction has been approved, your new auction will be listed under your ad space.

![](<../.gitbook/assets/creator flow 12.png>)

 Also, now that you have an active auction, your ad space will appear on the market!

![](<../.gitbook/assets/creator flow 13.png>)

## After The Auction

After the ad slot has been purchased and there is sufficient proof that you had shown the ad for the agreed period of time, you'll be able to withdraw the amount used to purchase your Zesty NFT.

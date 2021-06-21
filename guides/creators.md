---
description: Monetize your space.
---

# Creators

Before starting this tutorial, make sure you switch to "Creator" mode so you can see all of the features available to you.

![Outdated Image](../.gitbook/assets/image%20%287%29.png)

## Make an Ad Slot

The first thing you want to do is create an ad slot that allows you to group multiple NFTs together. To begin creating an ad slot, click on "Ad Slots".

![Outdated Image](../.gitbook/assets/image%20%2814%29.png)

When you're first starting out, you won't have any ad slots. That's okay, we'll create a new one now.

![Outdated Image](../.gitbook/assets/image%20%2811%29.png)

Give your ad slot a name, like "Alice's Gaming Stream". For the location URL, use your Twitch profile URL if you're going to be using OBS, or use the URL of your WebXR experience if you're going to be using Zesty's A-Frame/three.js SDKs. Give a simple description and an image for advertisers to be able to get a sense of what your space looks like.

![Outdated Image](../.gitbook/assets/image%20%281%29.png)

After you've filled out all of the necessary information, click "Done". After all necessary information is uploaded to IPFS \(our storage protocol\), you'll be redirected to view all of your ad slots!

![Outdated Image](../.gitbook/assets/image%20%285%29.png)

## Integrating Zesty

Now that you've created an ad slot, click on the "information" button to see integration instructions.

![Outdated Image](../.gitbook/assets/image%20%284%29.png)

You will find the instructions on this page for integrating the ad slot into three.js, A-Frame and OBS. You will only need to use one.

{% tabs %}
{% tab title="OBS" %}
Add the Browser as a source in OBS, set the width to 550px and height to 200px, and use the below URL:

[https://www.zesty.games/obs?publisher={YOUR](https://www.zesty.games/obs?publisher={YOUR) PUBLISHER ID}&tokenGroup={YOUR TOKEN GROUP}
{% endtab %}

{% tab title="three.js" %}
**Step 1:** After importing three.js into your project, include the following script in your html file:

`<script src="`[`https://lib.zesty.market/zesty-threejs-sdk.js`](https://lib.zesty.market/zesty-threejs-sdk.js)`"></script>`

**Step 2:** Add the ZestyAd object with your ad slot's parameters and add it to the scene:

`let zestyAd = new ZestyAd(2, 3, "YOUR_AD_SLOT_TOKENGROUP", "YOUR_PUBLISHER_ID");    
scene.add(zestyAd);`

**Note:** The first and second parameters are used for the width and height of the ZestyAd. Make sure this corresponds to the size of the ad space on Zesty.
{% endtab %}

{% tab title="A-Frame" %}
**Step 1:** In the head \(after the A-Frame import\), copy and paste:

`<script src="`[`https://lib.zesty.market/zesty-aframe-sdk.js`](https://lib.zesty.market/zesty-aframe-sdk.js)`"></script>`

**Step 2:** Add the &lt;a-entity&gt; with the zesty-ad component into your scene:

`<a-entity zesty-ad="publisher: YOUR_PUBLISHER_ID; tokenGroup: YOUR_AD_SLOT_TOKENGROUP"</a-entity>`
{% endtab %}
{% endtabs %}

## Minting NFTs

Now that you have an ad slot which represents your digital space, you can mint an NFT to sell to an advertiser/sponsor. You'll start with none, but click on "Mint New" to get started.

![Outdated Image](../.gitbook/assets/image%20%2813%29.png)

Once you've selected your ad slot from the drop-down, select a date range you would like to offer the ad slot for.

![Outdated Image](../.gitbook/assets/image%20%2812%29.png)

After you've selected the desired date range, click on "Mint". This step will require gas.

## The Auction

Now that you've minted your own ad space, you're ready to put your ad slot up for auction!

## After The Auction

After the ad slot has been purchased and there is sufficient proof that you had shown the ad for the agreed period of time, you'll be able to withdraw the amount used to purchase your Zesty NFT.


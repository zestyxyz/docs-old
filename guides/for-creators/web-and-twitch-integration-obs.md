---
description: How to add your Space NFT to your livestream via OBS Studio or Streamlabs OBS.
---

# Web & Twitch Integration (OBS)

## Web

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-web-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/web-sdk'
```

#### Step 2

In your page's `<body>`, copy and paste:

```
<zesty-web space="0" creator="0x0000000000000000000000000000000000000000" width="100px"></zesty-web>
```

If you wish to opt into enabling a beacon on your space, copy and paste:

```
<zesty-web space="0" creator="0x0000000000000000000000000000000000000000" width="100px" beacon="true"></zesty-web>
```

## OBS (for Livestreaming)

For livestreaming on platforms like Twitch, you can use below guide to add Zesty space into your stream scenes.

### 1. Obtaining Source Link

Go to your [Spaces](https://app.zesty.market/spaces) page and click on the Space you'd want to integrate.

![](../../.gitbook/assets/Zesty\_OBS\_1.png)

On your Space, scroll down and click on Integration section. The OBS integration settings should be showing by default, if not, find OBS Integrations under the Select Integration dropdown bar.

Copy the browser source link.

### 2. Setting up in OBS

![](../../.gitbook/assets/Zesty\_OBS\_2.png)

On your OBS program, click on Add New Source. It's is usually the + button under the Sources panel.

Find Browser or Browser Source and click on the option.

![](../../.gitbook/assets/Zesty\_OBS\_3.png)

The Properties window for the Browser Source will pop-up and you can paste the link from Step 1 into the URL field. Click OK.

![](../../.gitbook/assets/Zesty\_OBS\_4.png)

You'll see the browser source with Zesty logo in your preview panel.

Right-click on the source and choose Interact. The Interacting with Browser window will pop-up and you'll be able to interact with the browser.

![](../../.gitbook/assets/Zesty\_OBS\_5.png)

In the window, you may choose a few options:

* **Network** = Choose between Polygon or Rinkeby. Choose Polygon here as Rinkeby is a test network.
* **Default Banner Style** = Choose between Standard or Minimal default banner. Default banner is the banner that's showing when there are no Campaign running for the space.

![](../../.gitbook/assets/Zesty\_OBS\_6.png)

Once you've chosen your network and browser style, you should now do a little edit to hide the settings from being visible to viewers.

On the bottom edge of the source, press Alt and click on the line. You'll be able to crop the source instead of resizing it. The cropped line is green in colour.

![](../../.gitbook/assets/Zesty\_OBS\_7.png)

Finally, rearrange and place the banner where you want it to show. On the example above, I've added it at the bottom left of the scene so it doesn't distract from my livestream.

And that's it. You're done with OBS integration!

### **Watch our video to see the entire process:** <a href="#watch-our-video-to-see-the-entire-process" id="watch-our-video-to-see-the-entire-process"></a>

{% embed url="https://www.youtube.com/watch?v=a9i8ULRwcUI" %}

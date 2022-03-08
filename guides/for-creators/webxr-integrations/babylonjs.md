# babylon.js

Repository: https://github.com/zestymarket/sdk/tree/main/babylonjs

#### Importing the SDK

**NPM Project** - install it like so:

```
npm install '@zestymarket/babylonjs-sdk'
```

Once installed, import the ZestyBanner component:

```
import * as Zesty from '@zestymarket/babylonjs-sdk';
```


**HTML Tag** - Paste this into the `<head>`:

Zesty can be imported through a single HTML page, no need to install it as a Node Package.

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-babylonjs-sdk.js"></script>
```

#### Bringing the Zesty Banner into your scene

Make sure you have a reference to your scene and WebXRHelper (if applicable), then copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper);
```

Replace `0` with your Space ID and  `0x0000000000000000000000000000000000000000` with your wallet address

Substitute variable names as needed. The last parameter for the WebXRHelper is optional.

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper, true);
```


#### Customizing your banner display

These are the available attributes for your banner:

**space**
*required*

String: The ID of your space.

**creator**
*required*

String: The wallet address of the creator of the space

**network**
*optional - defaults to `polygon`*

String: The network in which your space NFT was minted

**format**
*required*

String: Specify format of your ad space `tall`, `wide`, or `square`

- Tall - 3:4
- Wide - 4:1
- Square - 1:1

**style**
*optional*

String: Style of your placeholder image, which notifies viewers that the ad space is available

**height**
*optional*

Integer: Scale the banner to your liking. Default value is `1`

**beacon**
*optional*

Boolean: Setting beacon to `true` allows you to view analytics on your space page

**Source**

```
export default class ZestyBanner {
  constructor(space, creator, network, format, style, height, scene, webXRExperienceHelper = null, beacon = false) {
    const options = {
      height: height,
      width: formats[format].width * height
    };
```
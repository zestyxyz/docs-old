# babylon.js

Repository: https://github.com/zestymarket/sdk/tree/main/threejs

#### Importing the SDK

**NPM Project** - install it like so:

```
npm install @zestymarket/threejs-sdk'
```

Once installed, import the ZestyBanner component:

```
import * as Zesty from '@zestymarket/threejs-sdk';
```


**HTML Tag** - Paste this into the `<head>`:

Zesty can be imported through a single HTML page, no need to install it as a Node Package.

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-threejs-sdk.js"></script>
```

#### Bringing the Zesty Banner into your scene

In the your scene setup, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3);
scene.add(zestyBanner);
```
Replace `0` with your Space ID and  `0x0000000000000000000000000000000000000000` with your wallet address

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, null, true);
scene.add(zestyBanner);
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
/**
   * @constructor
   * @param {string} space The space ID
   * @param {string} creator The wallet ID of the creator
   * @param {string} network The network to connect to ('rinkeby' or 'polygon')
   * @param {string} format The format of the default banner
   * @param {Number} height Height of the banner
   * @param {THREE.WebGLRenderer} renderer Optional field to pass in the WebGLRenderer in a WebXR project
   */
  constructor(space, creator, network, format, style, height, renderer = null, beacon = false) {
    super();
```
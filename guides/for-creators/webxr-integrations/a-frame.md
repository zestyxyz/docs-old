## A-Frame

#### Importing the SDK

**NPM Project** - install it like so:

```
npm install '@zestymarket/aframe-sdk'
```

Once installed, import the ZestyBanner component:

```
import * as Zesty from '@zestymarket/aframe-sdk';
```


**HTML Tag** - Paste this into the `<head>`:

_Zesty can be imported through a single HTML page, no need to install it as a Node Package.

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-aframe-sdk.js"></script>
```


#### Bringing the Zesty Banner into your scene

In the `<a-scene>`, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard" position="0 2 0"></a-entity>
```

Replace `space: ` and  `creator: ` with your space number and wallet address

To opt into enabling a beacon for your space, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard; beacon: true" position="0 2 0"></a-entity>
```

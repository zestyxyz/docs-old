## A-Frame

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-aframe-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/aframe-sdk'
```

Once installed, import the ZestyBanner component:

```
import * as Zesty from '@zestymarket/aframe-sdk';
```

#### Step 2

In the `<a-scene>`, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard" position="0 2 0"></a-entity>
```

To opt into enabling a beacon for your space, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard; beacon: true" position="0 2 0"></a-entity>
```

## babylon.js

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-babylonjs-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/babylonjs-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/babylonjs-sdk';
```

#### Step 2

Make sure you have a reference to your scene and WebXRHelper (if applicable), then copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper);
```

Substitute variable names as needed. The last parameter for the WebXRHelper is optional.

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper, true);
```
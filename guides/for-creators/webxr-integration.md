---
description: These are the steps to integrate Zesty into a WebXR experience.
---

# WebXR Integration

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

## Cryptovoxels

**Step 1**

Create an image in your Cryptovoxels parcel.

**Step 2**

Set the scale of the image to correspond with your space's format. For reference, the aspect ratios on each format are:

* Tall - 3:4
* Wide - 4:1
* Square - 1:1

**Step 3**

Change the Blend mode from Multiply to Combine, unless you would like the image to be affected by lighting.

**Step 4**

Set the Transparency mode to Alpha Blended.

**Step 5**

Under Display, make sure Stretch is checked.

**Step 6**

In the Script section, copy and paste the script located here:

[https://github.com/zestymarket/sdk/blob/main/cryptovoxels/integration.js](https://github.com/zestymarket/sdk/blob/main/cryptovoxels/integration.js)

**Step 7**

At the end of the script, copy this line to call the loadBanner function (modify according to your own space information):

```
loadBanner('0', '0x0000000000000000000000000000000000000000', 'polygon', 'tall', 'standard');
```

## react-three-fiber

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-r3f-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/r3f-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/r3f-sdk';
```

#### Step 2

In your VR Canvas component, copy and paste:

```
<ZestyBanner space={'0'} creator={'0x0000000000000000000000000000000000000000'} format={'tall'} style={'standard'} position={[0, 2, 0]} />
```

## three.js

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-threejs-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/threejs-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/threejs-sdk';
```

#### Step 2

In the your scene setup, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3);
scene.add(zestyBanner);
```

## Unity

**Step 1**

Download the [zesty-unity-sdk package](https://ipfs.io/ipns/lib.zesty.market/zesty-unity-sdk.unitypackage).

**Step 2**

Open your Unity project and import the package through `Assets > Import Package > Custom Package`.

**Step 3**

Add the ZestySDK prefab to your hierarchy.

**Step 4**

Add the Banner prefab and configure the space ID, creator ID, format, and style based on your space details from the Zesty marketplace.

## Wonderland Engine

#### Step 1a

To just use the bundled file, download it by right-clicking this link and saving it into your project folder: [https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js](https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js)

#### Step 1b

If you are using NPM in your Wonderland project, install it like so:

```
npm install '@zestymarket/wonderland-sdk'
```

#### Step 2

In your Wonderland project, open your Project Settings view and make sure that the SDK is being included in your JavaScript source paths.

#### Step 3

Create a new mesh, set its type to PrimitivePlane, and create a new material for it as well. Set the pipeline to either "Phong Opaque Textured" or "Flat Opaque Textured."

#### Step 4

Add the zesty-banner component to your mesh's object and fill in the following fields as such:

**creator**\
`0x0000000000000000000000000000000000000000`

**space**\
`0`

**format**\
`tall`

**style**\
`standard`

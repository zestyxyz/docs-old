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

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, null, true);
scene.add(zestyBanner);
```

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

To opt into enabling a beacon on your space, copy and paste:

```
<ZestyBanner space={'0'} creator={'0x0000000000000000000000000000000000000000'} format={'tall'} style={'standard'} beacon={true} position={[0, 2, 0]} />
```

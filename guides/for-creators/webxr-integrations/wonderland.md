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

To opt into enabling a beacon on your space, simply check the "beacon" box on the zesty-banner component.

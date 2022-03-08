# Cryptovoxels Integration

Repository: https://github.com/zestymarket/sdk/tree/main/cryptovoxels

## Before You Integrate

You will first need to create a Space NFT in order to get started checkout "For Creators" for more instructions.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

## Instructions

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

[https://github.com/zestymarket/sdk/blob/main/cryptovoxels/integration.js](https://raw.githubusercontent.com/zestymarket/sdk/main/cryptovoxels/integration.js)

**Step 7**

At the end of the script, copy this line to call the loadBanner function (modify according to your own space information):

```
loadBanner('0', '0x0000000000000000000000000000000000000000', 'polygon', 'tall', 'standard');
```

Replace `0` and  `0x0000000000000000000000000000000000000000` with your space number and wallet address

To opt into enabling a beacon on your space, copy and paste:

```
loadBanner('0', '0x0000000000000000000000000000000000000000', 'polygon', 'tall', 'standard', true)
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
*optional - defaults to `standard`*

String: Style of your placeholder image, which notifies viewers that the ad space is available

**height**
*optional - defaults to `1`*

Integer: Scale the banner to your liking.

**beacon**
*optional*

Boolean: Setting beacon to `true` allows you to view analytics on your space page


**Source**:

```
async function loadBanner(space, creator, network, format, style, beacon = false)
```
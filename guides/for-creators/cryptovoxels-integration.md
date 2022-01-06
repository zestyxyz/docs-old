# Cryptovoxels Integration

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

To opt into enabling a beacon on your space, copy and paste:

```
loadBanner('0', '0x0000000000000000000000000000000000000000', 'polygon', 'tall', 'standard', true)
```

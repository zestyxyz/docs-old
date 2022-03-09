# Muse Integration

## Before You Integrate

You will first need to create a Space NFT in order to get started. Check out "For Creators" for more instructions.

{% content-ref url="../create-space.md" %}
[create-space.md](../create-space.md)
{% endcontent-ref %}

## Instructions

**Step 1**

Log in to Muse and enter builder mode on one of your spaces.

**Step 2**

Press Tab to open the build menu, then click "Add". This shows you the different components you can add to your Muse scene.

**Step 3**

Click "Specify" and then paste in this identifier that corresponds to the Zesty Banner:

```
c1d1fb2d-bcb1-46a9-97c9-f0ba1bd3d81f
```

Click "Add" and you should then see a large black square appear in front of you. This is the banner, which now needs to be configured with the proper settings.

**Step 4**

Select the banner, then fill out the following fields to line up with your space on the Zesty marketplace. Currently you will need to type these fields out manually and in all lowercase, but in the future these will be replaced by dropdown fields. The fields are:

* Network: The network to connect to. Should be either `polygon` or `rinkeby`.
* Space: Your space ID on the marketplace. Should be a number.
* Format: The shape of your banner. Should be `tall`, `wide`, or `square`.
* Style: The style of your default banner when no campaign is currently running on it. Should be `standard`, `minimal`, or `transparent`.
* Beacon: Whether beacon analytics are turned on or off.

**Step 5**

Once you have all the options configured, your banner should now be appearing correctly! With that, you've successfully integrated a Zesty Banner into your Muse space. If you'd like to add another banner to the same scene, you can either repeat the process in Step 3 to spawn another, or you can duplicate your existing banner and adjust its settings/properties elsewhere.

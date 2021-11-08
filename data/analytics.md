---
description: >-
  In this doc we'll outline how we structured our data so it's easy for you
  integrate with us.
---

# Analytics

We take special care to ensure that unlike large tech companies, no personally identifiable information is recorded in our analytics.

Below are the data fields that we collect from our SDK:

**\_id**

The unique ID of the request, which becomes the instance's ID in IPFS.

**creator**

This is the wallet address of the creator the ad will be paying out to.

**adSpace**

The unique identifier for the NFT owned by the creator and listed/sold on the Zesty Market.

**uri**

The link (also on IPFS) which contains the details for the ad that were provided by the advertiser, such as the image to display and the CTA link that the ad should link out to.

**event**

The type of interaction the user has had with the ad slot, currently it's one of `click` or `view`.

**durationInMs**

If the `event` was a `click`, then this value is 0. If the `event` was a `view`, then this value is the number of milliseconds that the ad was viewed for in the experience at a particular instance in time.

**sessionId**

Our unique identifier for every time a user reloads the page.

**timestampInMs**

The Unix timestamp in ms.

**sdkType**

Helps to identify which SDK is sending the metrics.

**sdkVersion**

Helps to identify which version of the SDK is being used.

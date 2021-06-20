---
description: ZestyMarket V1.1 with no validation
---

# ZestyMarket\_ERC20\_V1\_1

## Introduction 

Zesty Market V1 follows the following flow. 

**Phase 0: Setup**

1.  Buyers would create campaigns for their advertising slots. These campaigns cannot be edited and can only be created. The campaigns cannot be edited so as to ensure that a malicious buyer would not be able to change the uri \(which is an ipfs hash\) once a seller has agreed to advertise the campaign. 
2. Sellers would deposit ZestyNFTs and set whether they would require approvals. After depositing the ZestyNFT, sellers would be able to create auctions. 

**Phase 1: Auction**

1. When the auctions are created buyers can bid on the auctions. The auctions are Dutch Auctions with a linearly decaying price. If the seller enabled auto approvals it would proceed directly to Phase 2: Contract section.
2. If auto approvals are disabled the seller would need to either approve or reject the ad slot. If the ad slot is approved Phase 2: Contact section would proceed, otherwise, the auction continues.

**Phase 2: Contract**

1. Zesty Market ****V1 contract only allows withdrawals. When the contract is over, the seller will be able to withdraw locked funds in the contract.




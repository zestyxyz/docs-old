# ZestyMarket\_ERC20\_V2

## Introduction

The logic of ZestyMarket V2 follows the V1 contract similarly, refer to the V1 contracts documentation for the specification. This section will describe additional changes that are not already documented on the V1 contracts documentation. The key difference is in Phase 2: Contract. V2 contracts use Shamir's Secret Sharing as a way of validating advertising delivery. The validator system will be treated as a Proof of Authority system initially, and we'll relax constraints on the trustworthiness of validators. A future edition of the contract will look into decentralizing the validation system. The process is as such.

**Phase 2: Contract**

1. Once the contract starts, a validator node would act as dealer and set the hashlock \(hash of the secret\) for the particular contract and declare the total number of shares of the secret to be distributed. The shares would then be distributed to random validators within the validator network. The minimum threshold to uncover the original secret is 75% of secret shares.  
2. Validator nodes would randomly check whether the advertisement is delivered on the location which the seller has defined. The location would be described in the URI section of the NFT, this could be a URI or machine readable instructions to access a location within a game world.   If the validator notes that the advertisement slot has be delivered, the validator would then publish the secret share on the smart contract. Otherwise, the secret share would be deleted. 
3. If at least 75% of the secret shares are known, the seller can reconstruct the original secret to unlock the hashlock which would unlock funds in the contract. Otherwise, after the contract expires \(+ an additional 2 days grace period for seller to withdraw funds\) the buyer would be refunded. As the advertisement has not be delivered in a satisfactory manner.






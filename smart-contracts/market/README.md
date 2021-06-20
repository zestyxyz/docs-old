# Market

## Introduction

The core contract that is used on Zesty Market are the market contracts for decentralized advertising market. V1 does not include validation of advertising slots, buyers have to trust sellers to not be malicious. Validation was not included to reduce the complexity of the system and is our minimal viable contract.

V2 will eventually include validation of the advertising slots, this will be done through a set of Proof of Authority \(POA\) validators on the system. Progressive decentralization will be introduced once the POA validation is stabilized.

Both market contracts are designed to accept ERC20 tokens. The key ERC20 token Zesty Market will be using is USDC. More ERC20 tokens will be supported depending on demand.

The contracts consists of two sections: **Auction** and and **Contract** \(referring to the fulfillment of the contract\). For V1 and V2 the **Auction** section is Dutch Auction. V1 and V2 differs mainly in the **Contract** section.


# User Story

User Navigates to CommunityAction page and enters the token contract address for the NFT collection he would like to create an intance for. If this collection does not already have a CA instance, one will be created and the user can create custom settings or default settings.

Once the instance is live, other holders of the respective NFT collection can join the CA instance. 





## User Experience:
When logged in (authenticated with wallet containing respective NFT) the user will see:
    -A dashboard allowing them to 
        -Review transaction history
        -Deposit into the wallet
        -Submit for a withdrawal (specifics based on CA configuration)
    -The balance of the CA wallet 
    -All NFTs possessed by the wallet [^1]

The site will track amount of SOL deposited by the members cumulatively, then divide the amount of each member's contributions to get their percentage of total that belongs to them. As a safegaurd against mass exodus, only 50% of the members total contributions will be available for withdrawal on any given withdrawal window until their contribution % is less than 0.1 SOL which will release the safegaurd. 

```i.e Joe has contributed 1 SOL to the CA wallet which has had 100 SOL total in member contributions. Since the last withdrawal window, the CA wallet has flipped a bunch of NFTs and made money from staking and now has balance of 500 SOL. Since Joe is entitled to 1% of the total, 5 SOL he is elligible to withdraw 2.5 SOL during withdrawal window.```

[^1]: Possible interactions with NFTs include:

        -**Flagging to hold:** which if X% of members flag the NFT it will not be available for sale
        -**Special Purchase:** NFTs held for X days will be available to the user for purchase at the CA wallets purchase price.
        -**Sell Personal NFT:** User can offer an NFT to the wallet for a specific price, thereby getting liquidity from the CA wallet, but maintining partial ownership.
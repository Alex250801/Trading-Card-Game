# Trading Card Blockchain
## Details 
* Smart contract address: [SC](https://github.com/cs-pub-ro/blockchain-protocols-and-distributed-applications/tree/main/assignments/tema-1) .
* Using [Jupyer Notebook](https://jupyter.org/) it was possible to interact with the contract.
* The project has numerous transactions that facilitated accessing and calling various endpoints. 

## Understanding the ideea
I have to interact with a smart contract deployed on the MultiversX blockchain. This SC contains a numbers of NFT's and each one has the those attributes: 
```
{
    "class": , 
    "power": ,
    "rarity": 
}
```
All players must find their assigned nft properties, create a card with the same properties and exchange the created card with one that already exists in the NFT supply, having the same properties.

# Exchanging a/n Card/Nft
1. Get your assigned nft calling (getYourNftCardProperties) endpoint
2. Query SC data and get the NFT nonce(number used once). Function to call (nftSupply).
3. Create a new card having those:

    3.1 Create an NFT collection

    3.2 Add ESDTRoleNFTCreate to the collection

    3.3 Create NFT inside collection after 3.2 gave us the role for that

    3.4 Mint our NFT
4. Exchange the minted NFT with the one we got earlier calling (exchangeNft) endpoint. 
    We are trading with ourselves, so sender address == receiver address.
5.  The last thing here is verification, which will be available once you re-run the scripts again and will be showing in the message:   

`"Congratulations! You already finished the homework!"`
# Challenges faced
At first I ran the "Obtain your assigned nft" part from main.ipynb multiple times and the SC had no time to respond to my initial request, so I was getting multiple errors. That was because I already moved the nonce counter to 10-15 by running it multiple times and I had no initial response for the first one, so my jupyter script couldn't find the transaction hash details that I was asking. (example: I was asking for the second transaction but the current nonce was indexed at 12, due to multiple runs).


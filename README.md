# Flow-NFT-Mint-IPFS-Marketplace

## Creating the contract and minting a token
flow project init

flow project start-emulator

flow project deploy

flow keys generate

flow transactions send --code ./transactions/MintPinataParty.cdc --signer emulator-account

flow scripts execute --code ./scripts/CheckTokenMetadata.cdc

## Creating an app to view NFTs created through this contract

## Creating a marketplace to transfer NFTs to others while also transferring the NFT's underlying assets on IPFS

flow transactions send --code ./transactions/LinkPinnie.cdc

flow transactions send --code ./transactions/MintPinnie.cdc --signer emulator-account

flow scripts execute --code ./scripts/CheckPinnieBalance.cdc

### To make sure to mint some and deposit them into a fresh account for someone else

flow keys generate

flow accounts create --key <NewPublicKey>

flow transactions status <TransactionID>

flow transactions send --code ./transactions/CreateEmptyPinnieVault.cdc --signer second-account

flow transactions send --code ./transactions/LinkPinnie.cdc --signer second-account

flow transactions send --code ./transactions/TransferPinnieToken.cdc --signer emulator-account

flow transactions send --code ./transactions/ListTokenForSale.cdc


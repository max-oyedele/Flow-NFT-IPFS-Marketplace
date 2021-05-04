# Flow-NFT-Mint-IPFS-Marketplace

## Creating the contract and minting a token

flow project start-emulator

flow project deploy

flow keys generate

flow transactions send --code ./transactions/MintPinataParty.cdc --signer emulator-account

flow scripts execute --code ./scripts/CheckTokenMetadata.cdc

## Creating an app to view NFTs created through this contract

## Creating a marketplace to transfer NFTs to others while also transferring the NFT's underlying assets on IPFS

# Instantiating Your Art

The PCOArt system empowers Artists to create both stand-alone works and "collections" of partial common ownership art. There are two creation methods:

1. By _minting_ a new token&#x20;
2. By _wrapping_ an existing NFT
   - This second method provides a method for adding PCOArt's Stewardship mechanisms to an existing ERC-721 or ERC-1155 NFT while maintaining the original metadata. This feature not yet enabled through the app, but the beta contract functionality is available for use as-is without any representations of its efficacy or security. 

## Metadata

PCOArt utilizes the [ERC-721 standard](https://ethereum.org/en/developers/docs/standards/tokens/erc-721/) as the foundation of its smart contract system.

It's a flexible, widely-supported, and battle-tested method for digitally representing unique objects, like art, on Ethereum-based blockchains.

Artists ultimately have unlimited configurability to define the attributes of work within their PCOArt tokens, but industry-standard fields integrated into the PCOArt app include the following: &#x20;

**Collection Data (ERC-721 Standard)**

- Collection Name (even if just 1 token)
- Collection Symbol
- URI (allows for further arbitrary metadata definition)

**URI Metadata (Commonly Supported)**

- Name (Note: this is for an individual token, not the collection)
- Description
- External Link
- Image
- Properties
  - [Legal License](legal-license) (PCOArt specific)

[Additional Reference](https://docs.opensea.io/docs/metadata-standards)

:::info
**Metadata Upload Instructions**

Individual token metadata is commonly implemented with a simple JSON schema and embedded folder structure. The recommended process for uploading your token metadata and creating a token (collection) through the PCOArt app is as follows:

1. Download & unzip our [sample metadata folder template](https://nftstorage.link/ipfs/bafybeidxfej5cokgom5ticchwgdwge3sibxdk73ua7s3tlmrxcydhhktjy?filename=metadata.zip)
2. Add all of your art's media files to the `assets` folder (and remove the sample file)
   - Number the files `0`, `1`, `2`, `3`... N (also include the appropriate file extension--.jpeg, .png, etc) according to the desired order of tokens in the collection
3. Upload the `assets` folder to the IPFS storage provider of your choice
   - [Pinata](https://pinata.cloud/) offers a free account with generous limits. You also might consider a paid account with Pinata or an alternative provider with single-payment perpetual storage like [NFT.Storage](https://nft.storage/) or [Lighthouse](https://www.lighthouse.storage/) to ensure your NFT Media never disappears.
4. Copy the IPFS CID of the folder you just uploaded
   - It should start with `Qm` or `baf` depending on the CID format version used
5. Open the `0` file from the template `metadata` folder with a text editor
   - Update each metadata field for the first token you want to mint in your collection
   - Tthe `image` file path should be constructed as follows:
     - Start with `ipfs://`
     - Then paste the IPFS CID of the `assets` folder (copied in step 4)
     - Add a `/` and the appropriate file name with file type extension (e.g. `/0.png`)
     - Result: `ipfs://bafybeidxfej5cokgom5ticchwgdwge3sibxdk73ua7s3tlmrxcydhhktjy/0.png`
6. Save and close the `0` file
7. Make a copy of the `0` file in the `metadata` folder for each token you wish to create
8. Update the file name of each copy so they are numbered sequentially to match your media files (`1`, `2`, `3`,... N)
   - **Important:** Do not add a file extension to these files
9.  Update and save the metadata file for each token as appropriate—-including the `image` path (e.g. `/0.jpeg` to `/1.jpeg`)
10. Upload the entire template folder (i.e. the folder that contains both the `image` & `metadata` folders) to your storage provider
11. Copy the IPFS CID of the folder you just uploaded & add it to the `URI (Metadata)` with a leading `ipfs://` identifier (i.e. `ipfs://QmVL...`)
    :::

## Minting Timing

The PCOArt system allows the Artist to defer the minting of tokens in their collection until the end of their first Auction Pitch. All of the art and metadata are still defined during the creation process, but the on-chain representation of the asset won't be created initially.&#x20;

This can save the Artist gas costs if there's an especially big collection. As PCOArt is initially targeted for support on Ethereum L2s, gas costs shouldn't be prohibitive regardless.&#x20;

If the Artist wishes to launch their PCOArt with an offline auction or by granting Stewardship directly to a 3rd-party, they should select the option to mint the tokens at creation. This will allow them to transfer the NFT to a new address before the first auction (i.e. assign Stewardship without an auction).

# Steward License

## IStewardLicense

### triggerTransfer

```solidity
function triggerTransfer(address from, address to, uint256 tokenId) external
```

Trigger transfer of license

### exists

```solidity
function exists(uint256 tokenId) external view returns (bool)
```

Check if token exists

### maxTokenCount

```solidity
function maxTokenCount() external view returns (uint256)
```

Get max token count

## StewardLicenseBase

### triggerTransfer

```solidity
function triggerTransfer(address from, address to, uint256 tokenId) external
```

Trigger transfer of license

### mintToken

```solidity
function mintToken(address to, uint256 tokenId) external
```

Initial bidder can mint token if it doesn't exist

### addTokenToCollection

```solidity
function addTokenToCollection(address to, string tokenURI, uint256 tokenInitialPeriodStartTime) external
```

Add token to collection

### addTokensToCollection

```solidity
function addTokensToCollection(address[] to, string[] tokenURIs, uint256[] tokenInitialPeriodStartTimes) external
```

Add tokens to collection with to

### addTokensToCollection

```solidity
function addTokensToCollection(string[] tokenURIs, uint256[] tokenInitialPeriodStartTimes, bool shouldMint) external
```

Add tokens to collection

### addTokensWithBaseURIToCollection

```solidity
function addTokensWithBaseURIToCollection(uint32 amount, uint256 initialPeriodStartTime, uint256 initialPeriodStartTimeOffset, string baseURI, bool shouldMint) external
```

Add tokens to collection with baseURI

### maxTokenCount

```solidity
function maxTokenCount() external view returns (uint256)
```

Get max token count

### exists

```solidity
function exists(uint256 tokenId) external view returns (bool)
```

Check if token exists

## StewardLicenseInternal

### ADD_TOKEN_TO_COLLECTION_ROLE

```solidity
bytes32 ADD_TOKEN_TO_COLLECTION_ROLE
```

### _initializeStewardLicense

```solidity
function _initializeStewardLicense(address minter, address addToCollectionMinter, address initialSteward, uint256 maxTokenCount, bool shouldMint, string name, string symbol, string baseURI) internal
```

Initialize license

### _isInitialized

```solidity
function _isInitialized() internal view returns (bool)
```

Check if initialized

### _minter

```solidity
function _minter() internal view returns (address)
```

Get minter

### _initialSteward

```solidity
function _initialSteward() internal view returns (address)
```

Get initial steward

### _triggerTransfer

```solidity
function _triggerTransfer(address from, address to, uint256 tokenId) internal
```

Trigger transfer

### _maxTokenCount

```solidity
function _maxTokenCount() internal view returns (uint256)
```

Get max token count

### _addTokenToCollection

```solidity
function _addTokenToCollection(address to, string tokenURI, uint256 tokenInitialPeriodStartTime) internal
```

Add token to collection

### _addTokenWithBaseURIToCollection

```solidity
function _addTokenWithBaseURIToCollection(string _baseURI, bool shouldMint, uint256 tokenInitialPeriodStartTime) internal
```

Add token to collection

### _tokenURI

```solidity
function _tokenURI(uint256 tokenId) internal view returns (string)
```

Override token URI

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | token URI |

### _beforeTokenTransfer

```solidity
function _beforeTokenTransfer(address from, address to, uint256 tokenId) internal virtual
```

Disable transfers if during auction period

## StewardLicenseStorage

### Layout

```solidity
struct Layout {
  bool isInitialized;
  address initialSteward;
  address minter;
  uint256 maxTokenCount;
}
```

### layout

```solidity
function layout() internal pure returns (struct StewardLicenseStorage.Layout l)
```

## WrappedStewardLicenseInternal

### _initializeWrappedLicense

```solidity
function _initializeWrappedLicense(address wrappedTokenAddress, uint256 wrappedTokenId) internal
```

Initialize license

### _wrappedTokenAddress

```solidity
function _wrappedTokenAddress() internal view returns (address)
```

Get wrapped token address

### _wrappedTokenId

```solidity
function _wrappedTokenId() internal view returns (uint256)
```

Get wrapped token ID

## WrappedStewardLicenseStorage

### Layout

```solidity
struct Layout {
  address wrappedTokenAddress;
  uint256 wrappedTokenId;
}
```

### layout

```solidity
function layout() internal pure returns (struct WrappedStewardLicenseStorage.Layout l)
```

## NativeStewardLicenseFacet

_ERC-1155 token license for Steward. Transfers are disabled during an auction_

### initializeStewardLicense

```solidity
function initializeStewardLicense(address minter_, address addToCollectionMinter_, address steward_, uint256 maxTokenCount_, bool shouldMint, string name, string symbol, string baseURI) external
```

Initialize license

### minter

```solidity
function minter() external view returns (address)
```

Get minter

## WrappedERC1155StewardLicenseFacet

_ERC-721 token license for Steward that wraps existing ERC-1155. Transfers are disabled during an auction._

### initializeWrappedStewardLicense

```solidity
function initializeWrappedStewardLicense(address tokenAddress, uint256 tokenId, address minter_, address addToCollectionMinter_, address steward_, uint256 maxTokenCount_, bool shouldMint, string name, string symbol, string tokenURI) external
```

Initialize license

### minter

```solidity
function minter() external view returns (address)
```

Get minter

### onERC1155Received

```solidity
function onERC1155Received(address, address, uint256 id, uint256 value, bytes) external view returns (bytes4)
```

### onERC1155BatchReceived

```solidity
function onERC1155BatchReceived(address, address, uint256[] ids, uint256[] values, bytes) external view returns (bytes4)
```

## WrappedERC721StewardLicenseFacet

_ERC-721 token license for Steward that wraps existing ERC-721. Only a particular ERC721 transfer is accepted._

### initializeWrappedStewardLicense

```solidity
function initializeWrappedStewardLicense(address tokenAddress, uint256 tokenId, address minter_, address addToCollectionMinter_, address steward_, uint256 maxTokenCount_, bool shouldMint, string name, string symbol, string tokenURI) external
```

Initialize license

### minter

```solidity
function minter() external view returns (address)
```

Get minter

### onERC721Received

```solidity
function onERC721Received(address, address, uint256 tokenId, bytes) external view returns (bytes4)
```
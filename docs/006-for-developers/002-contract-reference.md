# Smart Contract Reference

## AccessControlFacet

### DEFAULT_ADMIN_ROLE

```solidity
bytes32 DEFAULT_ADMIN_ROLE
```

### initializeAccessControl

```solidity
function initializeAccessControl(address admin) external
```

Initialize access control with admin

## AllowlistReadableInternal

### _isAllowed

```solidity
function _isAllowed(address _address) internal view returns (bool)
```

Check if address is allowed

### _getAllowlist

```solidity
function _getAllowlist() internal view returns (address[])
```

Get allowlist as array

### _getAllowAny

```solidity
function _getAllowAny() internal view returns (bool)
```

Get allow any

## AllowlistStorage

### Layout

```solidity
struct Layout {
  bool isInitialized;
  bool allowAny;
  struct EnumerableSet.AddressSet allowlist;
}
```

### layout

```solidity
function layout() internal pure returns (struct AllowlistStorage.Layout l)
```

## AllowlistWritableInternal

### _initializeAllowlist

```solidity
function _initializeAllowlist(bool _allowAny, address[] _addresses) internal
```

Initialize allowlist

### _isInitialized

```solidity
function _isInitialized() internal view returns (bool)
```

Check if initialized

### _setAllowAny

```solidity
function _setAllowAny(bool _allowAny) internal
```

Set allow any

### _addToAllowlist

```solidity
function _addToAllowlist(address _address) internal
```

Add to allowlist

### _removeFromAllowlist

```solidity
function _removeFromAllowlist(address _address) internal
```

Remove from allowlist

### _batchAddToAllowlist

```solidity
function _batchAddToAllowlist(address[] _addresses) internal
```

Batch add to allowlist

### _batchRemoveFromAllowlist

```solidity
function _batchRemoveFromAllowlist(address[] _addresses) internal
```

Batch remove from allowlist

## IAllowlistReadable

### isAllowed

```solidity
function isAllowed(address _address) external view returns (bool)
```

Check if address is allowed

## IAllowlistWritable

### setAllowAny

```solidity
function setAllowAny(bool _allowAny) external
```

Set allow any

### addToAllowlist

```solidity
function addToAllowlist(address _address) external
```

Add to allowlist

### removeFromAllowlist

```solidity
function removeFromAllowlist(address _address) external
```

Remove from allowlist

## IAllowlistWritableInternal

### Allowlisted

```solidity
event Allowlisted(address _address)
```

### BatchAllowlisted

```solidity
event BatchAllowlisted(address[] _addresses)
```

### Unallowlisted

```solidity
event Unallowlisted(address _address)
```

### BatchUnallowlisted

```solidity
event BatchUnallowlisted(address[] _addresses)
```

### AllowAnyUpdated

```solidity
event AllowAnyUpdated(bool _allowAny)
```

## AllowlistFacet

_Allows owner to set an allowlist of addresses_

### COMPONENT_ROLE

```solidity
bytes32 COMPONENT_ROLE
```

### initializeAllowlist

```solidity
function initializeAllowlist(bool allowAny, address[] _addresses) external
```

Initialize allowlist

### initializeAllowlist

```solidity
function initializeAllowlist(address _owner, bool allowAny, address[] _addresses) external
```

Initialize allowlist with owner

### isAllowed

```solidity
function isAllowed(address _address) external view returns (bool)
```

Check if address is allowed

### setAllowAny

```solidity
function setAllowAny(bool _allowAny) external
```

Set allow any

### getAllowAny

```solidity
function getAllowAny() external view returns (bool)
```

Get allow any

### getAllowlist

```solidity
function getAllowlist() external view returns (address[])
```

Get allowlist as array

### addToAllowlist

```solidity
function addToAllowlist(address _address) external
```

Add to allowlist

### addToAllowlist

```solidity
function addToAllowlist(address _address, bool _allowAny) external
```

Add to allowlist with allow any

### removeFromAllowlist

```solidity
function removeFromAllowlist(address _address) external
```

Remove from allowlist

### removeFromAllowlist

```solidity
function removeFromAllowlist(address _address, bool _allowAny) external
```

Remove from allowlist with allow any

### batchAddToAllowlist

```solidity
function batchAddToAllowlist(address[] _addresses) external
```

Batch add to allowlist

### batchAddToAllowlist

```solidity
function batchAddToAllowlist(address[] _addresses, bool _allowAny) external
```

Batch add to allowlist with allow any

### batchRemoveFromAllowlist

```solidity
function batchRemoveFromAllowlist(address[] _addresses) external
```

Batch remove from allowlist

### batchRemoveFromAllowlist

```solidity
function batchRemoveFromAllowlist(address[] _addresses, bool _allowAny) external
```

Batch remove from allowlist with allow any

### batchUpdateAllowlist

```solidity
function batchUpdateAllowlist(address[] _removeAddresses, address[] _addAddresses) external
```

Batch update allowlist

### batchUpdateAllowlist

```solidity
function batchUpdateAllowlist(address[] _removeAddresses, address[] _addAddresses, bool _allowAny) external
```

Batch update allowlist with allow any

## AllowlistMock

### Layout

```solidity
struct Layout {
  bool isAllowed;
}
```

### layout

```solidity
function layout() internal pure returns (struct AllowlistMock.Layout l)
```

### isAllowed

```solidity
function isAllowed(address) external view returns (bool)
```

Check if address is allowed

### setIsAllowed

```solidity
function setIsAllowed(bool _isAllowed) external
```

## EnglishPeriodicAuctionInternal

### _initializeAuction

```solidity
function _initializeAuction(address repossessor, address initialBidder, uint256 initialPeriodStartTime, uint256 initialPeriodStartTimeOffset, uint256 startingBid, uint256 auctionLengthSeconds, uint256 minBidIncrement, uint256 bidExtensionWindowLengthSeconds, uint256 bidExtensionSeconds) internal
```

Initialize parameters

### _setAuctionParameters

```solidity
function _setAuctionParameters(address repossessor, uint256 auctionLengthSeconds, uint256 minBidIncrement, uint256 bidExtensionWindowLengthSeconds, uint256 bidExtensionSeconds, uint256 startingBid) internal
```

Set auction parameters

### _isInitialized

```solidity
function _isInitialized() internal view returns (bool)
```

Check if initialized

### _startingBid

```solidity
function _startingBid() internal view returns (uint256)
```

Get starting bid

### _repossessor

```solidity
function _repossessor() internal view returns (address)
```

Get repossessor

### _setRepossessor

```solidity
function _setRepossessor(address repossessor) internal
```

Set repossessor

### _initialPeriodStartTime

```solidity
function _initialPeriodStartTime() internal view returns (uint256)
```

Get initial period start time

### _auctionLengthSeconds

```solidity
function _auctionLengthSeconds() internal view returns (uint256)
```

Get auction length

### _setStartingBid

```solidity
function _setStartingBid(uint256 startingBid) internal
```

Set starting bid

### _setAuctionLengthSeconds

```solidity
function _setAuctionLengthSeconds(uint256 auctionLengthSeconds) internal
```

Set auction length

### _minBidIncrement

```solidity
function _minBidIncrement() internal view returns (uint256)
```

Get minimum bid increment

### _setMinBidIncrement

```solidity
function _setMinBidIncrement(uint256 minBidIncrement) internal
```

Set minimum bid increment

### _bidExtensionWindowLengthSeconds

```solidity
function _bidExtensionWindowLengthSeconds() internal view returns (uint256)
```

Get bid extension window length

### _setBidExtensionWindowLengthSeconds

```solidity
function _setBidExtensionWindowLengthSeconds(uint256 bidExtensionWindowLengthSeconds) internal
```

Set bid extension window length

### _bidExtensionSeconds

```solidity
function _bidExtensionSeconds() internal view returns (uint256)
```

Get bid extension

### _setBidExtensionSeconds

```solidity
function _setBidExtensionSeconds(uint256 bidExtensionSeconds) internal
```

Set bid extension

### _initialBidder

```solidity
function _initialBidder() internal view returns (address)
```

Get initial bidder

### _highestBid

```solidity
function _highestBid(uint256 tokenId, uint256 round) internal view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get highest outstanding bid

### _bidOf

```solidity
function _bidOf(uint256 tokenId, uint256 round, address bidder) internal view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get bid for address

### _isAuctionPeriod

```solidity
function _isAuctionPeriod(uint256 tokenId) internal view returns (bool)
```

Get is auction period

### _isReadyForTransfer

```solidity
function _isReadyForTransfer(uint256 tokenId) internal view returns (bool)
```

Is token ready for transfer

### _currentAuctionRound

```solidity
function _currentAuctionRound(uint256 tokenId) internal view returns (uint256)
```

Get current auction round

### _lockedCollateral

```solidity
function _lockedCollateral(uint256 tokenId, address bidder) internal view returns (uint256)
```

Get locked collateral from all bids

### _availableCollateral

```solidity
function _availableCollateral(address bidder) internal view returns (uint256)
```

Get available collateral

### _placeBid

```solidity
function _placeBid(uint256 tokenId, address bidder, uint256 bidAmount, uint256 collateralAmount) internal
```

Place a bid

### _cancelBid

```solidity
function _cancelBid(uint256 tokenId, uint256 round, address bidder) internal
```

Cancel bid for current round if not highest bidder

### _cancelAllBids

```solidity
function _cancelAllBids(uint256 tokenId, address bidder) internal
```

Cancel bids for all rounds

### _withdrawCollateral

```solidity
function _withdrawCollateral(address bidder) internal
```

Withdraw collateral

### _closeAuction

```solidity
function _closeAuction(uint256 tokenId) internal
```

Close auction and trigger a transfer to the highest bidder

### _auctionStartTime

```solidity
function _auctionStartTime(uint256 tokenId) internal view returns (uint256 auctionStartTime)
```

Get auction start time

### _auctionEndTime

```solidity
function _auctionEndTime(uint256 tokenId) internal view returns (uint256 auctionEndTime)
```

Get auction end time

### _calculateFeeFromBid

```solidity
function _calculateFeeFromBid(uint256 bidAmount) internal view returns (uint256)
```

Calculate fee from bid

### _checkBidAmount

```solidity
function _checkBidAmount(uint256 bidAmount, uint256 feeAmount) internal view returns (bool)
```

Check that fee is within rounding error of bid amount

## EnglishPeriodicAuctionStorage

### Layout

```solidity
struct Layout {
  bool isInitialized;
  address initialBidder;
  uint256 startingBid;
  address repossessor;
  uint256 initialPeriodStartTime;
  uint256 initialPeriodStartTimeOffset;
  uint256 auctionLengthSeconds;
  uint256 minBidIncrement;
  uint256 bidExtensionWindowLengthSeconds;
  uint256 bidExtensionSeconds;
  mapping(uint256 => uint256) tokenInitialPeriodStartTime;
  mapping(uint256 => uint256) lastPeriodEndTime;
  mapping(uint256 => uint256) currentLicensePeriod;
  mapping(uint256 => uint256) currentAuctionRound;
  mapping(uint256 => uint256) currentAuctionLength;
  mapping(uint256 => mapping(uint256 => mapping(address => struct IEnglishPeriodicAuctionInternal.Bid))) bids;
  mapping(uint256 => mapping(uint256 => struct IEnglishPeriodicAuctionInternal.Bid)) highestBids;
  mapping(address => uint256) availableCollateral;
}
```

### layout

```solidity
function layout() internal pure returns (struct EnglishPeriodicAuctionStorage.Layout l)
```

## IEnglishPeriodicAuctionInternal

### Bid

```solidity
struct Bid {
  address bidder;
  uint256 bidAmount;
  uint256 feeAmount;
  uint256 collateralAmount;
}
```

### InitialPeriodStartTimeSet

```solidity
event InitialPeriodStartTimeSet(uint256 initialPeriodStartTime)
```

### RepossessorSet

```solidity
event RepossessorSet(address repossessor)
```

### AuctionLengthSet

```solidity
event AuctionLengthSet(uint256 auctionLengthSeconds)
```

### MinBidIncrementSet

```solidity
event MinBidIncrementSet(uint256 minBidIncrement)
```

### BidExtensionWindowLengthSet

```solidity
event BidExtensionWindowLengthSet(uint256 bidExtensionWindowLengthSeconds)
```

### BidExtensionSet

```solidity
event BidExtensionSet(uint256 bidExtensionSeconds)
```

### StartingBidSet

```solidity
event StartingBidSet(uint256 startingBid)
```

### BidPlaced

```solidity
event BidPlaced(uint256 tokenId, uint256 round, address bidder, uint256 bidAmount)
```

### AuctionClosed

```solidity
event AuctionClosed(uint256 tokenId, uint256 round, address winningBidder, address previousOwner, uint256 bidAmount)
```

## IPeriodicAuctionReadable

### isAuctionPeriod

```solidity
function isAuctionPeriod(uint256 tokenId) external view returns (bool)
```

Get is auction period

### initialPeriodStartTime

```solidity
function initialPeriodStartTime() external view returns (uint256)
```

Get initial period start time

### initialBidder

```solidity
function initialBidder() external view returns (address)
```

Get initial bidder

## IPeriodicAuctionWritable

### setRepossessor

```solidity
function setRepossessor(address _repossessor) external
```

Set repossessor

### setAuctionLengthSeconds

```solidity
function setAuctionLengthSeconds(uint256 _auctionLengthSeconds) external
```

Set auction length

### setMinBidIncrement

```solidity
function setMinBidIncrement(uint256 _minBidIncrement) external
```

Set minimum bid increment

### setBidExtensionWindowLengthSeconds

```solidity
function setBidExtensionWindowLengthSeconds(uint256 _bidExtensionWindowLengthSeconds) external
```

Set bid extension window length

### setBidExtensionSeconds

```solidity
function setBidExtensionSeconds(uint256 _bidExtensionSeconds) external
```

@notice Set bid extension seconds

## EnglishPeriodicAuctionFacet

### COMPONENT_ROLE

```solidity
bytes32 COMPONENT_ROLE
```

### initializeAuction

```solidity
function initializeAuction(address repossessor_, address initialBidder_, uint256 initialPeriodStartTime_, uint256 initialPeriodStartTimeOffset_, uint256 startingBid_, uint256 auctionLengthSeconds_, uint256 minBidIncrement_, uint256 bidExtensionWindowLengthSeconds_, uint256 bidExtensionSeconds_) external
```

Initialize auction parameters

### initializeAuction

```solidity
function initializeAuction(address owner_, address repossessor_, address initialBidder_, uint256 initialPeriodStartTime_, uint256 initialPeriodStartTimeOffset_, uint256 startingBid_, uint256 auctionLengthSeconds_, uint256 minBidIncrement_, uint256 bidExtensionWindowLengthSeconds_, uint256 bidExtensionSeconds_) external
```

Initialize auction parameters with owner

### setAuctionParameters

```solidity
function setAuctionParameters(address repossessor_, uint256 auctionLengthSeconds_, uint256 minBidIncrement_, uint256 bidExtensionWindowLengthSeconds_, uint256 bidExtensionSeconds_, uint256 startingBid_) external
```

Set auction parameters

### startingBid

```solidity
function startingBid() external view returns (uint256)
```

Get starting bid

### isAuctionPeriod

```solidity
function isAuctionPeriod(uint256 tokenId) external view returns (bool)
```

Get is auction period

### initialPeriodStartTime

```solidity
function initialPeriodStartTime() external view returns (uint256)
```

Get initial period start time

### initialBidder

```solidity
function initialBidder() external view returns (address)
```

Get initial bidder

### isReadyForTransfer

```solidity
function isReadyForTransfer(uint256 tokenId) external view returns (bool)
```

Is token ready for transfer

### placeBid

```solidity
function placeBid(uint256 tokenId, uint256 bidAmount) external payable
```

Place a bid

### cancelBid

```solidity
function cancelBid(uint256 tokenId, uint256 round) external
```

Cancel bid for current round

### withdrawCollateral

```solidity
function withdrawCollateral() external
```

Withdraw collateral

### cancelAllBidsAndWithdrawCollateral

```solidity
function cancelAllBidsAndWithdrawCollateral(uint256 tokenId) external
```

Cancel all bids and withdraw collateral

### cancelBidAndWithdrawCollateral

```solidity
function cancelBidAndWithdrawCollateral(uint256 tokenId, uint256 round) external
```

Cancel bid for current round and withdraw collateral

### lockedCollateral

```solidity
function lockedCollateral(uint256 tokenId, address bidder) external view returns (uint256)
```

Get locked collateral from all bids

### availableCollateral

```solidity
function availableCollateral(address bidder) external view returns (uint256)
```

Get available collateral

### closeAuction

```solidity
function closeAuction(uint256 tokenId) external
```

Close auction and trigger a transfer to the highest bidder

### calculateFeeFromBid

```solidity
function calculateFeeFromBid(uint256 bidAmount) external view returns (uint256)
```

Calculate fee from bid

### auctionStartTime

```solidity
function auctionStartTime(uint256 tokenId) external view returns (uint256)
```

Get auction start time

### auctionEndTime

```solidity
function auctionEndTime(uint256 tokenId) external view returns (uint256)
```

Get auction end time

### repossessor

```solidity
function repossessor() external view returns (address)
```

Get repossessor

### setStartingBid

```solidity
function setStartingBid(uint256 startingBid_) external
```

Set starting bid

### setRepossessor

```solidity
function setRepossessor(address repossessor_) external
```

Set repossessor

### auctionLengthSeconds

```solidity
function auctionLengthSeconds() external view returns (uint256)
```

Get auction length

### setAuctionLengthSeconds

```solidity
function setAuctionLengthSeconds(uint256 auctionLengthSeconds_) external
```

Set auction length

### minBidIncrement

```solidity
function minBidIncrement() external view returns (uint256)
```

Get minimum bid increment

### setMinBidIncrement

```solidity
function setMinBidIncrement(uint256 minBidIncrement_) external
```

Set minimum bid increment

### bidExtensionWindowLengthSeconds

```solidity
function bidExtensionWindowLengthSeconds() external view returns (uint256)
```

Get bid extension window length

### setBidExtensionWindowLengthSeconds

```solidity
function setBidExtensionWindowLengthSeconds(uint256 bidExtensionWindowLengthSeconds_) external
```

Set bid extension window length

### bidExtensionSeconds

```solidity
function bidExtensionSeconds() external view returns (uint256)
```

@notice Get bid extension seconds

### setBidExtensionSeconds

```solidity
function setBidExtensionSeconds(uint256 bidExtensionSeconds_) external
```

@notice Set bid extension seconds

### highestBid

```solidity
function highestBid(uint256 tokenId) external view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get highest outstanding bid

### highestBid

```solidity
function highestBid(uint256 tokenId, uint256 round) external view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get highest outstanding bid for a particular round

### bidOf

```solidity
function bidOf(uint256 tokenId, address bidder) external view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get bid for address

### bidOf

```solidity
function bidOf(uint256 tokenId, uint256 round, address bidder) external view returns (struct IEnglishPeriodicAuctionInternal.Bid)
```

Get bid for address for particular round

### currentAuctionRound

```solidity
function currentAuctionRound(uint256 tokenId) external view returns (uint256)
```

Get current auction round

## PeriodicAuctionMock

### Layout

```solidity
struct Layout {
  bool isAuctionPeriod;
  bool shouldFail;
  uint256 initialPeriodStartTime;
  address initialBidder;
}
```

### layout

```solidity
function layout() internal pure returns (struct PeriodicAuctionMock.Layout l)
```

### isAuctionPeriod

```solidity
function isAuctionPeriod(uint256) external view returns (bool)
```

### setIsAuctionPeriod

```solidity
function setIsAuctionPeriod(bool _isAuctionPeriod) external
```

### setShouldFail

```solidity
function setShouldFail(bool _shouldFail) external
```

### initialPeriodStartTime

```solidity
function initialPeriodStartTime() external view returns (uint256)
```

Get initial period start time

### setInitialPeriodStartTime

```solidity
function setInitialPeriodStartTime(uint256 _initialPeriodStartTime) external
```

### initialBidder

```solidity
function initialBidder() external view returns (address)
```

Get initial bidder

### setInitialBidder

```solidity
function setInitialBidder(address _initialBidder) external
```

## MockBidder

### auction

```solidity
contract EnglishPeriodicAuctionFacet auction
```

### constructor

```solidity
constructor(contract EnglishPeriodicAuctionFacet _auction) public
```

### withdrawCollateral

```solidity
function withdrawCollateral() external
```

### receive

```solidity
receive() external payable
```

## IBeneficiary

### distribute

```solidity
function distribute() external payable
```

Distribute to beneficiaries

## IDABeneficiaryInternal

### _initializeIDABeneficiary

```solidity
function _initializeIDABeneficiary(contract ISETH _token, struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) internal
```

Initialize beneficiary

### _isInitialized

```solidity
function _isInitialized() internal view returns (bool)
```

Check if initialized

### _setToken

```solidity
function _setToken(contract ISETH _token) internal
```

Set token

### _updateBeneficiaryUnits

```solidity
function _updateBeneficiaryUnits(struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) internal
```

Update beneficiary units

### _distribute

```solidity
function _distribute(uint256 value) internal
```

Distribute to beneficiaries

## IDABeneficiaryStorage

### Layout

```solidity
struct Layout {
  bool isInitialized;
  contract ISETH token;
}
```

### layout

```solidity
function layout() internal pure returns (struct IDABeneficiaryStorage.Layout l)
```

## IIDABeneficiary

### updateBeneficiaryUnits

```solidity
function updateBeneficiaryUnits(struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) external
```

Update beneficiary units

## IIDABeneficiaryInternal

### Beneficiary

```solidity
struct Beneficiary {
  address subscriber;
  uint128 units;
}
```

### TokenSet

```solidity
event TokenSet(address token)
```

### BeneficiaryUnitsUpdated

```solidity
event BeneficiaryUnitsUpdated(address subscriber, uint128 units)
```

### Distributed

```solidity
event Distributed(uint256 amount)
```

## BeneficiaryMock

### initializeMockBeneficiary

```solidity
function initializeMockBeneficiary(address _owner) external
```

Initialize beneficiary

### distribute

```solidity
function distribute() external payable
```

Distribute to beneficiaries

## IDABeneficiaryFacet

_Beneficiary implemented using a Superfluid IDA index_

### COMPONENT_ROLE

```solidity
bytes32 COMPONENT_ROLE
```

### initializeIDABeneficiary

```solidity
function initializeIDABeneficiary(contract ISETH _token, struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) external
```

Initialize beneficiary

### initializeIDABeneficiary

```solidity
function initializeIDABeneficiary(address _owner, contract ISETH _token, struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) external
```

Initialize beneficiary

### updateBeneficiaryUnits

```solidity
function updateBeneficiaryUnits(struct IIDABeneficiaryInternal.Beneficiary[] _beneficiaries) external
```

Update beneficiaries

### distribute

```solidity
function distribute() external payable
```

Distribute to beneficiaries

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

## NativeStewardLicenseMock

### mint

```solidity
function mint(address account, uint256 tokenId) external
```

### burn

```solidity
function burn(uint256 tokenId) external
```

### testTriggerTransfer

```solidity
function testTriggerTransfer(address from, address to, uint256 tokenId) external
```

## SolidStateERC1155Mock

### constructor

```solidity
constructor(string tokenURI) public
```

### __mint

```solidity
function __mint(address account, uint256 id, uint256 amount) external
```

## SolidStateERC721Mock

### constructor

```solidity
constructor(string name, string symbol, string baseURI) public
```

### mint

```solidity
function mint(address account, uint256 tokenId) external
```

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

## WrappedERC1155StewardLicenseMock

### mint

```solidity
function mint(address account, uint256 tokenId) external
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

## WrappedERC721StewardLicenseMock

### mint

```solidity
function mint(address account, uint256 tokenId) external
```

## IPeriodicPCOParamsInternal

### LicensePeriodSet

```solidity
event LicensePeriodSet(uint256 licensePeriod)
```

### FeeNumeratorSet

```solidity
event FeeNumeratorSet(uint256 feeNumerator)
```

### FeeDenominatorSet

```solidity
event FeeDenominatorSet(uint256 feeDenominator)
```

## IPeriodicPCOParamsReadable

### licensePeriod

```solidity
function licensePeriod() external view returns (uint256)
```

Get license period

### feeNumerator

```solidity
function feeNumerator() external view returns (uint256)
```

Get fee numerator

### feeDenominator

```solidity
function feeDenominator() external view returns (uint256)
```

Get fee denominator

## IPeriodicPCOParamsWritable

### setLicensePeriod

```solidity
function setLicensePeriod(uint256 _licensePeriod) external
```

Set license period

### setFeeNumerator

```solidity
function setFeeNumerator(uint256 _feeNumerator) external
```

Set fee numerator

### setFeeDenominator

```solidity
function setFeeDenominator(uint256 _feeDenominator) external
```

Set fee denominator

## PeriodicPCOParamsInternal

### _initializeParams

```solidity
function _initializeParams(uint256 licensePeriod, uint256 feeNumerator, uint256 feeDenominator) internal
```

Initialize parameters

### _setPCOParameters

```solidity
function _setPCOParameters(uint256 licensePeriod, uint256 feeNumerator, uint256 feeDenominator) internal
```

Set PCO parameters

### _isInitialized

```solidity
function _isInitialized() internal view returns (bool)
```

Check if initialized

### _licensePeriod

```solidity
function _licensePeriod() internal view returns (uint256)
```

Get license period

### _setLicensePeriod

```solidity
function _setLicensePeriod(uint256 licensePeriod) internal
```

Set license period

### _feeNumerator

```solidity
function _feeNumerator() internal view returns (uint256)
```

Get fee numerator

### _setFeeNumerator

```solidity
function _setFeeNumerator(uint256 feeNumerator) internal
```

Set fee numerator

### _feeDenominator

```solidity
function _feeDenominator() internal view returns (uint256)
```

Get fee denominator

### _setFeeDenominator

```solidity
function _setFeeDenominator(uint256 feeDenominator) internal
```

Set fee denominator

## PeriodicPCOParamsStorage

### Layout

```solidity
struct Layout {
  bool isInitialized;
  uint256 licensePeriod;
  uint256 feeNumerator;
  uint256 feeDenominator;
}
```

### layout

```solidity
function layout() internal pure returns (struct PeriodicPCOParamsStorage.Layout l)
```

## PeriodicPCOParamsFacet

_Params store for periodic PCO_

### COMPONENT_ROLE

```solidity
bytes32 COMPONENT_ROLE
```

### initializePCOParams

```solidity
function initializePCOParams(uint256 licensePeriod_, uint256 feeNumerator_, uint256 feeDenominator_) external
```

Initialize params

### initializePCOParams

```solidity
function initializePCOParams(address owner_, uint256 licensePeriod_, uint256 feeNumerator_, uint256 feeDenominator_) external
```

Initialize params with owner

### setPCOParameters

```solidity
function setPCOParameters(uint256 licensePeriod_, uint256 feeNumerator_, uint256 feeDenominator_) external
```

Set PCO parameters

### licensePeriod

```solidity
function licensePeriod() external view returns (uint256)
```

Get license period

### setLicensePeriod

```solidity
function setLicensePeriod(uint256 licensePeriod_) external
```

Set license period

### feeNumerator

```solidity
function feeNumerator() external view returns (uint256)
```

Get fee numerator

### setFeeNumerator

```solidity
function setFeeNumerator(uint256 feeNumerator_) external
```

Set fee numerator

### feeDenominator

```solidity
function feeDenominator() external view returns (uint256)
```

Get fee denominator

### setFeeDenominator

```solidity
function setFeeDenominator(uint256 feeDenominator_) external
```

Set fee denominator

## IDiamond

### FacetInit

```solidity
struct FacetInit {
  address target;
  address initTarget;
  bytes initData;
  bytes4[] selectors;
}
```

## IDiamondFactory

### DiamondCreated

```solidity
event DiamondCreated(address diamondAddress)
```

### createDiamond

```solidity
function createDiamond(struct IDiamond.FacetInit[] facetInits) external returns (address)
```

## OwnableDiamond

### constructor

```solidity
constructor(address owner, struct IDiamond.FacetInit[] facetInits) public
```

### receive

```solidity
receive() external payable
```

### _transferOwnership

```solidity
function _transferOwnership(address account) internal virtual
```

### _getImplementation

```solidity
function _getImplementation() internal view returns (address implementation)
```

query custom fallback address is no implementation is found

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| implementation | address | implementation address |

## OwnableDiamondFactory

### createDiamond

```solidity
function createDiamond(struct IDiamond.FacetInit[] facetInits) external returns (address)
```

## SingleCutDiamond

### constructor

```solidity
constructor(struct IDiamond.FacetInit[] facetInits) public
```

### receive

```solidity
receive() external payable
```

## SingleCutDiamondFactory

### createDiamond

```solidity
function createDiamond(struct IDiamond.FacetInit[] facetInits) external returns (address)
```

## BeaconDiamond

### BeaconDiamond__NoFacetForSignature

```solidity
error BeaconDiamond__NoFacetForSignature()
```

### constructor

```solidity
constructor(contract IDiamondReadable _beacon) public
```

### _getImplementation

```solidity
function _getImplementation() internal view returns (address)
```

get logic implementation address

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | implementation address |

## BeaconDiamondInternal

### _setBeacon

```solidity
function _setBeacon(contract IDiamondReadable beacon) internal
```

## BeaconDiamondStorage

### Layout

```solidity
struct Layout {
  contract IDiamondReadable beacon;
}
```

### layout

```solidity
function layout() internal pure returns (struct BeaconDiamondStorage.Layout l)
```


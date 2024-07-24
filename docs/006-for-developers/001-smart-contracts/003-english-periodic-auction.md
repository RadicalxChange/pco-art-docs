# English Periodic Auction

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
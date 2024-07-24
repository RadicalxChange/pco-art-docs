# Diamonds

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
# Allowlist

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
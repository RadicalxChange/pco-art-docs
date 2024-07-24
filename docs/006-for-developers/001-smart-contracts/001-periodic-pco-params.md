# Periodic PCO Parameters

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
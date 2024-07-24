# Beneficiary

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
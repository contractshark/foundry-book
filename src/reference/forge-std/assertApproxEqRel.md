## `assertApproxEqRel`

### Signature

```solidity
function assertApproxEqRel(uint256 a, uint256 b, uint256 maxPercentDelta) internal virtual;
```

```solidity
function assertApproxEqRel(uint256 a, uint256 b, uint256 maxPercentDelta, string memory err) internal virtual;
```

```solidity
function assertApproxEqRel(int256 a, int256 b, uint256 maxPercentDelta) internal virtual;
```

```solidity
function assertApproxEqRel( int256 a, int256 b, uint256 maxPercentDelta, string memory err) internal virtual;
```

### Description

Asserts `a` is approximately equal to `b` with delta in percentage (An 18 decimal fixed point number, where 1e18 == 100%).

### Examples

```solidity
uint256 a = 100;
uint256 b = 200;
function testFail () external {
    assertApproxEqRel(a, b, 0.4e18);
}
//[PASS] testFail() (gas: 23884)
//Logs:
//  Error: a ~= b not satisfied [uint]
//      Expected: 200
//        Actual: 100
//   Max % Delta: 0.400000000000000000
//       % Delta: 0.500000000000000000
```
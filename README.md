# rari-docs-proposal
proposal for rari capital fuse docs improvement 

# getPoolUsersWithData()
```js
getPoolUsersWithData(address Comptroller, uint256 maxHealth) returns (tuple[], uint256, uint256)
```
`Comptroller`: Pool to parse <br />
`maxHealth`: maximum account health to parse for <br />
`RETURN`: [ [FusePoolUser[]](docs.rari.capital/fuse#FusePoolUser), [closeFactor](docs.rari.capital/fuse#FusePoolUser), [liquidationIncentive](docs.rari.capital/fuse#FusePoolUser) ] <br />
(FYI: return values will link to their definitions in docs. all return values will be documented at the top as they are complex and repeated often in the lens functions)

## Solidity
```js
fusePoolLens lens = fusePoolLens(0xABCD...);

poolUsers usrs = lens.getPoolUsersWithData(0xEFGH..., 101010101010101010);
```
## Web3 1.0
```js	
const lens = new Web3.eth.Contract(FUSE_POOL_LENS_ABI, 0xABCD...);

const usrs = await lens.methods.getPoolUsersWithData(0xEFGH..., 101010101010101010);
```

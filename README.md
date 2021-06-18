# rari-docs-proposal
Example documentation for a fuse pool lens function

### getPoolUsersWithData()
Gets users and their data in a fuse pool under a given account [health](docs.rari.capital/fuse#FusePoolUser) 
#### fERC20 / FEther
```js
getPoolUsersWithData(address Comptroller, uint256 maxHealth) returns (tuple[], uint256, uint256)
```
- `Comptroller`: Pool to parse <br />
- `maxHealth`: Maximum account health to parse for <br />
- `RETURN`: [ [FusePoolUser[]](docs.rari.capital/fuse#FusePoolUser), [closeFactor](docs.rari.capital/fuse#FusePoolUser), [liquidationIncentive](docs.rari.capital/fuse#FusePoolUser) ] <br />
`(FYI: return values will link to their definitions in docs. All return values will be documented at the top as some are complex and many are repeated often in the functions)`

#### Solidity
```js
fusePoolLens lens = fusePoolLens(0xABCD...);

poolUsers usrs = lens.getPoolUsersWithData(0xEFGH..., 101010101010101010);
```
#### Web3 1.0
```js	
const lens = new Web3.eth.Contract(FUSE_POOL_LENS_ABI, 0xABCD...);

const usrs = await lens.methods.getPoolUsersWithData(0xEFGH..., 101010101010101010);
```
[(Example of currrent documentation for fuse from the rari docs)](Screen%20Shot%202021-06-17%20at%205.43.53%20PM.png)

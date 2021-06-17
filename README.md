# rari-docs-proposal
proposal for rari capital fuse docs improvement 

# getPoolUsersWithData()
```js
	getPoolUsersWithData(address Comptroller, uint256 maxHealth) returns (tuple[], uint256, uint256)
```
`Comptroller`: Pool to parse
`maxHealth`: maximum account health to parse for
`RETURN`: [ FusePoolUser[](docs.rari.capital/fuse#FusePoolUser), closeFactor, liquidationIncentive ]
(return values will link to their definitions in docs. all parameters and return values will be documented at the top)

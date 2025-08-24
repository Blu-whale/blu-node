## BluWhale node

### requirements
- docker
- docker-compose
- git
- evm private key

### setup
```bash
git clone https://github.com/Blu-whale/blu-node.git
cd blu-node
vim conf/config.yaml # set your evm private key
docker-compose up -d
```


### config file explanation
```yaml
app:
  contractAddress: '0x3fbb4dfa4cb8b26478d27fd89f59e8d91a39a7e6'   # heartbeat contract address
  privateKey: ''                                                  # your evm private key
  rpcUrl: 'https://oceanum-testnet.rpc.caldera.xyz/http'          # rpc url of bluWhale chain
  dataPath: './data'                                              # path to store data
  ipfsGateway: 'https://prod-common-api.bluwhale.com'             # ipfs gateway url(eg:https://ipfs.io), https://prod-common-api.bluwhale.com is recommended,faster than ipfs.io

logger:
  level: info
  maxFiles: 31
  enableConsole: true

```

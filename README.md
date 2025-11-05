## BluWhale node

### Hardware requirements
- CPU: Dual-core processor or higher
- RAM: 2GB or more
- Storage: At least 10GB free space
- Internet: Stable connection (5Mbps+ upload/download)
- OS: Windows 10+, macOS 11+, or Linux (Ubuntu 20.04+)
- Note: Higher specs may improve node performance and reward stability.

### Environment requirements
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
  privateKey: '' # your evm private key
  rpc: 'https://prod-common-api.bluwhale.com/node/api/heartbeat'

logger:
  level: "info"
  encoderType: "console"
  outputType: "all"
  maxAge: 30
  enableColor: true

```

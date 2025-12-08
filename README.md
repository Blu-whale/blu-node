# BluWhale node

## Node Operation Options
### Option 1: Stake to Run
* Operators need to stake the specified amount of (ve)BLUAI tokens to run the nodes.
* Staking Requirements:
    * Master Node: 5,000 (ve)BLUAI
    * Common Node: 500 (ve)BLUAI

#### Hardware Requirements
- CPU: Quad-core processor or higher (recommended 2.0GHz+ clock speed)
- RAM: 4GB or more
- Storage: At least 20GB free space (SSD recommended for faster data read/write)
- Internet: Stable high-speed connection (10Mbps+ upload/download speed)
- OS: Windows 10+, macOS 11+, or Linux (Ubuntu 20.04+)

#### Environment Requirements
- docker
- docker-compose
- git
- evm private key

#### Setup
```bash
git clone https://github.com/Blu-whale/blu-node.git
cd blu-node
vim conf/config.yaml # set your evm private key
docker-compose up -d
```


#### Config File
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
      

### Option 2: Run nodes on Chain (Coming Soon)
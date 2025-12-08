## BluWhale node

### Gas Fee Estimation
1. Transaction Frequency: Heartbeat transactions are sent at a fixed interval of 10 seconds per transaction.

2. Per-Transaction Gas Fee Standard: Each heartbeat transaction consumes 2-3 BLUAI as gas fee. The exact amount fluctuates based on on-chain congestion and transaction byte size; it is recommended to use 2.5 BLUAI per transaction as the benchmark for calculation.

3. Periodic Fee Estimation (calculated at the benchmark of 2.5 BLUAI per transaction):
  * Hourly: 360 transactions × 2.5 BLUAI/transaction = 900 BLUAI 
  * Daily: 8,640 transactions × 2.5 BLUAI/transaction = 21,600 BLUAI
  * Monthly (based on 30 days): 259,200 transactions × 2.5 BLUAI/transaction = 648,000 BLUAI

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

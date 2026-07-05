# BluWhale node

## Node Operation Options
### Run On Chain 
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
  contractAddress: '0xc66D32df5e3C7C692393E12e17CF66Eea9848e73'
  privateKey: '' # your evm private key
  rpc: 'https://rpc.bout.network'
  DataPath: './data/db/node.sqlite'
  heartbeatBatchSize: 100

logger:
  level: "debug"
  encoderType: "console"
  outputType: "all"
  maxAge: 30
  enableColor: true

```

#### Gas Fee Estimation
1. Transaction Frequency: Heartbeat transactions are sent at a fixed interval of 10 seconds per transaction.

2. Per-Transaction Gas Fee Standard: Each heartbeat transaction consumes 2-3 BLUAI as gas fee. The exact amount fluctuates based on on-chain congestion and transaction byte size; it is recommended to use 2.5 BLUAI per transaction as the benchmark for calculation.

3. Periodic Fee Estimation (calculated at the benchmark of 2.5 BLUAI per transaction):
* Hourly: 360 transactions × 2.5 BLUAI/transaction = 900 BLUAI
* Daily: 8,640 transactions × 2.5 BLUAI/transaction = 21,600 BLUAI
* Monthly (based on 30 days): 259,200 transactions × 2.5 BLUAI/transaction = 648,000 BLUAI

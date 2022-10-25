## init
`./geth --datadir data init genesis.json`
- 文件依赖：
	- genesis.json

## run
```bash
./geth --config config.toml --datadir ./data --networkid 820014 --rpc --rpcapi eth,net,web3,miner,txpool --rpcaddr 0.0.0.0 --rpcport 8545 --port 30303
```
- 文件依赖：
	- config.toml
    - trustconfig.json

## debug
```bash
cd trust-bsc/cmd/geth
dlv debug . -- --config /Users/k/bsc_test/config.toml --datadir /Users/k/bsc_test/data --networkid 820014 --rpc --rpcapi eth,net,web3,miner,txpool --rpcaddr 0.0.0.0 --rpcport 8545 --port 30303
```
- 依赖：
	- dlv
    ```bash 
    go install github.com/go-delve/delve/cmd/dlv@latest
    export PATH="~/go/bin:$PATH"
    ```
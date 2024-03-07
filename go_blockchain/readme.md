# A complete Blockchain developed with Golang <3

# Run
`go run blockchain.go`

# help full commands
`go mod init go_blockchain`

## fomart code
`gofmt -w block/blockchain.go`

### run servers
`cd to directory you want to run`
`go run main.go blockchain_server.go -port 5001`
`go run main.go wallet_server.go`

### Endpoints and node servers
- Wallet http://0.0.0.0:8080/
- Blockchain transactions http://0.0.0.0:5000/transactions
- Blockchain chain http://0.0.0.0:5000/chain
- Blockchain mining http://0.0.0.0:5000/mine/start
- Wallet total amount http://0.0.0.0:5000/amount?blockchain_address=1NVNQbFvy1dJBegPJzJKK3ZvLQfrcL5GyJ

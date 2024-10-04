# MoneyMonkey Chain

### Instruction

```bash

# 0. Make a binary directory
mkdir bin

# 1. build Moneymonkeyappd
# go build -output <path> <optional flags> <app-name>
go build -o bin/moneymonkeyappd ./moneymonkeyappd # without version flag
go build -o bin/moneymonkeyappd -ldflags '-X github.com/cosmos/cosmos-sdk/version.Version=v1.0.0' ./moneymonkeyappd # with version flag

# 2. Check your binary
# ./bin/<app-name>
./bin/moneymonkeyappd version

# >>> v1.0.0

# init moneymonkey chain
./scripts/init.sh

# start moneymonkey chain
./scripts/start.sh
```

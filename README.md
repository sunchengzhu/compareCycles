# compareCycles
## Usage

1. retrieve the 'block_verifier' logs from `ckb replay`

```shell
nohup sudo ./ckb replay --tmp-target ../tmp/replay --profile 1 12960000 | grep block_verifier > replay-116.1.log 2>&1 &
nohup sudo ./ckb replay --tmp-target ../tmp/replay --profile 1 12960000 | grep block_verifier > replay-spwan.log 2>&1 &
```

2. compare two log files

```shell
node compareLogs.js replay-116.1.log replay-spwan.log
```

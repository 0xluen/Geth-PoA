boot:
bootnode -nodekey "./core.key" -verbosity 7 -addr "127.0.0.1:30301"

node-1:
geth --networkid 14333 --datadir "./data" --bootnodes enode://a33ad86c390de4309cd68b34fc33a78d322872d18b2280e919899f25c7df4b80bd92fb4e19173d5459fa4f5bc12e3ee3ff3cb4586963c997a3cc3c3eaeb74c45@127.0.0.1:0?discport=30301 --port 30303 --ipcdisable --syncmode 'full' --http --allow-insecure-unlock --http.corsdomain “*” --http.port 8546 --authrpc.port 8552 --unlock 0x7baE258F2be4A4b76a2e4283d8d97DF014e3A934 --password pass.txt --mine console --miner.etherbase 0x7baE258F2be4A4b76a2e4283d8d97DF014e3A934

node-2:
geth --networkid 14333 --datadir "./data" --bootnodes enode://a33ad86c390de4309cd68b34fc33a78d322872d18b2280e919899f25c7df4b80bd92fb4e19173d5459fa4f5bc12e3ee3ff3cb4586963c997a3cc3c3eaeb74c45@127.0.0.1:0?discport=30301 --port 30304 --ipcdisable --syncmode 'full' --http --allow-insecure-unlock --http.corsdomain “*” --http.port 8547  --authrpc.port 8553 --unlock 0x3Cd63f4f8AfD4fDdC8c2dE99eF1F23096f33Ff8E --password pass.txt --mine console --miner.etherbase 0x3Cd63f4f8AfD4fDdC8c2dE99eF1F23096f33Ff8E

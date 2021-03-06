## Chain

GenTx

```bash
BINARY gentx polkachu AMOUNT \
 --chain-id CHAIN_ID \
 --moniker 'polkachu.com' \
 --website "https://polkachu.com" \
 --identity "0A6AF02D1557E5B4" \
 --details "Polkachu is the trusted staking service provider for blockchain projects. 100% refund for downtime slash. Contact us at hello@polkachu.com" \
 --security-contact="hello@polkachu.com"
 --commission-max-change-rate=0.05 \
 --commission-max-rate=0.10 \
 --commission-rate=0.01
```

Create validator

```bash
BINARY tx staking create-validator \
 --amount AMOUNT \
 --commission-max-change-rate "0.05" \
 --commission-max-rate "0.10" \
 --commission-rate "0.01" \
 --min-self-delegation "1" \
 --pubkey=$(BINARY tendermint show-validator) \
 --moniker ' polkachu.com' \
 --website "https://polkachu.com" \
 --identity "0A6AF02D1557E5B4" \
 --details "Polkachu is the trusted staking service provider for blockchain projects. 100% refund for downtime slash. Contact us at hello@polkachu.com" \
 --security-contact="hello@polkachu.com"
 --chain-id CHAIN_ID \
 --SOME-EXTRA \
 --from polkachu
```

```bash
chaind tx staking create-validator --yes \
 --amount 1000000000000tkyve \
 --pubkey=$(chaind tendermint show-validator) \
 --chain-id korellia \
 --from kyve_test \
 --commission-max-change-rate "0.05" \
 --commission-max-rate "0.20" \
 --commission-rate "0.10" \
 --min-self-delegation "1" \
 --moniker 'polkachu.com' \
 --website "https://polkachu.com" \
 --identity "0A6AF02D1557E5B4" \
 --details "Polkachu is the trusted staking service provider for blockchain projects. 100% refund for downtime slash. Contact us at hello@polkachu.com" \
 --security-contact="hello@polkachu.com" \
--gas auto \
--gas-adjustment 1.5 \
--gas-prices 0.001udws \
--broadcast-mode block
```

```bash
chaind tx staking delegate kyvevaloper1jt9w26mpxxjsk63mvd4m2ynj0af09cslxlnsvh 1350000000000tkyve \
--from kyve_test
```

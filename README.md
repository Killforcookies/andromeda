# andromeda
wget -q -O andromeda.sh https://api.nodes.guru/andromeda.sh && chmod +x andromeda.sh && /bin/bash andromeda.sh
source $HOME/.bash_profile
andromedad tx staking create-validator \
--moniker="$VALIDATOR" \
--amount=1000000uandr \
--fees 300uandr \
--pubkey=$(andromedad tendermint show-validator) \
--chain-id=$CHAIN_ID \
--commission-max-change-rate=0.01 \
--commission-max-rate=0.20 \
--commission-rate=0.10 \
--min-self-delegation=1 \
--from=wallet \
--yes 

# StarkNet - Setup Guide
StarkNet is a permissionless decentralized Validity-Rollup (often referred to as ZK-Rollup). It operates as an L2 network over Ethereum, enabling any dApp to achieve unlimited scale for its computation – without compromising Ethereum's composability and security.


### To run starknet we will use the nodes provided by the Alchemy service, so register at Alchemy and create endpoints in your personal account.
ref: https://alchemy.com/?r=33beda56a64e44bf

![png1](https://github.com/0xfunda/starknet/blob/main/1.png)
![png2](https://github.com/0xfunda/starknet/blob/main/2.png)
![png3](https://github.com/0xfunda/starknet/blob/main/3.png)
![png4](https://github.com/0xfunda/starknet/blob/main/4.png)
![png5](https://github.com/0xfunda/starknet/blob/main/5.png)

### Copy the address and go to step Installing

Replace YOUR_ALCHEMY_HTTP_ADDRESS with your alchemy address.

ALCHEMY=YOUR_ALCHEMY_HTTP_ADDRESS
echo 'export ALCHEMY='$ALCHEMY >> $HOME/.bash_profile

Example, do not copy!
ALCHEMY=https://eth-goerli.alchemyapi.io/v2/Ey8Guru7zpg3EfUcLm8iR4FTxPAvqMS
echo 'export ALCHEMY='$ALCHEMY >> $HOME/.bash_profile

![Screenshot_4](https://user-images.githubusercontent.com/76862881/203631948-4454925b-4a31-4497-9596-7fe0c9d2d8e9.png)

Node guru script for a quick installation:

wget -O starknet.sh https://api.nodes.guru/starknet.sh && chmod +x starknet.sh && ./starknet.sh


Check the status of the node

service starknetd status

Check logs this code :
journalctl -u starknetd -f 

restart Node :
systemctl restart starknetd

Delete node:
systemctl stop starknetd
systemctl disable starknetd
rm -rf ~/pathfinder/
rm -rf /etc/systemd/system/starknetd.service
rm -rf /usr/local/bin/pathfinder











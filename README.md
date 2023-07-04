### Hi there 👋

<!--
**kimisha1/kimisha1** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
git clone https://github.com/AleoHQ/snarkOS.git --depth 1
cd snarkOS
sudo apt update && sudo apt upgrade -y

sudo apt install screen

screen -S sui

wget -O sui_testnet.sh https://api.nodes.guru/sui_testnet.sh && chmod +x sui_testnet.sh && ./sui_testnet.sh

***Check node

curl -s -X POST http://127.0.0.1:9000 -H 'Content-Type: application/json' -d '{ "jsonrpc":"2.0", "method":"rpc.discover","id":1}' | jq .result.info

****Check node logs

journalctl -u suid -f -o cat

***Delete node

sudo systemctl stop suid
sudo systemctl disable suid
rm -rf ~/sui /var/sui/ /usr/local/bin/sui*
rm /etc/systemd/system/suid.service


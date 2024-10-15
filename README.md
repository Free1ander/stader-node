# stader-node

## 1. Clone Repository & Install Dependencies:
```
git clone https://github.com/stader-labs/stader-node.git
cd stader-node
pip install -r requirements.txt
docker-compose up -d
```
## 2. Environment Setup:

Edit .env file:

```
ETH_RPC_URL=https://mainnet.infura.io/v3/<your_project_id>
NETWORK=mainnet
ETH_PRIVATE_KEY=<your_eth_private_key>
```
## 3. Run the Node:

Initialize and start the node:

```
./run-node.sh
```
## 4. Register Validator:
```
stader-cli validator register --eth-address <your_eth_address>
```
## 5. Stake ETH:
```
stader-cli validator stake --amount 4 --sd-amount 0.4
```
## 6. Monitor Logs:
Track real-time logs:

```
docker-compose logs -f
```
## 7. Check Node Status:
```
stader-cli node status
```
## 8. Customizing Docker Setup:

If you need to customize Docker containers, modify the docker-compose.yml file. For example, adjust ports:

```
ports:
  - "30303:30303"
  - "8545:8545"
```
## 9. Validator Rewards:

To check rewards, run:

```
stader-cli validator rewards --validator <validator_address>\
```
## 10. Backup Node Data:

Regular backups ensure node reliability:

```
cp -r <stader_node_data_dir> <backup_location>
```
## 11. Node Maintenance:

To restart the node:

```
docker-compose restart
```
To stop:

```
docker-compose down
```
Let me know if you need more commands or advanced configurations!

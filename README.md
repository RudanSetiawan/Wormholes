# Wormholes

Minimal Spesifikasi VPS

4Core vCPU

6/8GB RAM

160GB/200GB SSD/NVME Storage

## Open Port
```
sudo ufw allow 22 && sudo ufw allow 30303/tpc && sudo ufw enable
```

## Install Docker
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl build-essential git wget jq make gcc ack tmux ncdu -y
sudo apt-get install ca-certificates curl gnupg lsb-release -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

## Install Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Install Wormholes
```
git clone https://github.com/wormholes-org/wormholes
```

## Jalankan Wormholes
```
cd wormholes
bash ./wormholes_install.sh
```
Masukkan Private Key https://www.limino.com/#/wallet

## Install Cek Log
```
wget -O checkworm.sh https://raw.githubusercontent.com/pramonoutomo/wormholes-scripts/main/checkworm.sh && chmod +x checkworm.sh && ./checkworm.sh
```

## Cek Log
```
bash ./checkworm.sh
```
Tunggu hingga Sync

## Jadi Validator

![image](https://user-images.githubusercontent.com/91402307/196043288-15910eff-9c2a-4363-a6cc-107dca8cf402.png)
Setelah Sync silahkan delegate ERB Coin disana

## Cara Update Versi 
```
cd wormholes 
bash wormholes_install.sh
```
Tekan Enter tunggu saja sampai selesai 

## Cek Versi
```
curl -X POST -H "Content-Type:application/json" --data '{"jsonrpc":"2.0","method":"eth_version","id":64}' http://127.0.0.1:8545
```
Selesai update versi silahkan tunggu beberapa menit setelah itu cek versi untuk melihat versi terbaru

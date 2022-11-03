# OKP4-Nemeton-Testnet
Incentivized





# Open Knowledge Protocol For (OKP4)

**Dokumen Official :**
> [OKP4](https://docs.okp4.network/)


## Installation
### Update & Install screen
```
sudo apt-get update && sudo apt install git && sudo apt install screen
```

### Install tools yang diperlukan
```
sudo apt-get install -y make bzip2 automake libbz2-dev libssl-dev doxygen graphviz libgmp3-dev \
autotools-dev libicu-dev python2.7 python2.7-dev python3 python3-dev \
autoconf libtool curl zlib1g-dev sudo ruby libusb-1.0-0-dev \
libcurl4-gnutls-dev pkg-config patch llvm-7-dev clang-7 vim-common jq libncurses5
```

### Beri izin akses port
```
ufw allow 22 && ufw allow 8888 && ufw allow 9010 && ufw enable
```

### Clone Repositori
```
git clone https://github.com/okp4/okp4d.git
cd okp4d
```

### Install OKP4d
```
make install
```

### cek jika sudah terinstall
```
okp4d version
``` 
outputnya: ``` v2.2.0 atau 2.2.0 ```

</> 

## Running a Node

### Chain ID 
```
CHAIN_ID=okp4-testnet-1
```

### Set Moniker
```
MONIKER=<isi_nama_node_anda>
```
*<isi_nama_node_anda> diisi bebas, ini akan dibaca sebagai moniker node anda nanti

### Initialize the Node 
```
okp4d init $MONIKER --chain-id $CHAIN_ID
```
*simpan semua file di config/priv_validator_key & config/node_key.json

### Set Genesis
```
cd ..
cd .okp4d/config
nano genesis.json
```
>(tekan ctrl+k sampai field kosong)
* kemudian buka > [file genesis](https://raw.githubusercontent.com/okp4/networks/main/chains/nemeton/genesis.json), copy semuanya, kemudian pastekan kembali ke field yang sudah kosong tadi, lalu tekan ctrl+x lalu y dan enter

Add Peers

# OKP4-Nemeton-Testnet
Incentivized





# Open Knowledge Protocol For (OKP4)

**Dokumen Official :**
> [OKP4](https://docs.okp4.network/)


# Installation
# Auto
```
source <(curl -s https://raw.githubusercontent.com/nodejumper-org/cosmos-scripts/master/okp4/okp4-nemeton/install.sh)
```

# Manual

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


.
.
.
.
.


# Running a Node

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

###  Add Peers
```
PEERS=574354efcdd98c7589b056e98c31e5d45aabbf22@95.217.3.177:26656,34d5901c75666b92c02e661d62589d7eaabbf691@64.225.107.193:26656,95986e08f5baee420d3b72be67826e321663072b@65.109.85.221:6070,003c002f675e819eb6840166c5822394eae9446e@75.119.148.0:5000,7e6a2f8d4db53685dfbdad4eddc25a063b2dd220@185.197.194.200:31656,be7578dbdf52a350b88f29f15d6c6ab90947c3fc@45.81.224.126:26656,23608445bcff9999afbd041985933a7d0cf409fe@51.68.141.191:26656,417b8ef377324f6a83ce284ff95e19456103f9c4@209.145.56.41:36656,fdb3f06d223569755a3d83f6928ef88eaeb28f27@89.108.109.116:26656,06670a6d7b4f43917ff43c96456dab560e768cd8@195.201.194.249:36656,2182373d3ffba08d67a54b50a78102bd1ec4b037@95.216.14.72:33656,17a9132d8148546a8b2bb6f76338fb691a3de587@185.169.252.60:26656,08f5473f079950c31b94de36c844e1e42e75fede@138.201.141.76:06656,6f133dc916eda62b08385088b046df83af4399a7@5.9.181.38:36656,187196748ba6871817f67a82a46ecc8fa8f8584a@192.145.37.152:36656,8b1b953795296de39e82dd04dd578d0bd9f105ed@109.205.181.162:26656,5c49edfa9760169d7f488fde07c6d3187804b971@38.242.200.220:26656,1a3469488a36e7a260b69e543f6306f6dce9723b@65.109.38.208:46656,83194c9a2b3294326e7269469cd469efa719c654@95.216.65.163:36656,4126e8184b7113a7bbab0347e21492d080506430@45.142.212.93:26656,5c1fa384e8fa54cb756e9e22105a113574099a88@34.125.31.243:26656,a5342303239a8fd2fab39a7377b12e129d88cec6@65.109.5.119:60656,5f55d5638a1e8aee0de2fd0ec75d1f755402650d@178.208.228.249:26656,d2b0c5934e119f32cf4eecc954404b717574ed4f@194.233.76.103:26656,a842e142bc56f65eadc30e9cdc51546e22e38c7d@173.249.43.94:26656,cdbf785e20eb004b3bad95957dbe2d119a4f08ff@80.209.239.232:26656,350c61879bb4bd90e3371dbcc6d9b1e52bcfe5e3@116.202.16.227:26656,6edbb5b6e4707211625dcd6ca493555386271265@108.175.13.152:26656,58a85d6318543abe8e81ab4f20753d4fa90d1dcc@91.223.3.190:55156,6ae64ca7f5e5867919c340904e7a468ddd832d1c@104.208.99.54:26656,58d8e7968913ea9fd1a4fc2dfc7f6bfda6f1127e@195.3.221.13:56656,261599efe808c2d1deab3156ad87eaee15815f56@94.130.207.215:36656,4c64db846a14ff7ac2990dc97bd21438d44e6234@135.181.115.115:26686,3376b31aa59a65c174260d9d083d3345b4f3db08@45.61.161.192:26656,007c0884dea393ec1ea5a6da42e47d0da61f7587@65.108.219.5:26656,a009a02a23428538b57591f73ba5a6462c476a70@136.243.88.91:6040,d68ebe705c19ca4c21e430b07ec133c4bd9f35d7@152.69.220.10:26656,b1d361471c09eb071d26ddd610fecc3df79fca48@193.33.194.58:26656,eeced73bd8fe781ff9fb2e2f02c60a1d6ade45c0@80.82.222.145:26656,aa5cc52860381e60f38e88fc3c7f47e04078eaf4@45.87.104.113:61656,604901569a7b17deac75236de7fabbdbbca083d7@65.109.57.141:33656,f045c5324e03d54f96285a33130d3886457e18be@46.4.81.204:49656,29608f98a690d87e6efe365d5c5af980bd678097@65.109.85.226:6070,0eb043a3105ba22c2ab19a394a42b99ecd303301@95.111.252.207:36656,2590f28592a97137de0b6f68043225e2890054b0@65.108.229.225:37656,decab4f626e3b6fdc091e3758d92f703bd8c650e@178.211.139.124:36656,a8bdf781811b36ba225b712ddef3cea5231271bc@65.108.42.105:30656,ebcd770b7fcea7a9634b33aeb4b4643330c9d553@113.30.191.103:26656,affddf671da85dd59f01fc2c0a9b05e9c0eab203@159.65.135.236:26656,debfc0c1a784a43fd87bd6c3af549d9eab93c7d6@62.33.2.182:26656,24802e52cd833cddbb3af50e840e9eeb89905982@167.86.115.26:26656,3e581b0da978b4aa173ed1ab7e1a636e3c70cbb8@20.106.193.160:26656,951bae8787569f0c33651edbac40c97afc6ae198@88.255.100.129:26656,83a5bec69a78e63f18e665b59a6f162363d8a518@65.108.100.53:34656,1a9cfa0b6f19405fa96d5ecd93be068d18603393@185.250.36.151:10656,f6f0ab010d40d181d7d17d7589b91e382b3a8de3@20.15.224.74:26656,a9be7c2e7646c8e3ebddf7f55941e135b868e20a@193.33.195.227:26656,ad5d29c1fc2e5224a51547a677968d84bde76eb8@95.217.118.96:26858,6894c679d851420522baf151e1d1bbf63d9defc9@144.76.97.251:12656,7d801627805fb656e073b11277080ab014510643@167.235.149.1:26656,f595a1386d5ca2e0d2cd81d3c6372c3bf84bbd16@65.109.31.114:2280,8ac312cae38d92c44fba3c9f34631807adacecfb@135.181.248.18:26656,0bd6a4a185f95c20e707b327e924797b5af11b02@95.214.53.178:36656,f27cfc89e60166c4dcb859710a5d12051fb20fbd@154.12.225.88:26656,488f6fb2160ba5148fef6de36e82672c73f47c99@20.255.163.130:26656,14f0b90b5a7d551cd104b67ae187d81eeb02ca07@167.86.101.182:26656,085cf43f463fe477e6198da0108b0ab08c70c8ab@65.108.75.237:6040,767fdefbd14877376ad6205825db0a040f8bd6c0@5.9.199.77:26656,edce5965be6d1ecdd59dcfc976cea3ca10ff85c3@207.180.238.198:26656,188472ca82adaa44b3b1309f892a771e3673d0ff@45.8.133.221:26656,1061de5a15ffc220a4a06c522ec28441fd41c4c8@167.235.192.148:26656,cbdb5c3f7cabda100a096a23140550e89670a390@149.255.32.178:26656,2379bd316d19dd209f37c8d14940bba08b8c6031@66.175.235.233:26656,c9e0d661f49b9fe4d67693e2179501567a68b62c@65.109.5.123:26656,a9846cb942782610feaefaa2676bba0e486dc36d@159.69.65.97:44656,1b245a72c54b714c64b9f5a54a6c5669384c91e9@82.223.101.90:26656,7a95b3def12d08e6649fab160bb4623b317d0ba1@95.217.57.232:46656,1cbe918d4cd8eac6b25ef484459286e53ce8acbb@65.109.31.7:36656,91d7595c0921759a89cf182d955333bcb70909fc@92.43.189.78:26656,5e174d8c1f9906bc4d03bf7d05003036dcc47a46@95.217.34.159:60656,9085d90e79f34fcf0179157cb55d383273858f3f@138.201.203.103:36656,5dc87938cbcfe24b801d1d8d575d7ac19abac6bb@95.216.7.169:56656,bc3de7cc43cc0c0aa43cf435e374225b201addf1@95.217.211.135:37656,a461789181c0b7acaac77749b7c1ada8601e22f7@185.245.183.232:36656,69d82ed4ce97d252355effbe9725e9b530588af6@149.102.140.79:26656,dc14197ed45e84ca3afb5428eb04ea3097894d69@88.99.143.105:26656,d6ac03a2051e55c5511aa59b83c61f3bf37b286a@38.242.147.84:26656,60b7fc4553ef2ba2498b1de890b3415d7007774f@185.194.219.96:26656,400e31ef8ee56f33a57d5b2fa18c62085c9a1869@149.102.135.94:26656,9e3109ba10d8cdb18d37dde787665ad1b38a85ed@65.108.235.107:12656,ef595ee71a161131efadc9edfc0d1ec4bcd82b59@65.108.195.235:25656,5c5b4e55c3af67875efba1b78fbeee77db54cef5@88.198.39.43:26776,8eed844a71fd834d8c99308ca04fbb5633061331@185.216.75.174:36656,8c9771a4332b9165c5be81c89d562043a2663f32@49.12.222.110:26656,3f6f2db064eb6455c973ea9ba3d7814494c1e400@161.97.149.123:26656,9917f412470344841e913415a5ea5da9da96a8fa@65.108.238.217:11014,ae7a130db96f04166ff0db2f83cbd827d223102b@80.65.211.249:2456,394ee378f82a2c7e73dbb601b4e266d3f5185b47@65.108.124.54:37656,2c4a1db8418583fcf60f9ab89356af4d2de8a792@193.203.15.86:26656,0ae7ca5b67a95d950bc3bdc81cec119ec455f18c@144.217.201.167:26656,9ae02970da0f5a5fade69a268fbefdac13b69810@109.226.233.125:29656,dfee3c13f3cff558c1370650763c8195194e9a28@95.217.214.125:26656,e63e7bd171ba513a4fec4ddc6e2deea8aeb23a38@185.245.183.246:23656,27696f7ea1a539e72d0d3ac4b71771a11fa9251a@88.99.39.165:26656,d5b833082a82391fd9a2f21adaf05856a7b9355e@35.242.184.95:26656,5087da66cbdb8d428cbcd57865e8e45ebf8cca3e@45.67.217.120:36656,40bca6d9cd758cfb57c88fd4ac645da436ccfa28@178.18.243.159:26656,26fc3ba3b344063a2e5d550ecf564643accbfa41@80.92.204.131:26656,80aba5a6bdf23829acd0ebd4c2e697051bcb95d8@194.163.190.91:36656,fcd52547b0590d404675894e24f7978c7ce7762e@95.216.215.15:26656,501ad80236a5ac0d37aafa934c6ec69554ce7205@89.149.218.20:26656,886cbce0d90cc025d7480935fdae16af3f3c8bfe@65.109.34.9:46656,f520eae8cf078b363f2e376a88349df075373242@176.124.211.14:26656,3e481c7cccb4881cb2e4cadc3b21509415ab79a2@167.86.71.155:26656,672110154dac7272d68d794487a23a5bb4915ead@173.212.214.154:36656,563ace6361d56ccffaef578b0ff58f3f8ccb62b0@161.97.129.244:26656,1d9053cdf997044c07e0952b1ca90f3a1e4b17c4@75.119.146.75:36656,a82f876be1cfd41a2a1beb06bd4656de5a0dbdf0@74.119.195.123:36656,0ebc762a311f4ca0fdb10964278cb29361270e41@65.109.80.176:16656,c33140aeb168050b0cdce22f55e150063c497279@185.245.183.192:36656,bbce2b9457ae486611d88c5cc2a7898be8fb9f9e@45.67.217.116:36656,f2ef3a1f92ccc10b4fc93e7fcba0edf5779bb7b8@45.67.217.128:36656,c0864edb1e36c52dbee47ce38d8b47ec364a9eb9@135.181.24.128:28656,7cea833024800f360a2d339e633e14eefd19267c@65.108.152.40:26656,c678412f29458f3ec3acb4d3cd48eabe92fcbc05@88.218.168.77:26656,245a5ac3deed7bb70b4ed7fbf6997fbd08e89d94@192.145.37.151:36656,6bf102aab0785c0e788fd48c8734ae00651ca067@94.131.109.222:26656,28d660d4612458576f5066a2e4ccb836cca4c8c6@185.249.227.249:26656,2b6e25566856c841b8e9388eb08f63bdaf203700@185.241.53.73:26656,3bd9453daf17c6200590c2a93fe463de34682c7c@89.22.224.107:26656,93df35ca5b8c53768e91d609ac4805791abdbe9a@62.183.22.243:26656
sed -i.bak -e "s/^persistent_peers *=.*/persistent_peers = \"$PEERS\"/" $HOME/.okp4d/config/config.toml
```

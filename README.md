# hde-create-new-sidechain

- Task ID: [647569182](https://hde.horizen.io/task/647569182)
- Task name: Create a new sidechain
- OS: Linux Mint 20.1 Cinnamon / 64 bits
- Zend_oo: [v2.1.0-beta4](https://github.com/HorizenOfficial/zend_oo/releases/tag/v2.1.0-beta4)
- Sidechains-SDK: [v0.2.6](https://github.com/HorizenOfficial/Sidechains-SDK/releases/tag/0.2.6)

## Install and start a node (mainchain)

Git clone
```
$ git clone https://github.com/HorizenOfficial/zend_oo/
```

Cd to zend_oo
```
$ cd zend_oo
```

Checkout
```
$ git checkout sidechains_testnet
```

Install dependencies
```
sudo apt-get install \
      build-essential pkg-config libc6-dev m4 g++-multilib \
      autoconf libtool ncurses-dev unzip git python \
      zlib1g-dev bsdmainutils automake curl
```
 
 Build
```
 $ ./zcutil/build.sh -j$(nproc)
```
  
Fetch key
```
$ ./zcutil/fetch-params.sh
```

Start Node
```
$ ./src/zend -regtest -websocket
```

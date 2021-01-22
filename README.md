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

## Build Sidechains-SDK

Install Java & Maven.

clone 
```
$ git clone https://github.com/HorizenOfficial/Sidechains-SDK.git
```

cd
```
cd Sidechains-SDK
```

Build
```
$ mvn clean package
```
```
[INFO] -----------------------< com.horizen:Sidechains >-----------------------
[INFO] Building Sidechains 0.2.6                                          [4/4]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ Sidechains ---
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for Sidechains 0.2.6:
[INFO] 
[INFO] io.horizen:sidechains-sdk .......................... SUCCESS [11:01 min]
[INFO] sidechains-sdk-simpleapp ........................... SUCCESS [ 42.414 s]
[INFO] sidechains-sdk-scbootstrappingtools ................ SUCCESS [ 18.936 s]
[INFO] Sidechains ......................................... SUCCESS [  0.016 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  11:30 min
[INFO] Finished at: 2021-01-21T23:35:10-08:00
[INFO] ------------------------------------------------------------------------
```

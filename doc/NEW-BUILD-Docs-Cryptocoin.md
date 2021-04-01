### BUILDING EXTERNAL LIBS ON UBUNTU 18.04 ###
This is a guide to compiling the external depends for building cryptocoin android wallet APK. Follow these instructions and then import the entire folder into android studio to build the APKs.

### Install Dependencies ###
`sudo apt-get update` <br>
`sudo apt-get install build-essential cmake tofrodos libtool-bin build-essential cmake pkg-config libboost-all-dev libssl-dev`

### Clone Cryptocoin Android Wallet Repository ###
`git clone --recursive https://github.com/GonzoTheDev/cryptocoin-android-wallet.git`

### Create Some Missing Directories and Clone Crypto Source ###
`cd cryptocoin-android-wallet/external-libs`
`mkdir build`
`mkdir build/src`
`cd build`
`git clone --recursive https://github.com/GonzoTheDev/crypto`
`cd ..`
`make -j <Thread Count (2x cores)>`


After that you need to copy all .a files into their respective folders in /external-libs, then import the entire cryptocoin-android-wallet folder into android studio and build the APK.

If you are having trouble following my guide, don't be afraid to reach out!



# pico-blink
How to setup dev environment to program Raspberry Pi Pico with C/C++ SDK.

* [tutorial video](https://youtu.be/JhajoAyP8e4)
* [Pico SDK github](https://github.com/raspberrypi/pico-sdk)

# 1. Setup
```sh
$ cd ~/workspace_arm

$ git clone git@github.com:raspberrypi/pico-sdk.git --depth 1
$ cd pico-sdk
$ git submodule update --init
$ cd ..

$ mkdir pico-blink
$ cd pico-blink/

# import pico sdk
$ cp ~/workspace_arm/pico-sdk/external/pico_sdk_import.cmake ./
$ export PICO_SDK_PATH=~/workspace_arm/pico-sdk

# Build
$ mkdir build
$ cd build/
/build$ cmake ..
/build$ make
/build$ ll
total 564
drwxr-xr-x 7 ryan ryan   4096 Sep 23 23:02 ./
drwxr-xr-x 3 ryan ryan   4096 Sep 23 23:02 ../
-rw-r--r-- 1 ryan ryan  18581 Sep 23 23:02 CMakeCache.txt
drwxr-xr-x 5 ryan ryan   4096 Sep 23 23:02 CMakeFiles/
-rw-r--r-- 1 ryan ryan  82077 Sep 23 23:02 Makefile
-rwxr-xr-x 1 ryan ryan   8408 Sep 23 23:02 blink.bin*
-rw-r--r-- 1 ryan ryan 153902 Sep 23 23:02 blink.dis
-rwxr-xr-x 1 ryan ryan  37180 Sep 23 23:02 blink.elf*
-rw-r--r-- 1 ryan ryan 183060 Sep 23 23:02 blink.elf.map
-rw-r--r-- 1 ryan ryan  23718 Sep 23 23:02 blink.hex
-rw-r--r-- 1 ryan ryan  16896 Sep 23 23:02 blink.uf2
-rw-r--r-- 1 ryan ryan   1568 Sep 23 23:02 cmake_install.cmake
drwxr-xr-x 6 ryan ryan   4096 Sep 23 23:02 elf2uf2/
drwxr-xr-x 3 ryan ryan   4096 Sep 23 23:02 generated/
drwxr-xr-x 6 ryan ryan   4096 Sep 23 23:02 pico-sdk/
drwxr-xr-x 3 ryan ryan   4096 Sep 23 23:02 pioasm/

/build$ cp blink.uf2 /media/user/RPI-RP2/
```

# Proxmark3GUI
![downloads](https://img.shields.io/github/downloads/wh201906/Proxmark3GUI/total)  

A cross-platform GUI for [Proxmark3](https://github.com/Proxmark/proxmark3) client

[中文介绍](doc/README/README_zh_CN.md)

***

## Features

+ Easy to find available Serial Port
+ Support raw commands of Proxmark3 client(Official/Iceman)
+ Have a friendly UI to test Mifare cards
    + Support different card size(MINI, 1K, 2K, 4K)
    + Easy to edit Mifare block data
    + Easy to read all/selected blocks with well-designed read logic
    + Easy to write all/selected blocks
    + Support binary(.bin .dump) files and text(.eml) files
    + Analyze Access Bits
    + Support Chinese Magic Card
+ Have basic support for LF commands
+ Customize UI  
+ ...  

***

## Preview
![preview](doc/README/preview.png)  

[more previews](doc/preview/previews.md)  

***

## About Iceman fork/repo

The [Iceman fork/repo](https://github.com/RfidResearchGroup/proxmark3) has more powerful functions. These guys even developed a new hardware called Proxmark3 RDV4 with smart card support. But the official repo and the Iceman repo is not fully compatible.  
This GUI is compatible with Iceman/RRG repo(tested on v4.13441)  

***

## About Compiled Windows clients

A cool guy [Gator96100](https://github.com/Gator96100) creates [ProxSpace](https://github.com/Gator96100/ProxSpace) and makes it possible to compile both the firmware and the client on Windows.  
Also, he makes the [pre-compiled Windows client](https://www.proxmarkbuilds.org/) so you can download it and run your PM3 client on Windows instantly.  
I included his compiled client in my releases so you can use the GUI on the fly, and you can also use the GUI with your prefered client.  
Great thanks to him.  

***

## Build on Linux

    cd ~
    sudo apt-get update
    sudo apt-get install qt5-default libqt5serialport5 libqt5serialport5-dev 
    git clone https://github.com/wh201906/Proxmark3GUI.git --depth=1
    cd Proxmark3GUI
    mkdir build && cd build
    qmake ../src
    make -j4 && make clean
    cp -r ../config ./
    ./Proxmark3GUI

***
## Tutorial

[1.Quickstart](doc/tutorial/Quickstart/quickstart.md)  
[2.Edit Mifare Classic data](doc/tutorial/Edit_Mifare_Classic_data/Edit_Mifare_Classic_data.md)(Proxmark3 hardware is not necessary)  
***

## Update Log:

### V0.2.4
+ Clone EM410x card to T55xx card  

### V0.2.3
+ Fix bug [#27](https://github.com/wh201906/Proxmark3GUI/issues/27)
+ Try to support Non-ASCII path

### V0.2.2
+ Load command format from external json file  
+ Fix bug [#20](https://github.com/wh201906/Proxmark3GUI/issues/20), [#21](https://github.com/wh201906/Proxmark3GUI/issues/21), [#22](https://github.com/wh201906/Proxmark3GUI/issues/22)  
+ Support Iceman/RRG repo v4.13441

### V0.2.1
+ Optimize MIFARE Classic reading logic  
+ Fix bug [#16](https://github.com/wh201906/Proxmark3GUI/issues/16)  
+ Fix bug [#15](https://github.com/wh201906/Proxmark3GUI/issues/15) partially (the path can contain spaces now)  

### V0.2
+ Use Dock widget for more flexible layout  
+ Support basic LF commands  
+ Fix a bug in RawCommand tab  

### V0.1.4
+ Optimize performance  
+ Optimize UI  
+ Search available ports automatically  
+ Add High-DPI support  
+ Support configuring environment variables by script  
(Useful when the client requires specific environment variables)  
+ All functions are compatible with Iceman/RRG repo(tested on v4.9237)  
+ Support specifying client working directory
+ Fix some bugs

### V0.1.3
+ Fix Trailer Decoder
+ Add feedback when writing selected blocks

### V0.1.2
+ Optimize read logic
+ Make UI Customizable
+ Save client path automatically
+ Add Trailer Decoder(Deprecated, plz use V0.1.3 or higher version)
+ Support read/write selected blocks
+ Support a few Iceman functions
+ Fix some bugs

### V0.1.1
+ Complete Mifare module(support simulate and sniff)

### V0.1
+ Able to deal with Mifare card and related files

### V0.0.1
+ a dumb version with a useless GUI and a serial choose box.
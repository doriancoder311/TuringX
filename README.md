# TuringX [TRGX] - Next Generation Blockchain for Neuromorphic Computing

With the end of Moore’s law approaching and Dennard scaling ending, the computing community is increasingly looking at new technologies to enable continued performance improvements. A neuromorphic computer is a nonvon Neumann computer whose structure and function are inspired by biology and physics. Today, such systems can be built and operated using existing technology, even at scale, and are capable of outperforming current quantum computers.

TuringX is a next-generation platform for neuromorphic computing based on a new flexible blockchain protocol. It is designed for the development of software applications and algorithms that utilize neuromorphic hardware and are capable of accelerating computation. To accomplish this goal, the platform connects hosts that are running clusters of neuromorphic chips with users and applications that utilize this next-generation hardware. On the TuringX platform, computation time is exchanged for the TuringX native token. 

TuringX has also developed a proprietary circuit design, the TuringX Neuromorphic Chip, that complements the TuringX ecosystem and turns any modern field programmable gate array (FPGA) based chip into a neuromorphic computing chip that can perform orders of magnitude faster than classical or quantum methodologies for a wide range of applications. Due to the dominance of ASICs in the proof-of-work token mining industry, there is a large amount of dormant FPGA infrastructure available which can be converted into high performance next-generation neuromorphic computing clusters.

For more information, read our [TuringX White Paper](https://github.com/TuringXplatform/TuringX-Whitepaper)

## The TuringX mainnet is live!
Starting from September 16th 2022, the TuringX mainnet is live. Everyone is welcome to join!

## Using the TuringX-App to manage your TRGX

Users who just want to use the TuringX wallet functionality to create wallets or send and receive TRGX are recommended to use the convenient GUI based app. You can find it in the dedicated repository: https://github.com/TuringXplatform/TuringX-Wallet-App 

![TuringX-Wallet-App](https://github.com/TuringXplatform/TuringX-Wallet-App/blob/main/wallet-app-screen.jpg "TuringX Wallet App")

## Mining TRGX and managing TRGX from the command line (precompiled binaries)

The easiest way to start minging TRGX or to manage TRGX wallet(s) from the command line in the terminal is by using our precompiled binaries. Download the version matching your operating system:

Microsoft Windows: https://github.com/TuringXplatform/TuringX/blob/main/Windows_x64_executeables.zip

Apple MacOS: https://github.com/TuringXplatform/TuringX/blob/main/MacOS_M1_executeables.zip

Linux: https://github.com/TuringXplatform/TuringX/blob/main/Ubuntu_22.04.1_executables.tar.xz

Please note that Linux users are required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
```
sudo apt-get install libboost-all-dev (Ubuntu Linux)
```

After downloading the precompiled binary, unzip the executable on your machine. To run a full Node in the TuringX blockchain, run the main service (=daemon) with the following command and wait until your node is fully synchronised with the network:
```
./turingxd
```

![TuringX-Daemon](https://github.com/TuringXplatform/TuringX/blob/main/turingxd.jpg)

From the command line, you can also create and manage your personal wallet to mine and transact your TRGX tokens (make sure you have the main service daemon running):

```
./simplewallet
```

![TuringX-Daemon](https://github.com/TuringXplatform/TuringX/blob/main/simplewallet.jpg)

Then just follow the commands (use "O" to open an existing wallet or "G" to generate a new wallet for your TRGX).

You can also start minig from within the wallet: type the command "start_mining <number_of_threads>" to start mining TRGX. The command "stop_mining" will stop the mining procedure. You can follow your hashrate in the main service daemon with the command "show_hr".

Typing "help" (both in the wallet and in the main service daemon) displays all available functions and features. Please make sure you exit these gracefully by typing in the command "exit".

## Mining TRGX and managing TRGX from the command line (build from source)

You can also entirely build all binaries from the source. First, clone the repository:
```
git clone https://github.com/TuringXplatform/TuringX.git
```

### Linux

It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
```
sudo apt-get install libboost-all-dev (Ubuntu Linux)
```

To compile and build:
```
mkdir build 
cd build
cmake ..
make
```

### MacOS

It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
```
sudo apt-get install libboost-all-dev (Ubuntu Linux)
```

To compile and build:
```
mkdir build 
cd build
cmake ..
make
```

### Windows

1. It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
```
sudo apt-get install libboost-all-dev (Ubuntu Linux)
```

2. It is required to have [cmake](https://cmake.org/) for windows installed.
3. You also need [Microsoft Visual Studio](https://visualstudio.microsoft.com) (2017 or later) installed for the build process.

To compile and build:
```
mkdir build 
cd build
cmake ..
```
Then open Visual Studio. Make sure you have set Solution->Configuration to "Release". You also need to add "bcrypt.lib" to P2P->Properties->Configuration Properties->Librarian->Additional Dependencies. This is necessary to build boost's cryptographic randomizer functions. Once these settings are done, proceed a full build to generate your binaries.





# Onion Monero Prover

Currently, to prove to someone that you send him/her Monero, one can use
 this service [checktx](http://xmr.llcoins.net/checktx.html). However,
 this has some limitations:

 - it uses JavaScript, 
 - it is not available as hidden services,
 - it is dependant on a third party service, i.e., http://moneroblocks.info,
 which is closed sourced.


In this example, these limitations are addressed by development of
an Onion Monero Prover. The prover is

 - fully open sourced, 
 - does not depend on any third party services, 
 - it does not require JavaScript, and
 - is avaliable as a hidden service 

## Address

Tor users:

 - [http://xmrblocksvckbwvx.onion](http://xmrblocksvckbwvx.onion)

Non tor users, can use its clearnet version (thanks to [Gingeropolous](https://github.com/Gingeropolous)):

 - [http://explore.MoneroWorld.com](http://explore.moneroworld.com)


## Prerequisite

Everything here was done and tested using Monero 0.9.4 on Ubuntu 16.04 x86_64.

Instruction for Monero 0.9 compilation and Monero headers and libraries setup are
as shown here:
 - [Compile Monero 0.9 on Ubuntu 16.04 x64](https://github.com/moneroexamples/compile-monero-09-on-ubuntu-16-04)

## C++ code

```c++
```



## Example screenshot

![Onion Monero Blockchain Explorer](https://raw.githubusercontent.com/moneroexamples/onion-monero-blockchain-explorer/master/screenshot/screenshot.jpg)


## Compile and run the prover

##### Monero headers and libraries setup

The Onion Prover uses Monero C++ libraries and headers. Also some functionality
 in the Prover for mempool is achieved through [patching](https://github.com/moneroexamples/compile-monero-09-on-ubuntu-16-04/blob/master/res/tx_blob_to_tx_info.patch)
 the Monero deamon.
 Instructions how to download Monero source files, apply a patch, compile  Monero,
 setup header and library files are presented here:

- https://github.com/moneroexamples/compile-monero-09-on-ubuntu-16-04 (Ubuntu 16.04)
- https://github.com/moneroexamples/compile-monero-09-on-arch-linux (Arch Linux)


##### Compile and run the prover
Once the Monero is compiled and setup, the explorer can be downloaded and compiled
as follows:

```bash
# download the source code
git clone https://github.com/moneroexamples/onion-monero-prover.git

# enter the downloaded sourced code folder
cd onion-monero-prover

# create the makefile
cmake .

# compile
make
```

When compilation finishes executable `xmrprover` should be created.

To run it:
```
./xmrprover
```


Go to your browser: http://127.0.0.1:8083


## Other examples

Other examples can be found on  [github](https://github.com/moneroexamples?tab=repositories).
Please know that some of the examples/repositories are not
finished and may not work as intended.

## How can you help?

Constructive criticism, code and website edits are always good. They can be made through github.

Some Monero are also welcome:
```
48daf1rG3hE1Txapcsxh6WXNe9MLNKtu7W7tKTivtSoVLHErYzvdcpea2nSTgGkz66RFP4GKVAsTV14v6G3oddBTHfxP6tU
```

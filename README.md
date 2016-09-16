# Onion Monero Blockchain Explorer

Curently available Monero blockchain explorer websites have several limitations which are of special importance to privacy-oriented users:

 - they use JavaScript,
 - have images which might be used for [cookieless tracking](http://lucb1e.com/rp/cookielesscookies/),
 - track users activates through google analytics,
 - are closed sourced,
 - are not available as hidden services,
 - provide only basic search capabilities,
 - can't identify users outputs based on provided Monero address and viewkey.


In this example, these limitations are addressed by development of
an Onion Monero Blockchain Explorer. The example not only shows how to use Monero C++ libraries, but also demonstrates how to use:

 - [crow](https://github.com/ipkn/crow) - C++ micro web framework
 - [lmdb++](https://github.com/bendiken/lmdbxx) - C++ wrapper for the LMDB
 - [mstch](https://github.com/no1msd/mstch) - C++ {{mustache}} templates
 - [rapidjson](https://github.com/miloyip/rapidjson) - C++ JSON parser/generator


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


## Compile and run the explorer

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

Example output:

```bash
[mwo@arch onion-monero-prover$ ./xmrprover
2016-May-28 10:04:49.160280 Blockchain initialized. last block: 1056761, d0.h0.m12.s47 time ago, current difficulty: 1517857750
(2016-05-28 02:04:49) [INFO    ] Crow/0.1 server is running, local port 8081
```

Go to your browser: http://127.0.0.1:8081


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

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
 - is available as a hidden service

# The prover's functionality was added to Onion Monero blockchain explorer

https://github.com/moneroexamples/onion-monero-blockchain-explorer

Thus, the prover as a standalone service wont be maintained anymore. 

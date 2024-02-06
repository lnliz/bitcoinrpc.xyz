# bitcoin rpc - a public bitcoind rpc server - [bitcoinrpc.xyz](https://bitcoinrpc.xyz)

Read-only RPC access to a bitcoind node - quick and easy.
Get bitcoind rpc access without the hassle of running your own node.
Perfect for CI/CD or other development and testing.

Warning: "Don't trust - verify" - this is not a suitable replacement for running 
your own bitcoind node but it can be a quick and easy way to get access to a 
bitcoind rpc host for POCs and tests.


__This is still in beta__


Try it yourself at [bitcoinrpc.xyz](https://bitcoinrpc.xyz)


### To test, use the following settings:
```
    rpc host:     <b>bitcoinrpc.xyz:2082</b>   (note the non-standard port 2082)
    rpc user:     <b>tst</b>
    rpc password: <b>this_is_a_test</b>
```



### Connect using bitcoin-cli like this:

```
    $ bitcoin-cli -rpcuser=tst -rpcpassword=this_is_a_test -rpcconnect=bitcoinrpc.xyz:2082 getblock 00000000430a20b3f4f658c153168b6615512dfe1a8362602e44a5e11e83011a

    {
      "hash": "00000000430a20b3f4f658c153168b6615512dfe1a8362602e44a5e11e83011a",
      "confirmations": 828004,
      "strippedsize": 216,
      "size": 216,
      "weight": 864,
      "height": 1002,
      "version": 1,
      "versionHex": "00000001",
      "merkleroot": "9d5c8fde7aa7647a8972c59d7ad8c4527ab989b5f37b599113172b38499492d2",
      "tx": [
        "9d5c8fde7aa7647a8972c59d7ad8c4527ab989b5f37b599113172b38499492d2"
      ],
      "time": 1232348906,
      "nonce": 929536258,
      "bits": "1d00ffff",
      "difficulty": 1,
      "previousblockhash": "00000000a2887344f8db859e372e7e4bc26b23b9de340f725afbf2edb265b4c6",
      "nextblockhash": "000000002d5d8c3264d9c6e352b76430cda7a1edac661a515dd1445c15168de5"
    }
```



### Supported commands:
```
    - decoderawtransaction
    - decodescript
    - getbestblockhash
    - getblock
    - getblockchaininfo
    - getblockcount
    - getblockfilter
    - getblockhash
    - getblockheader
    - getblockstats
    - getblocktemplate
    - getchaintips
    - getchaintxstats
    - getdifficulty
    - getmininginfo
    - getnetworkhashps
    - getnetworkinfo
    - getrawmempool
    - getrawtransaction
    - gettxout
    - validateaddress
```

This is a work-in-progress, there are still some commands being added.
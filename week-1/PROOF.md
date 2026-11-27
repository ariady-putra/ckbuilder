# CKB Academy lesson 2: Send a Transaction

```
tx_hash: 0x837c8b7120bb41c47dc67e8c50d4ced2a1509c3ea6b0925590af676508b8bfa2
```

https://testnet.explorer.nervos.org/transaction/0x837c8b7120bb41c47dc67e8c50d4ced2a1509c3ea6b0925590af676508b8bfa2

## Initial Transaction Information

```json
{
  "version": "0x0",
  "headerDeps": [],
  "cellDeps": [
    {
      "outPoint": {
        "txHash": "0xf8de3bb47d055cdf460d93a2a6e1b05f7432f9777c8c474abf4eec1d4aee5d37",
        "index": "0x0"
      },
      "depType": "depGroup"
    },
    {
      "outPoint": {
        "txHash": "0xec18bf0d857c981c3d1f4e17999b9b90c484b303378e94de1a57b0872f5d4602",
        "index": "0x0"
      },
      "depType": "code"
    }
  ],
  "inputs": [
    {
      "since": "0x0",
      "previousOutput": {
        "txHash": "0x1168751f4e59ee7927fdbddef909a421d827ce16d357315ad7b929989b068618",
        "index": "0x0"
      }
    }
  ],
  "outputs": [
    {
      "capacity": "0x177825f00",
      "lock": {
        "codeHash": "0xf329effd1c475a2978453c8600e1eaf0bc2087ee093c3ee64cc96ec6847752cb",
        "hashType": "type",
        "args": "0x01955abb56a0a56813de3900d95d3faa8945cd17bb00"
      }
    }
  ],
  "outputsData": ["0x"],
  "witnesses": ["0x"]
}
```

## The serialized Transaction before hash function

```
0x190100001c000000200000006e00000072000000a20000000d0100000000000002000000f8de3bb47d055cdf460d93a2a6e1b05f7432f9777c8c474abf4eec1d4aee5d370000000001ec18bf0d857c981c3d1f4e17999b9b90c484b303378e94de1a57b0872f5d46020000000000000000000100000000000000000000001168751f4e59ee7927fdbddef909a421d827ce16d357315ad7b929989b068618000000006b0000000800000063000000100000001800000063000000005f8277010000004b000000100000003000000031000000f329effd1c475a2978453c8600e1eaf0bc2087ee093c3ee64cc96ec6847752cb011600000001955abb56a0a56813de3900d95d3faa8945cd17bb000c0000000800000000000000
```

## Tx Hash

```
0x837c8b7120bb41c47dc67e8c50d4ced2a1509c3ea6b0925590af676508b8bfa2
```

## Message

```
0xe905c3863be2605bba10a012bac1dc2daffe32d92c77f91690c3d6dd8e71b530
```

## Signature

```
0xeef4b02e3d915cdd759527c84984338a0873f5f02eccfa7800324c32c1f3b468042f1cabf954115ba149b0be5a6e57dff4c2513d613562db746702d73b8b33b51c
```

## Witness

```
0x69000000100000006900000069000000550000005500000010000000550000005500000041000000eef4b02e3d915cdd759527c84984338a0873f5f02eccfa7800324c32c1f3b468042f1cabf954115ba149b0be5a6e57dff4c2513d613562db746702d73b8b33b501
```

## Transaction Information with Witness

```json
{
  "version": "0x0",
  "headerDeps": [],
  "cellDeps": [
    {
      "outPoint": {
        "txHash": "0xf8de3bb47d055cdf460d93a2a6e1b05f7432f9777c8c474abf4eec1d4aee5d37",
        "index": "0x0"
      },
      "depType": "depGroup"
    },
    {
      "outPoint": {
        "txHash": "0xec18bf0d857c981c3d1f4e17999b9b90c484b303378e94de1a57b0872f5d4602",
        "index": "0x0"
      },
      "depType": "code"
    }
  ],
  "inputs": [
    {
      "since": "0x0",
      "previousOutput": {
        "txHash": "0x1168751f4e59ee7927fdbddef909a421d827ce16d357315ad7b929989b068618",
        "index": "0x0"
      }
    }
  ],
  "outputs": [
    {
      "capacity": "0x177825f00",
      "lock": {
        "codeHash": "0xf329effd1c475a2978453c8600e1eaf0bc2087ee093c3ee64cc96ec6847752cb",
        "hashType": "type",
        "args": "0x01955abb56a0a56813de3900d95d3faa8945cd17bb00"
      }
    }
  ],
  "outputsData": ["0x"],
  "witnesses": [
    "0x69000000100000006900000069000000550000005500000010000000550000005500000041000000eef4b02e3d915cdd759527c84984338a0873f5f02eccfa7800324c32c1f3b468042f1cabf954115ba149b0be5a6e57dff4c2513d613562db746702d73b8b33b501"
  ]
}
```

## Block Information

```
Block：23198907
Hash：0x1848b48729d58384f246512232c09c44c05f00cb1f6bf34b812c6c8de29a073a

Time：11/27/2026, 3:01:18 PM
Transactions：Count 2
```

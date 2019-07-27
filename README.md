### bip69
---
https://github.com/bitcoinjs/bip69

```js
var bitcoinjs = require('bitcoinjs-lib')
var bip69 = require('bip69')

var inputs = [{
  "txId": "xxx",
  "vout": 0
}, ...]
var outputs = [{
  "txId": new Buffer("xxx", "hex"),
  "vout": 40000000000
}, ...]

var sortedInputs = bip69.sortInputs(inputs)
var sortedOutputs = bip69.sortOutputs(outputs)

var txb = new bitcoinjs.TransactionBuilder()

sortedInputs.forEach(function (input) {
  txb.addInput(input.txId, input.vout)
})

sortedOutputs.forEach(function (output) {
  txb.addOutput(bitcoinjs.Script.fromBuffer(output.script), output.value)
})

```

```
```

```
```



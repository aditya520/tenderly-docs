---
description: >-
  A brief overview of supported Ethereum JSON RPC calls.
---

{% hint style='info'%}
This page shows a brief overview of supported Ethereum JSON RPC calls. 
Find a [detaild list of supported calls](detailed-json-rpc.md).
{% endhint %}

## `eth_getBlockByHash`

Returns information about a block by hash.
      
[Detailed version](./detailed-json-rpc.md#eth_getBlockByHash)



**RESULT**: Block information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    false
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    false
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetBlockByHash() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getBlockByHash', ["0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e", false]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetBlockByHash()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "number": "0x77ed36",
    "hash": "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    "parentHash": "0xdf9734476dcc360d864e31cc8422ce96f8aa8dff9a827b57f2c3c4ec8f71c421",
    "nonce": "0x0000000000000000",
    "mixHash": "0x3dd2d65fcd45d469cdca6e524382053d27b9e36b2b2e2f5808247c406d6bafd5",
    "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
    "logsBloom": "0x00300000000000080000000800800800000040c000080012000888102002041000000000020002000020000040000800000008000002404100001000402468300844000080000008880800280808090000000001001400000000290040000800000400004200088001402280800008120d000040104000000000001000800080000000840060480001020000000005000000008028000204010208008020004002050800500002900000083080000000010000010400006100100000000000200804900200000800051400001800a050000008240001001000000028008060201034004000020011200008080000008880080008000048019040000081000010",
    "stateRoot": "0x1a6a2f5902392bf771ec405d427eae2df1c634ed26705e182e48adb893e2fa22",
    "miner": "0x4d496ccc28058b1d74b7a19541663e21154f9c84",
    "difficulty": "0x0",
    "extraData": "0x",
    "size": "0xead",
    "gasLimit": "0x1c9c380",
    "gasUsed": "0x20af8f",
    "timestamp": "0x635e2a44",
    "transactionsRoot": "0x24254b70d82f362e21f82ca841a893d1fe714fcdadba260fac0032359a40d9d8",
    "receiptsRoot": "0x956eb9e1ec572a6d044663dc0085bf421d6cf49193e383b4dc004c36e2f676e5",
    "baseFeePerGas": "0x10",
    "totalDifficulty": "0xa4a470",
    "uncles": [],
    "transactions": [
      "0xea5bbd6f391894557eec975d161391f25ce4cf86cc404964a2c39957b11dad43",
      "0x08f23a8d29dc0b23989b648f11fd89fad609c6694305b5d35e9b6d5fe1616d3a",
      "0x912b1146c5bc2c17b2e0726cc43d51ba9d22e19cd0a38dd248062520349db02b",
      "0xf10ba2f27477339095f9e7b60611812d6ca2a75e69e72f6acb64e2b109ae74b8",
      "0x559fd3851c1470cac199885335676fedcdde9789aee0ad894feef6705be7139c",
      "0x2ecf200a6c4da6478430acfac77a58fe90bd9c7db8c5bc19059eecd87dbb6794",
      "0xe5227c1cc37b2c7af8ef050fbc56913425b01b82b1866fa5099ba512630ae7d1",
      "0x4033bed32cca181377b703e742f092142447a0ab65ae4c1fb8a156d816ac397f",
      "0x6d8d45835f7101188cb9e7b5e8fb18e3d1fdc3bd26e3417ffbed63423a936c37",
      "0xe78704b2a82a49603ca2cdeffde7543911b68207ff397ed756e19da125e3eda6"
    ]
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_getBlockByNumber`

Returns information about a block by number.
      
[Detailed version](./detailed-json-rpc.md#eth_getBlockByNumber)



**RESULT**: Block information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
    "latest",
    false
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
    "latest",
    false
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetBlockByNumber() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getBlockByNumber', ["latest", false]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetBlockByNumber()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "number": "0x78497e",
    "hash": "0x0c9773247f923b16c93934650d117c4d4741211613d30ea58961701877f2c0ee",
    "parentHash": "0x1935b69c024eea35339e1f4184ba28f0c48b731e599e7cb47117e3d259a2ba61",
    "nonce": "0x0000000000000000",
    "mixHash": "0x94305febf472336718208517422274222f7469c1e4e50c2fbba39b6bc78bb875",
    "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
    "logsBloom": "0x00000000000000040000000000000000000000000000102000000008000008000000000100000000000000000000010000400000000020000000020000000000000000000400000800000008000000000000204000800000000000008000000000000000020000000000000000000800000000004008000000800010020800000000000000000000000800000000000000010001000000000000010000000000000000000000040000000000000210000000000000000000000000000040000000004002000800000000000000080004000001000000000000000100000020000802000000400000001000000040080000000000000000400000000000000000",
    "stateRoot": "0x6cd5638736c7f544426f499241d4a8800d1b2c8474110cbe42d296109900482d",
    "miner": "0x4d496ccc28058b1d74b7a19541663e21154f9c84",
    "difficulty": "0x0",
    "extraData": "0x",
    "size": "0x782",
    "gasLimit": "0x1c9c380",
    "gasUsed": "0x5bc79",
    "timestamp": "0x636377d0",
    "transactionsRoot": "0xb9ddb9742d0cedfba53c556f68473fe1a0ef7b2481e9e716bdd6127feea4abb3",
    "receiptsRoot": "0x0f99c0914f8debb4b4adef53fdfb51d82bf664cc54c7d884eb53ac237d53c7ac",
    "baseFeePerGas": "0x36ee5d9d2",
    "totalDifficulty": "0xa4a470",
    "uncles": [],
    "transactions": [
      "0x9af208aea7f591a20684f7a0ceb74760b23451f81b3ee7e82692138ec3f90497",
      "0x4fd55ab3722492d58a8df12ed9e429064793fa4ba24e3f53804f9335ae457e28",
      "0xe1309742bffcab4a8c93a177b6c4465751f11b50192fa3062948e8016ab89385",
      "0xaaf485fb922a25f7b64877bd751775ab368b9c48e7f1e7bce144a0031eead825",
      "0x04c4f5c40fff45a87a9f43bf5283e6c3164ed81883cf353d031afbd147c0418b",
      "0xb87e8b3b8b4f479efbbc348ec87d3a07d63bed8eb7f50f9ad2b8a4960dd14945"
    ]
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_getBlockTransactionCountByHash`

Returns the number of transactions in a block from a block matching the given block hash.
      
[Detailed version](./detailed-json-rpc.md#eth_getBlockTransactionCountByHash)



**RESULT**: Transaction count

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetBlockTransactionCountByHash() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getBlockTransactionCountByHash', ["0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetBlockTransactionCountByHash()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0xa"
}
```
{% endtab %}

{% endtabs %}







## `eth_getBlockTransactionCountByNumber`

Returns the number of transactions in a block matching the given block number.
      
[Detailed version](./detailed-json-rpc.md#eth_getBlockTransactionCountByNumber)



**RESULT**: Transaction count

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByNumber",
  "params": [
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByNumber",
  "params": [
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetBlockTransactionCountByNumber() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getBlockTransactionCountByNumber', ["latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetBlockTransactionCountByNumber()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x6"
}
```
{% endtab %}

{% endtabs %}







## `eth_getUncleCountByBlockHash`

Returns the number of uncles in a block from a block matching the given block hash.
      
[Detailed version](./detailed-json-rpc.md#eth_getUncleCountByBlockHash)



**RESULT**: Uncle count

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockHash",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetUncleCountByBlockHash() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getUncleCountByBlockHash', ["0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetUncleCountByBlockHash()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0"
}
```
{% endtab %}

{% endtabs %}







## `eth_getUncleCountByBlockNumber`

Returns the number of transactions in a block matching the given block number.
      
[Detailed version](./detailed-json-rpc.md#eth_getUncleCountByBlockNumber)



**RESULT**: Uncle count

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockNumber",
  "params": [
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockNumber",
  "params": [
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetUncleCountByBlockNumber() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getUncleCountByBlockNumber', ["latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetUncleCountByBlockNumber()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0"
}
```
{% endtab %}

{% endtabs %}







## `eth_chainId`

Returns the chain ID of the current network.
      
[Detailed version](./detailed-json-rpc.md#eth_chainId)



**RESULT**: Chain ID

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_chainId",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_chainId",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runChainId() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_chainId', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runChainId()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x5"
}
```
{% endtab %}

{% endtabs %}







## `eth_syncing`

Returns an object with data about the sync status or false.
      
[Detailed version](./detailed-json-rpc.md#eth_syncing)



**RESULT**: Syncing status

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_syncing",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_syncing",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runSyncing() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_syncing', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runSyncing()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": false
}
```
{% endtab %}

{% endtabs %}







## `eth_accounts`

Returns a list of addresses owned by client.
      
[Detailed version](./detailed-json-rpc.md#eth_accounts)



**RESULT**: Accounts

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_accounts",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_accounts",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runAccounts() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_accounts', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runAccounts()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": []
}
```
{% endtab %}

{% endtabs %}







## `eth_blockNumber`

Returns the number of most recent block.
      
[Detailed version](./detailed-json-rpc.md#eth_blockNumber)



**RESULT**: Block number

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_blockNumber",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_blockNumber",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runBlockNumber() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_blockNumber', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runBlockNumber()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x78497e"
}
```
{% endtab %}

{% endtabs %}







## `eth_call`

Executes a new message call immediately without creating a transaction on the block chain.
      
[Detailed version](./detailed-json-rpc.md#eth_call)



**RESULT**: Return data

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_call",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    },
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_call",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    },
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runCall() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_call', [{
  "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
  "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
  "value": "0x0",
  "data": "0x2e7700f0"
}, "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runCall()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0000000000000000000000000000000000000000000000000000000000000001"
}
```
{% endtab %}

{% endtabs %}







## `eth_estimateGas`

Generates and returns an estimate of how much gas is necessary to allow the transaction to complete.
      
[Detailed version](./detailed-json-rpc.md#eth_estimateGas)



**RESULT**: Gas used

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_estimateGas",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    },
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_estimateGas",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    },
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runEstimateGas() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_estimateGas', [{
  "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
  "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
  "value": "0x0",
  "data": "0x2e7700f0"
}, "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runEstimateGas()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x5bf6"
}
```
{% endtab %}

{% endtabs %}







## `eth_gasPrice`

Returns the current price per gas in wei.
      
[Detailed version](./detailed-json-rpc.md#eth_gasPrice)



**RESULT**: Gas price

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_gasPrice",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_gasPrice",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGasPrice() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_gasPrice', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGasPrice()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x36f6f672e"
}
```
{% endtab %}

{% endtabs %}







## `eth_maxPriorityFeePerGas`

Returns the current maxPriorityFeePerGas per gas in wei.
      
[Detailed version](./detailed-json-rpc.md#eth_maxPriorityFeePerGas)



**RESULT**: Max priority fee per gas

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_maxPriorityFeePerGas",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_maxPriorityFeePerGas",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runMaxPriorityFeePerGas() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_maxPriorityFeePerGas', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runMaxPriorityFeePerGas()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x898d5c"
}
```
{% endtab %}

{% endtabs %}







## `eth_feeHistory`

Transaction fee history
      
[Detailed version](./detailed-json-rpc.md#eth_feeHistory)



**RESULT**: feeHistoryResult
Fee history for the returned block range. This can be a subsection of the requested range if not all blocks are available.
{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_feeHistory",
  "params": [
    2,
    "latest",
    []
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_feeHistory",
  "params": [
    2,
    "latest",
    []
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runFeeHistory() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_feeHistory', [2, "latest", []]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runFeeHistory()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "oldestBlock": "0x78497d",
    "baseFeePerGas": [
      "0x33474d6dc",
      "0x36ee5d9d2",
      "0x303c9facb"
    ],
    "gasUsedRatio": [
      0.7849216666666666,
      0.012530966666666667
    ]
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_newFilter`

Creates a filter object, based on filter options, to notify when the state changes (logs).
      
[Detailed version](./detailed-json-rpc.md#eth_newFilter)



**RESULT**: Filter Identifier

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_newFilter",
  "params": [
    null
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_newFilter",
  "params": [
    null
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runNewFilter() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_newFilter', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runNewFilter()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0xc7ab5ea3fc83132683f43dd31a31e252425404ef2e9d9bf38bc2a7fe69d52794"
}
```
{% endtab %}

{% endtabs %}







## `eth_newBlockFilter`

Creates a filter in the node, to notify when a new block arrives.
      
[Detailed version](./detailed-json-rpc.md#eth_newBlockFilter)



**RESULT**: Filter Identifier

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_newBlockFilter",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_newBlockFilter",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runNewBlockFilter() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_newBlockFilter', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runNewBlockFilter()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0xc5697a3f85c054bb88138f675958c407475ea36e2ca6a3557877a7f03b0e0a54"
}
```
{% endtab %}

{% endtabs %}







## `eth_mining`

Returns whether the client is actively mining new blocks.
      
[Detailed version](./detailed-json-rpc.md#eth_mining)



**RESULT**: Mining status

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_mining",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_mining",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runMining() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_mining', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runMining()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": false
}
```
{% endtab %}

{% endtabs %}







## `eth_hashrate`

Returns the number of hashes per second that the node is mining with.
      
[Detailed version](./detailed-json-rpc.md#eth_hashrate)



**RESULT**: Mining status

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_hashrate",
  "params": []
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_hashrate",
  "params": []
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runHashrate() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_hashrate', []);

  // Print the output to console
  console.log(result);
}

(async ()=> {runHashrate()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0"
}
```
{% endtab %}

{% endtabs %}







## `eth_getBalance`

Returns the balance of the account of given address.
      
[Detailed version](./detailed-json-rpc.md#eth_getBalance)



**RESULT**: Balance

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBalance",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getBalance",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetBalance() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getBalance', ["0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b", "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetBalance()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0"
}
```
{% endtab %}

{% endtabs %}







## `eth_getStorageAt`

Returns the value from a storage position at a given address.
      
[Detailed version](./detailed-json-rpc.md#eth_getStorageAt)



**RESULT**: Value

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getStorageAt",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "0x0000000000000000000000000000000000000000000000000000000000000001",
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getStorageAt",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "0x0000000000000000000000000000000000000000000000000000000000000001",
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetStorageAt() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getStorageAt', ["0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b", "0x0000000000000000000000000000000000000000000000000000000000000001", "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetStorageAt()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x0000000000000000000000000000000000000000000000000000000000000000"
}
```
{% endtab %}

{% endtabs %}







## `eth_getTransactionCount`

Returns the number of transactions sent from an address.
      
[Detailed version](./detailed-json-rpc.md#eth_getTransactionCount)



**RESULT**: Transaction count

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionCount",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionCount",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetTransactionCount() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getTransactionCount', ["0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b", "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetTransactionCount()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x1"
}
```
{% endtab %}

{% endtabs %}







## `eth_getCode`

Returns code at a given address.
      
[Detailed version](./detailed-json-rpc.md#eth_getCode)



**RESULT**: Bytecode

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getCode",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getCode",
  "params": [
    "0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b",
    "latest"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetCode() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getCode', ["0x05c476a8b9a1a69c47ca81944fbb13a1ac55d62b", "latest"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetCode()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": "0x6080604052600436106100e15760003560e01c806380f59a651161007f578063c01a8c8411610059578063c01a8c8414610349578063c642747414610372578063d0549b851461039b578063ee22610b146103c657610138565b806380f59a65146102a05780639ace38c2146102dd578063a0e67e2b1461031e57610138565b806320ea8d86116100bb57806320ea8d86146101ce5780632e7700f0146101f75780632f54bf6e1461022257806333ea3dc81461025f57610138565b8063025e7c271461013d57806306fdde031461017a5780630bc0fe8f146101a557610138565b36610138573373ffffffffffffffffffffffffffffffffffffffff167f90890809c654f11d6e72a28fa60149770a0d11ec6c92319d6ceb2bb0a4ea1a15344760405161012e929190611704565b60405180910390a2005b600080fd5b34801561014957600080fd5b50610164600480360381019061015f919061176d565b6103ef565b60405161017191906117db565b60405180910390f35b34801561018657600080fd5b5061018f61042e565b60405161019c919061188f565b60405180910390f35b3480156101b157600080fd5b506101cc60048036038101906101c79190611a25565b61046b565b005b3480156101da57600080fd5b506101f560048036038101906101f0919061176d565b61086e565b005b34801561020357600080fd5b5061020c610b48565b6040516102199190611a81565b60405180910390f35b34801561022e57600080fd5b5061024960048036038101906102449190611a9c565b610b55565b6040516102569190611ae4565b60405180910390f35b34801561026b57600080fd5b506102866004803603810190610281919061176d565b610b75565b604051610297959493929190611b54565b60405180910390f35b3480156102ac57600080fd5b506102c760048036038101906102c29190611bae565b610c88565b6040516102d49190611ae4565b60405180910390f35b3480156102e957600080fd5b5061030460048036038101906102ff919061176d565b610cb7565b604051610315959493929190611b54565b60405180910390f35b34801561032a57600080fd5b50610333610db2565b6040516103409190611cac565b60405180910390f35b34801561035557600080fd5b50610370600480360381019061036b919061176d565b610e40565b005b34801561037e57600080fd5b5061039960048036038101906103949190611d83565b61111d565b005b3480156103a757600080fd5b506103b0611327565b6040516103bd9190611a81565b60405180910390f35b3480156103d257600080fd5b506103ed60048036038101906103e8919061176d565b61132d565b005b600181815481106103ff57600080fd5b906000526020600020016000915054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b60606040518060400160405280600e81526020017f4d756c746953696757616c6c6574000000000000000000000000000000000000815250905090565b60008060019054906101000a900460ff1615905080801561049c5750600160008054906101000a900460ff1660ff16105b806104c957506104ab30611625565b1580156104c85750600160008054906101000a900460ff1660ff16145b5b610508576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016104ff90611e64565b60405180910390fd5b60016000806101000a81548160ff021916908360ff1602179055508015610545576001600060016101000a81548160ff0219169083151502179055505b7f63a242a632efe33c0e210e04e4173612a17efa4f16aa4890bc7e46caece80de0600a6040516105759190611ec9565b60405180910390a160008351116105c1576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016105b890611f30565b60405180910390fd5b6000821180156105d2575082518211155b610611576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161060890611fc2565b60405180910390fd5b60005b835181101561080857600084828151811061063257610631611fe2565b5b60200260200101519050600073ffffffffffffffffffffffffffffffffffffffff168173ffffffffffffffffffffffffffffffffffffffff1614156106ac576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016106a39061205d565b60405180910390fd5b600260008273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff1615610739576040517f08c379a0000000000000000000000000000000000000000000000000000000008152600401610730906120c9565b60405180910390fd5b6001600260008373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060006101000a81548160ff0219169083151502179055506001819080600181540180825580915050600190039060005260206000200160009091909190916101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555050808061080090612118565b915050610614565b508160038190555080156108695760008060016101000a81548160ff0219169083151502179055507f7f26b83ff96e1f2b6a682f133852f6798a09c465da95921460cefb3847402498600160405161086091906121a9565b60405180910390a15b505050565b600260003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff166108fa576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016108f190612210565b60405180910390fd5b806005805490508110610942576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016109399061227c565b60405180910390fd5b816005818154811061095757610956611fe2565b5b906000526020600020906005020160030160009054906101000a900460ff16156109b6576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016109ad906122e8565b60405180910390fd5b6000600584815481106109cc576109cb611fe2565b5b906000526020600020906005020190506004600085815260200190815260200160002060003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff16610a79576040517f08c379a0000000000000000000000000000000000000000000000000000000008152600401610a7090612354565b60405180910390fd5b6001816004016000828254610a8e9190612374565b9250508190555060006004600086815260200190815260200160002060003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060006101000a81548160ff021916908315150217905550833373ffffffffffffffffffffffffffffffffffffffff167fc423fd18c78c483f167229efa90b29abe30eed1425ab9cb40441f6555650eca860405160405180910390a350505050565b6000600580549050905090565b60026020528060005260406000206000915054906101000a900460ff1681565b6000806060600080600060058781548110610b9357610b92611fe2565b5b906000526020600020906005020190508060000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff168160010154826002018360030160009054906101000a900460ff168460040154828054610bf4906123d7565b80601f0160208091040260200160405190810160405280929190818152602001828054610c20906123d7565b8015610c6d5780601f10610c4257610100808354040283529160200191610c6d565b820191906000526020600020905b815481529060010190602001808311610c5057829003601f168201915b50505050509250955095509550955095505091939590929450565b60046020528160005260406000206020528060005260406000206000915091509054906101000a900460ff1681565b60058181548110610cc757600080fd5b90600052602060002090600502016000915090508060000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1690806001015490806002018054610d16906123d7565b80601f0160208091040260200160405190810160405280929190818152602001828054610d42906123d7565b8015610d8f5780601f10610d6457610100808354040283529160200191610d8f565b820191906000526020600020905b815481529060010190602001808311610d7257829003601f168201915b5050505050908060030160009054906101000a900460ff16908060040154905085565b60606001805480602002602001604051908101604052809291908181526020018280548015610e3657602002820191906000526020600020905b8160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019060010190808311610dec575b5050505050905090565b600260003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff16610ecc576040517f08c379a0000000000000000000000000000000000000000000000000000000008152600401610ec390612210565b60405180910390fd5b806005805490508110610f14576040517f08c379a0000000000000000000000000000000000000000000000000000000008152600401610f0b9061227c565b60405180910390fd5b8160058181548110610f2957610f28611fe2565b5b906000526020600020906005020160030160009054906101000a900460ff1615610f88576040517f08c379a0000000000000000000000000000000000000000000000000000000008152600401610f7f906122e8565b60405180910390fd5b826004600082815260200190815260200160002060003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff1615611027576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161101e90612455565b60405180910390fd5b60006005858154811061103d5761103c611fe2565b5b9060005260206000209060050201905060018160040160008282546110629190612475565b9250508190555060016004600087815260200190815260200160002060003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060006101000a81548160ff021916908315150217905550843373ffffffffffffffffffffffffffffffffffffffff167f52a3954c699324c8e90e7e2f7cb9f57cd61af1902197bafcc5085b6c2a57b82360405160405180910390a35050505050565b600260003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff166111a9576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016111a090612210565b60405180910390fd5b6000600580549050905060056040518060a001604052808673ffffffffffffffffffffffffffffffffffffffff1681526020018581526020018481526020016000151581526020016000815250908060018154018082558091505060019003906000526020600020906005020160009091909190915060008201518160000160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555060208201518160010155604082015181600201908051906020019061128c929190611648565b5060608201518160030160006101000a81548160ff0219169083151502179055506080820151816004015550508373ffffffffffffffffffffffffffffffffffffffff16813373ffffffffffffffffffffffffffffffffffffffff167f52e5c631bb2fd786d6b1c26f68548e07c61d087bf325770dd88d072cf0a5e8b086866040516113199291906124cb565b60405180910390a450505050565b60035481565b600260003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060009054906101000a900460ff166113b9576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016113b090612210565b60405180910390fd5b806005805490508110611401576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016113f89061227c565b60405180910390fd5b816005818154811061141657611415611fe2565b5b906000526020600020906005020160030160009054906101000a900460ff1615611475576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161146c906122e8565b60405180910390fd5b60006005848154811061148b5761148a611fe2565b5b90600052602060002090600502019050600354816004015410156114e4576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016114db90612547565b60405180910390fd5b60018160030160006101000a81548160ff02191690831515021790555060008160000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168260010154836002016040516115549190612606565b60006040518083038185875af1925050503d8060008114611591576040519150601f19603f3d011682016040523d82523d6000602084013e611596565b606091505b50509050806115da576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016115d190612669565b60405180910390fd5b843373ffffffffffffffffffffffffffffffffffffffff167f5445f318f4f5fcfb66592e68e0cc5822aa15664039bd5f0ffde24c5a8142b1ac60405160405180910390a35050505050565b6000808273ffffffffffffffffffffffffffffffffffffffff163b119050919050565b828054611654906123d7565b90600052602060002090601f01602090048101928261167657600085556116bd565b82601f1061168f57805160ff19168380011785556116bd565b828001600101855582156116bd579182015b828111156116bc5782518255916020019190600101906116a1565b5b5090506116ca91906116ce565b5090565b5b808211156116e75760008160009055506001016116cf565b5090565b6000819050919050565b6116fe816116eb565b82525050565b600060408201905061171960008301856116f5565b61172660208301846116f5565b9392505050565b6000604051905090565b600080fd5b600080fd5b61174a816116eb565b811461175557600080fd5b50565b60008135905061176781611741565b92915050565b60006020828403121561178357611782611737565b5b600061179184828501611758565b91505092915050565b600073ffffffffffffffffffffffffffffffffffffffff82169050919050565b60006117c58261179a565b9050919050565b6117d5816117ba565b82525050565b60006020820190506117f060008301846117cc565b92915050565b600081519050919050565b600082825260208201905092915050565b60005b83811015611830578082015181840152602081019050611815565b8381111561183f576000848401525b50505050565b6000601f19601f8301169050919050565b6000611861826117f6565b61186b8185611801565b935061187b818560208601611812565b61188481611845565b840191505092915050565b600060208201905081810360008301526118a98184611856565b905092915050565b600080fd5b7f4e487b7100000000000000000000000000000000000000000000000000000000600052604160045260246000fd5b6118ee82611845565b810181811067ffffffffffffffff8211171561190d5761190c6118b6565b5b80604052505050565b600061192061172d565b905061192c82826118e5565b919050565b600067ffffffffffffffff82111561194c5761194b6118b6565b5b602082029050602081019050919050565b600080fd5b61196b816117ba565b811461197657600080fd5b50565b60008135905061198881611962565b92915050565b60006119a161199c84611931565b611916565b905080838252602082019050602084028301858111156119c4576119c361195d565b5b835b818110156119ed57806119d98882611979565b8452602084019350506020810190506119c6565b5050509392505050565b600082601f830112611a0c57611a0b6118b1565b5b8135611a1c84826020860161198e565b91505092915050565b60008060408385031215611a3c57611a3b611737565b5b600083013567ffffffffffffffff811115611a5a57611a5961173c565b5b611a66858286016119f7565b9250506020611a7785828601611758565b9150509250929050565b6000602082019050611a9660008301846116f5565b92915050565b600060208284031215611ab257611ab1611737565b5b6000611ac084828501611979565b91505092915050565b60008115159050919050565b611ade81611ac9565b82525050565b6000602082019050611af96000830184611ad5565b92915050565b600081519050919050565b600082825260208201905092915050565b6000611b2682611aff565b611b308185611b0a565b9350611b40818560208601611812565b611b4981611845565b840191505092915050565b600060a082019050611b6960008301886117cc565b611b7660208301876116f5565b8181036040830152611b888186611b1b565b9050611b976060830185611ad5565b611ba460808301846116f5565b9695505050505050565b60008060408385031215611bc557611bc4611737565b5b6000611bd385828601611758565b9250506020611be485828601611979565b9150509250929050565b600081519050919050565b600082825260208201905092915050565b6000819050602082019050919050565b611c23816117ba565b82525050565b6000611c358383611c1a565b60208301905092915050565b6000602082019050919050565b6000611c5982611bee565b611c638185611bf9565b9350611c6e83611c0a565b8060005b83811015611c9f578151611c868882611c29565b9750611c9183611c41565b925050600181019050611c72565b5085935050505092915050565b60006020820190508181036000830152611cc68184611c4e565b905092915050565b600080fd5b600067ffffffffffffffff821115611cee57611ced6118b6565b5b611cf782611845565b9050602081019050919050565b82818337600083830152505050565b6000611d26611d2184611cd3565b611916565b905082815260208101848484011115611d4257611d41611cce565b5b611d4d848285611d04565b509392505050565b600082601f830112611d6a57611d696118b1565b5b8135611d7a848260208601611d13565b91505092915050565b600080600060608486031215611d9c57611d9b611737565b5b6000611daa86828701611979565b9350506020611dbb86828701611758565b925050604084013567ffffffffffffffff811115611ddc57611ddb61173c565b5b611de886828701611d55565b9150509250925092565b7f496e697469616c697a61626c653a20636f6e747261637420697320616c72656160008201527f647920696e697469616c697a6564000000000000000000000000000000000000602082015250565b6000611e4e602e83611801565b9150611e5982611df2565b604082019050919050565b60006020820190508181036000830152611e7d81611e41565b9050919050565b6000819050919050565b6000819050919050565b6000611eb3611eae611ea984611e84565b611e8e565b6116eb565b9050919050565b611ec381611e98565b82525050565b6000602082019050611ede6000830184611eba565b92915050565b7f6f776e6572732072657175697265640000000000000000000000000000000000600082015250565b6000611f1a600f83611801565b9150611f2582611ee4565b602082019050919050565b60006020820190508181036000830152611f4981611f0d565b9050919050565b7f696e76616c6964206e756d626572206f6620726571756972656420636f6e666960008201527f726d6174696f6e73000000000000000000000000000000000000000000000000602082015250565b6000611fac602883611801565b9150611fb782611f50565b604082019050919050565b60006020820190508181036000830152611fdb81611f9f565b9050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052603260045260246000fd5b7f696e76616c6964206f776e657200000000000000000000000000000000000000600082015250565b6000612047600d83611801565b915061205282612011565b602082019050919050565b600060208201905081810360008301526120768161203a565b9050919050565b7f6f776e6572206e6f7420756e6971756500000000000000000000000000000000600082015250565b60006120b3601083611801565b91506120be8261207d565b602082019050919050565b600060208201905081810360008301526120e2816120a6565b9050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b6000612123826116eb565b91507fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff821415612156576121556120e9565b5b600182019050919050565b6000819050919050565b600060ff82169050919050565b600061219361218e61218984612161565b611e8e565b61216b565b9050919050565b6121a381612178565b82525050565b60006020820190506121be600083018461219a565b92915050565b7f6e6f74206f776e65720000000000000000000000000000000000000000000000600082015250565b60006121fa600983611801565b9150612205826121c4565b602082019050919050565b60006020820190508181036000830152612229816121ed565b9050919050565b7f747820646f6573206e6f74206578697374000000000000000000000000000000600082015250565b6000612266601183611801565b915061227182612230565b602082019050919050565b6000602082019050818103600083015261229581612259565b9050919050565b7f747820616c726561647920657865637574656400000000000000000000000000600082015250565b60006122d2601383611801565b91506122dd8261229c565b602082019050919050565b60006020820190508181036000830152612301816122c5565b9050919050565b7f7478206e6f7420636f6e6669726d656400000000000000000000000000000000600082015250565b600061233e601083611801565b915061234982612308565b602082019050919050565b6000602082019050818103600083015261236d81612331565b9050919050565b600061237f826116eb565b915061238a836116eb565b92508282101561239d5761239c6120e9565b5b828203905092915050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052602260045260246000fd5b600060028204905060018216806123ef57607f821691505b60208210811415612403576124026123a8565b5b50919050565b7f747820616c726561647920636f6e6669726d6564000000000000000000000000600082015250565b600061243f601483611801565b915061244a82612409565b602082019050919050565b6000602082019050818103600083015261246e81612432565b9050919050565b6000612480826116eb565b915061248b836116eb565b9250827fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff038211156124c0576124bf6120e9565b5b828201905092915050565b60006040820190506124e060008301856116f5565b81810360208301526124f28184611b1b565b90509392505050565b7f63616e6e6f742065786563757465207478000000000000000000000000000000600082015250565b6000612531601183611801565b915061253c826124fb565b602082019050919050565b6000602082019050818103600083015261256081612524565b9050919050565b600081905092915050565b60008190508160005260206000209050919050565b60008154612594816123d7565b61259e8186612567565b945060018216600081146125b957600181146125ca576125fd565b60ff198316865281860193506125fd565b6125d385612572565b60005b838110156125f5578154818901526001820191506020810190506125d6565b838801955050505b50505092915050565b60006126128284612587565b915081905092915050565b7f7478206661696c65640000000000000000000000000000000000000000000000600082015250565b6000612653600983611801565b915061265e8261261d565b602082019050919050565b6000602082019050818103600083015261268281612646565b905091905056fea26469706673582212206c9d550f615a6cc987e89a94b4f4b6d7be4c8c2da4ace7b55292611c528f9a8864736f6c63430008090033"
}
```
{% endtab %}

{% endtabs %}







## `eth_sendTransaction`

Signs and submits a transaction.
      
[Detailed version](./detailed-json-rpc.md#eth_sendTransaction)



**RESULT**: Transaction hash

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_sendTransaction",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    }
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_sendTransaction",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    }
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runSendTransaction() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_sendTransaction', [{
  "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
  "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
  "value": "0x0",
  "data": "0x2e7700f0"
}]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runSendTransaction()})();
```
{% endtab %}

{% tab title="Response" %}
```json
N/A
```
{% endtab %}

{% endtabs %}







## `eth_sendRawTransaction`

Submits a raw transaction.
      
[Detailed version](./detailed-json-rpc.md#eth_sendRawTransaction)



**RESULT**: Transaction hash

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_sendRawTransaction",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    }
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_sendRawTransaction",
  "params": [
    {
      "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
      "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
      "value": "0x0",
      "data": "0x2e7700f0"
    }
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runSendRawTransaction() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_sendRawTransaction', [{
  "from": "0xDC6bDc37B2714eE601734cf55A05625C9e512461",
  "to": "0xff39a3e734fe363e631441f6d24c7539240c2628",
  "value": "0x0",
  "data": "0x2e7700f0"
}]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runSendRawTransaction()})();
```
{% endtab %}

{% tab title="Response" %}
```json
N/A
```
{% endtab %}

{% endtabs %}







## `eth_getTransactionByHash`

Returns the information about a transaction requested by transaction hash.
      
[Detailed version](./detailed-json-rpc.md#eth_getTransactionByHash)



**RESULT**: Transaction information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByHash",
  "params": [
    "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByHash",
  "params": [
    "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetTransactionByHash() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getTransactionByHash', ["0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetTransactionByHash()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "blockHash": "0xb39de02094847558d1b5b7be17899af87d4026419f063946d347aeb4b8f17b56",
    "blockNumber": "0x7787e4",
    "transactionIndex": "0x24",
    "hash": "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188",
    "from": "0xdc6bdc37b2714ee601734cf55a05625c9e512461",
    "to": "0xd9ded92319814d8f3587dfad7be72ca71e16697a",
    "input": "0xee22610b0000000000000000000000000000000000000000000000000000000000000000",
    "nonce": "0x17",
    "value": "0x0",
    "gas": "0xf4240",
    "gasPrice": "0x9a26693e",
    "maxPriorityFeePerGas": "0x59682f00",
    "maxFeePerGas": "0xab58f0b6",
    "accessList": [],
    "chainId": "0x5",
    "type": "0x2",
    "v": "0x1",
    "r": "0x1a54710a2409beff5e5726830497f9f56f0ae1545c25b4436d8ac8d68900c2e8",
    "s": "0x5b6b60bbb030b1f88d098252d98b4731d7e89d6b1a8b2e7dee61c2ea45866f29"
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_getTransactionByBlockHashAndIndex`

Returns information about a transaction by block hash and transaction index position.
      
[Detailed version](./detailed-json-rpc.md#eth_getTransactionByBlockHashAndIndex)



**RESULT**: Transaction information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockHashAndIndex",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    "0x1"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockHashAndIndex",
  "params": [
    "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    "0x1"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetTransactionByBlockHashAndIndex() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getTransactionByBlockHashAndIndex', ["0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e", "0x1"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetTransactionByBlockHashAndIndex()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "blockHash": "0x5a10754ae6c673ebabb1a78166232c6b88633d50fafe1499392dd6e4c61c344e",
    "blockNumber": "0x77ed36",
    "transactionIndex": "0x1",
    "hash": "0x08f23a8d29dc0b23989b648f11fd89fad609c6694305b5d35e9b6d5fe1616d3a",
    "from": "0x22841539c4c3a3fa3c1355db7352adfb3a699ada",
    "to": null,
    "input": "0x608060405273b3cb14c326da065d8987e9ef4d771d758dad42a76000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555034801561006457600080fd5b50610196806100746000396000f3fe608060405234801561001057600080fd5b506004361061002b5760003560e01c80639e5faafc14610030575b600080fd5b61003861004e565b6040518082815260200191505060405180910390f35b60008067ffffffff0000ffff60c01b3360601b16905060005b611fff811161015a5760008054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16633370204e826201388001846040518363ffffffff1660e01b8152600401808277ffffffffffffffffffffffffffffffffffffffffffffffff19168152602001915050602060405180830381600088803b15801561010457600080fd5b5087f19350505050801561013957506040513d602081101561012557600080fd5b810190808051906020019092919050505060015b6101425761014d565b50809250505061015d565b8080600101915050610067565b50505b9056fea26469706673582212201082b38baaf4aa56ba1dbf14484c0ecabd8ba0cfb25a9b73905c51f3740d8bdb64736f6c634300060c0033",
    "nonce": "0x85",
    "value": "0x0",
    "gas": "0x282ac",
    "gasPrice": "0x9502f910",
    "maxPriorityFeePerGas": "0x9502f900",
    "maxFeePerGas": "0x9502f920",
    "accessList": [],
    "chainId": "0x5",
    "type": "0x2",
    "v": "0x0",
    "r": "0x1e4c8de7ea1e201d509144f8d081100db747267738c4f4b0e649cda6886f1e4c",
    "s": "0x6177915db9f2b5cd103bcf528a66cdad152f2394eabe42c0d357cd4c45600154"
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_getTransactionByBlockNumberAndIndex`

Returns information about a transaction by block number and transaction index position.
      
[Detailed version](./detailed-json-rpc.md#eth_getTransactionByBlockNumberAndIndex)



**RESULT**: Transaction information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockNumberAndIndex",
  "params": [
    "latest",
    "0x1"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockNumberAndIndex",
  "params": [
    "latest",
    "0x1"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetTransactionByBlockNumberAndIndex() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getTransactionByBlockNumberAndIndex', ["latest", "0x1"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetTransactionByBlockNumberAndIndex()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "blockHash": "0x5e90342dd3068502937f00b6a167dfcd972cb10fe8baef71dadc7c003c5cbfd6",
    "blockNumber": "0x78497f",
    "transactionIndex": "0x1",
    "hash": "0xdaed43a62f763553a2c552a3749da4477414a6469185b5f4e8d8e76e800a00bd",
    "from": "0x5043cb357681b26b56960f54d573855900e47911",
    "to": "0x805fe47d1fe7d86496753bb4b36206953c1ae660",
    "input": "0x85ff842c00000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000080383847bd75f91c168269aa74004877592f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e900000000000000000000000000000000000000000000000000000000000aae6000000000000000000000000000000000000000000000000000000000000000145043cb357681b26b56960f54d573855900e47911000000000000000000000000",
    "nonce": "0x30",
    "value": "0x58d15e176280000",
    "gas": "0x61a80",
    "gasPrice": "0x35d3229cb",
    "maxPriorityFeePerGas": "0x59682f00",
    "maxFeePerGas": "0x44bf58000",
    "accessList": [],
    "chainId": "0x5",
    "type": "0x2",
    "v": "0x1",
    "r": "0x9f5162f8de803f863c7bec113ba4da681a5de0362020393f018f9f9f01ec687f",
    "s": "0x230b8e9b75727f7c5be31548f65dbe1fbe5ffdeca2741e95157003d737f5a099"
  }
}
```
{% endtab %}

{% endtabs %}







## `eth_getTransactionReceipt`

Returns the receipt of a transaction by transaction hash.
      
[Detailed version](./detailed-json-rpc.md#eth_getTransactionReceipt)



**RESULT**: Receipt Information

{% tabs %}
{% tab title="Raw" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionReceipt",
  "params": [
    "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"
  ]
}
```
{% endtab %}

{% tab title="cURL" %}
```bash

curl https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY \
-X POST \
-H "Content-Type: application/json" \
-d \
'{
  "id": 0,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionReceipt",
  "params": [
    "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"
  ]
}'

```
{% endtab %}

{% tab title="ethers" %}
```javascript
// Installation Instructions: https://docs.ethers.io/v5/getting-started/#installing
const { ethers } = require('ethers');


async function runGetTransactionReceipt() {
  // Initialize an ethers instance
  const provider = new ethers.providers.JsonRpcProvider('https://goerli.gateway.tenderly.co/$TENDERLY_WEB3_GATEWAY_KEY');

  // Execute method
  const result = await provider.send('eth_getTransactionReceipt', ["0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188"]);

  // Print the output to console
  console.log(result);
}

(async ()=> {runGetTransactionReceipt()})();
```
{% endtab %}

{% tab title="Response" %}
```json
{
  "id": 0,
  "jsonrpc": "2.0",
  "result": {
    "type": "0x2",
    "status": "0x1",
    "cumulativeGasUsed": "0x65f9a6",
    "logsBloom": "0x02000008000000000000000000000000000000000000000000000004000000000000000000000000000000004000000000000000000000400000000000000000000000000000000000000000000000000000000000000000000000000000000040000000020000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000008000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000008000000000",
    "logs": [
      {
        "address": "0xd9ded92319814d8f3587dfad7be72ca71e16697a",
        "topics": [
          "0x5445f318f4f5fcfb66592e68e0cc5822aa15664039bd5f0ffde24c5a8142b1ac",
          "0x000000000000000000000000dc6bdc37b2714ee601734cf55a05625c9e512461",
          "0x0000000000000000000000000000000000000000000000000000000000000000"
        ],
        "data": "0x",
        "blockNumber": "0x7787e4",
        "transactionHash": "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188",
        "transactionIndex": "0x24",
        "blockHash": "0xb39de02094847558d1b5b7be17899af87d4026419f063946d347aeb4b8f17b56",
        "logIndex": "0x55",
        "removed": false
      }
    ],
    "transactionHash": "0xd9724b68ad04ac3919678e3158f5d474d3c129cfb4cb7fafcde9b4c756fce188",
    "from": "0xdc6bdc37b2714ee601734cf55a05625c9e512461",
    "to": "0xd9ded92319814d8f3587dfad7be72ca71e16697a",
    "contractAddress": null,
    "gasUsed": "0x19280",
    "effectiveGasPrice": "0x9a26693e",
    "blockHash": "0xb39de02094847558d1b5b7be17899af87d4026419f063946d347aeb4b8f17b56",
    "blockNumber": "0x7787e4",
    "transactionIndex": "0x24"
  }
}
```
{% endtab %}

{% endtabs %}






# Blockchain

This is simple implementation for bitcoin that inspired by the book [Learn Blockchain Programming with JavaScript](https://github.com/PacktPublishing/Learn-Blockchain-Programming-with-JavaScript/tree/96721e76c6b4ddbdbe146ff9eec35ba35a15c1c3). keep it as simple as possible to be used as educational material, this is only the core of decentralized system communication, and the minimal logic of transaction.

## Blockchain summary

Bitcoin is a system which keeps track of virtual coins, accounts which contain them, and transactions between those, without relying on a central authority like a bank or PayPal or a government.

## Installation

node v15.7.0
npm 7.4.3

## Usage

### start new node

``` javascript
PORT=3000 npm start http://localhost:3000
```

### Rest API

|METHOD|Endpoint|Description|
|----|----|----|
|GET| /api/blockchain | get entire blockchain | 
|GET| /api/blockchain/mine | mine a block | 
|GET| /api/blockchain/consensus | consensus between nodes | 
|POST| /api/transaction/broadcast | broadcast transaction  Content-Type: application/json payload {"amount": Number , "sender": String , "recipient": String} | 
|POST| /api/network/register-and-broadcast-node | regester new node to the system Content-Type: application/json payload={"newNodeUrl":http://[ip]:[port]}'

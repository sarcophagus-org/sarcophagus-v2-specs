```mermaid
sequenceDiagram
  participant Archaeologists
  participant Smart Contracts

  Archaeologists->>Smart Contracts: Call `unwrap` function

  Note right of Archaeologists: pass in<br/>- id of Sarcophagus<br/>- private keys for encrypted shards

  Smart Contracts->>Smart Contracts: verify

  Note left of Smart Contracts: contracts have public keys, so<br/> can use on-chain code to verify<br/>that input private key derives<br/>stored public key

  Smart Contracts->>Archaeologists: distribute reward, mark complete
```

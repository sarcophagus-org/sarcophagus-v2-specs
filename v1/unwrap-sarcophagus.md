```mermaid
sequenceDiagram
  participant Archaeologists
  participant Smart Contracts

  Archaeologists->>Smart Contracts: Call `unwrap` function

  Note right of Archaeologists: pass in<br/>- id of Sarcophagus<br/>- private key corresponding to public key on sarcophagus

  Smart Contracts->>Smart Contracts: verify

  Note left of Smart Contracts: contract has archaeologist public key, so<br/> can use on-chain code to verify<br/>that input private key derives<br/>stored public key

  Smart Contracts->>Archaeologists: distribute reward, mark complete
```
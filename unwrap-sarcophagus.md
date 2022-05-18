```mermaid
sequenceDiagram
  participant Archaeologists
  participant Smart Contracts

  Archaeologists->>Smart Contracts: Call `unwrap` function

  Note right of Archaeologists: pass in<br/>- id of Sarcophagus<br/>- unencrypted shard

  Smart Contracts->>Smart Contracts: verify

  Note left of Smart Contracts: Validate unencrypted shard <br />(contracts have hashes of unencrypted shards, <br /> so they can use on-chain code to verify that the input unencrypted shard is valid) <br /> <br /> Validate caller is archaeologist on sarcophagus (using msg.sender or signature)

  Smart Contracts->>Archaeologists: distribute reward, mark complete
```

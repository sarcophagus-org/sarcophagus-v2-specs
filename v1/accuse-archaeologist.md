```mermaid
sequenceDiagram
  participant Third Party
  participant Smart Contracts

  Third Party->>Smart Contracts: Call `accuse` function

  Note right of Archaeologist: pass in<br/>- id of sarcophagus <br/>- hash of inner layer
  
  Smart Contracts->>Smart Contracts: Verify Inner Layer Hash
  
  Note right of Smart Contracts: distributes bond: <br/>- half to ebmalmer<br/>- half to third party
  Note right of Smart Contracts: distributes bounty + digging fees to embalmer
```
```mermaid
sequenceDiagram
  participant Embalmer
  participant Archaeologists
  participant Smart Contracts

  Embalmer->>Smart Contracts: Call `rewrap` function

  Note right of Embalmer: pass in<br/>- id of Sarcophagus<br/>- new resurrection time<br/>- fees

  Smart Contracts->>Smart Contracts: Verify

  Note left of Smart Contracts: verify new resurrection time<br/> and fees are within archaeologist limits<br/> Update archaeologist bond if necessary 

  Smart Contracts->>Archaeologists: distribute digging fees, update resurrection time
```
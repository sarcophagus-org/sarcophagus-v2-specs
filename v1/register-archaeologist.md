```mermaid
sequenceDiagram
  participant Archaeologist
  participant Smart Contracts

  Archaeologists->>Smart Contracts: Call `register` function

  Note right of Archaeologist: pass in<br/>- min fees <br/>- min resurrection time <br/>- endpoint<br/>- free bond to add
```
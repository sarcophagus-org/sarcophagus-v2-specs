```mermaid
stateDiagram-v2
  [*] --> Pending
  Pending --> [*]: Cancelled
  Pending --> Active
  Active --> Active: Rewrapped
  Active --> Closeable: DMS triggered
  Closeable --> Expired: Window expired
  Active --> [*]: Buried
  Active --> [*]: Accused
  Closeable --> [*]: Unwrap
  Expired --> [*]: Cleaned up
```

https://mermaidjs.github.io/mermaid-live-editor

# Request Handling

```mermaid
sequenceDiagram
  activate Frontend
  Client->>Frontend: Request
  Frontend->>Requests Queue: Request
  Requests Queue-->>Request Handler: Request
  activate Request Handler
  Request Handler->>States Db: Changed Object States
  Request Handler->>States Db: Transaction State
  opt Should we keep transaciton data in log or as states?
      Request Handler->> Transaction Log: Transaction
  end
  Request Handler->>Responses Queue: Response
  deactivate Request Handler
  Responses Queue-->> Frontend: Response
  Frontend->>Client: Response
  deactivate Frontend
```

- Each `Frotnend` has its own `Response Queue`
- Request
  - Modification operation, JSON
  - Sync, Binary package Avro
  - View, JSON
  - Upload big data attachment
  - Download big data
  
   
  
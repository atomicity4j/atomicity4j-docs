https://mermaidjs.github.io/mermaid-live-editor

# Request Handling

```mermaid
sequenceDiagram
  activate Frontend
  Client->>Frontend: Request
  Frontend->>Requests Queue: Request
  Note over Frontend: Each request can have its own queue
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

# States Db

Why we need `States Db`? To provide `eventual atomicity`.

- Each request can modify one or few states
- Eventually all modifications must be either applied or compensated

Design details:

- Each state has a key
- State is a `dedicated` if only one transaction can own the state key. Dedicated states keep owner
- State is `shared` if few transactions can be applied. Shared states must keep list of all applied transactions

Example: customer must have unique email 
- Two states are needed to handle this requirement
- `Customer Email` is a dedicated  state, has an `email` as a key and `Customer.id` as a value
- `Customer Data` is a shared state, has `customer.id` as a key and customer fields as a value
- `Create Customer` reqest  first try to create  `Customer Email` state, if ok, `Customer Data` is created
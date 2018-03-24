https://mermaidjs.github.io/mermaid-live-editor

# Client Message Handling

sequenceDiagram
  activate Frontend
  Client->>Frontend:Client Message
  Frontend->>Client Messages Queue: Client Message
  Client Messages Queue-->>Message Handler: Client Message
  activate Message Handler
  Message Handler->>States Db: Changed States
  Message Handler->>States Db: Transaction State
  opt Keep log in Kafka???
      Message Handler->> Kafka: Transaction
  end
  Message Handler->>Responses Queue: Response
  deactivate Message Handler
  Responses Queue-->> Frontend: Response
  Frontend->>Client: Response
  deactivate Frontend

- Each `Frotnend` has its own `Response Queue`
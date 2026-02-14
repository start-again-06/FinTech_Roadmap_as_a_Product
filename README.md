```mermaid
sequenceDiagram
    autonumber
    participant User
    participant App
    participant PaymentService
    participant Bank

    User->>App: Initiate payment
    App->>PaymentService: Create payment request
    PaymentService->>Bank: Process transaction
    Bank-->>PaymentService: Success / Failure
    PaymentService-->>App: Transaction status
    App-->>User: Payment confirmation

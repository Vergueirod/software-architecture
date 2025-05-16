# Personal Software Architecture Guide

## Code and System Design Architectures

### Clean Architecture (Robert C. Martin)
- Concentric layers: Entities → Use Cases → Interface Adapters → Frameworks & Drivers.
- Promotes independence from frameworks, UI, and databases.

### Hexagonal Architecture (Ports & Adapters)
- Core logic is surrounded by ports (interfaces) and adapters.
- Simplifies testing and external integration.

### Onion Architecture
- Similar to Clean/Hexagonal, but emphasizes a central domain model with inward-dependent layers.

### Layered Architecture (N-Tier)
- Classic structure: UI → Application → Domain → Infrastructure/Data.
- Simple to implement but can become inflexible as complexity grows.

## Distributed and Integration Architectures

### Microservices Architecture
- System is split into independently deployable services with single responsibilities.
- Communication via REST, gRPC, or events.
- Requires strong DevOps practices, observability, and governance.

### Event-Driven Architecture (EDA)
- Components communicate asynchronously by producing and consuming events.
- Enables high scalability and decoupled systems.

### Service-Oriented Architecture (SOA)
- Legacy style focused on reusable services, often coordinated via an ESB (Enterprise Service Bus).

### Serverless Architecture
- Uses Functions-as-a-Service (FaaS) for handling logic.
- Cost-effective, scalable, and great for event-based workloads.

### SAGA Pattern (Distributed Transaction Management)
- Manages distributed transactions using orchestration or choreography.
- Ensures eventual consistency without relying on 2PC.

## Frontend and UI Architectures

### Micro Frontends
- Microservice principles applied to frontend development.
- Each team can independently build and deploy parts of the UI.
- Integration techniques include Web Components, Module Federation, or iframes.

## Data-Centric Architectures

### Lambda Architecture
- Combines batch and stream processing layers.
- Suitable for big data systems requiring both accuracy and low latency.

### Kappa Architecture
- Stream-only processing model.
- Simpler alternative to Lambda for real-time applications.

### CQRS (Command Query Responsibility Segregation)
- Separates read and write models for scalability and complexity management.

### Event Sourcing
- System state is built from an append-only event log.
- Improves auditability, consistency, and traceability.

## Strategic and Foundational Patterns

### Domain-Driven Design (DDD)
- Not an architecture itself, but a design philosophy.
- Focuses on Bounded Contexts, ubiquitous language, and a rich domain model.

### Backend For Frontend (BFF)
- Creates a dedicated backend per frontend type (e.g., web, mobile).
- Optimizes performance and API usability.

### Monolithic Architecture
- All application components live in a single deployable unit.
- Easy to start with, but becomes harder to scale and maintain over time.

## Modern and Emerging Architectures

### Edge Architecture
- Runs logic closer to the user using edge locations (e.g., CDNs, edge functions).
- Reduces latency and enhances performance.

### Zero Trust Architecture
- Every request must be authenticated and authorized, regardless of network origin.
- Increases security posture in distributed systems.

### Data Mesh
- Decentralized data ownership and product thinking in data systems.
- Encourages domain-aligned teams to own, publish, and govern their data.


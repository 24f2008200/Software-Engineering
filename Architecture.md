There's no single canonical count — different textbooks group them differently — but here are the major, widely-recognized architecture styles, organized by category:

## 1. Layered (N-Tier) Architecture
**Idea:** System is divided into horizontal layers, each with a specific responsibility, where each layer only talks to the layer directly below it.
**Example:** A typical web app with Presentation Layer → Business Logic Layer → Data Access Layer → Database. Classic enterprise Java (Spring MVC) apps follow this.

## 2. Client-Server Architecture
**Idea:** Clients request services/resources; a server provides them. Clean separation of concerns between the requester and the provider.
**Example:** A browser (client) requesting a web page from a web server; a mobile banking app talking to a backend server.

## 3. Microservices Architecture
**Idea:** The application is decomposed into small, independently deployable services, each owning its own data and business capability, communicating over the network.
**Example:** Netflix — separate services for user profiles, recommendations, billing, and streaming, each independently scalable.

## 4. Monolithic Architecture
**Idea:** The entire application is built and deployed as a single, unified unit — all modules share the same codebase, process, and database.
**Example:** A traditional Ruby on Rails or Django app where the UI, business logic, and data access all live in one deployable package.

## 5. Service-Oriented Architecture (SOA)
**Idea:** Similar to microservices but coarser-grained services communicate via an Enterprise Service Bus (ESB), often sharing more infrastructure than microservices do.
**Example:** Large enterprise systems (banks, airlines) with services like "Customer Management" and "Payment Processing" integrated through a centralized bus.

## 6. Event-Driven Architecture (EDA)
**Idea:** Components communicate by producing and consuming events asynchronously, rather than calling each other directly.
**Example:** An e-commerce system where "OrderPlaced" event triggers inventory update, email notification, and shipping — all reacting independently via a message broker like Kafka.

## 7. Microkernel (Plug-in) Architecture
**Idea:** A minimal core system provides basic functionality, and additional features are added via plug-ins/extensions.
**Example:** Eclipse IDE or VS Code — the core editor is minimal, and almost all functionality (language support, debugging, themes) comes from plug-ins.

## 8. Pipe-and-Filter Architecture
**Idea:** Data flows through a series of independent processing components ("filters") connected by "pipes," each transforming the data.
**Example:** Unix command-line pipelines like `cat file.txt | grep "error" | sort | uniq -c`, or a compiler's stages (lexer → parser → optimizer → code generator).

## 9. Peer-to-Peer (P2P) Architecture
**Idea:** No central server — each node (peer) acts as both client and server, sharing resources directly with other peers.
**Example:** BitTorrent for file sharing; blockchain networks like Bitcoin where every node validates and shares data.

## 10. Space-Based Architecture (Cloud/Tuple Space)
**Idea:** Designed to solve scalability bottlenecks by removing the central database dependency — uses in-memory data grids shared across processing units.
**Example:** High-traffic systems like online ticket booking or stock trading platforms that need to avoid database bottlenecks under load spikes.

## 11. Broker Architecture (Message Broker)
**Idea:** A broker component coordinates communication between distributed components, decoupling them from knowing about each other directly.
**Example:** RabbitMQ or ActiveMQ acting as a middleman between publishers and subscribers in a distributed system.

## 12. Domain-Driven Design (Hexagonal / Ports & Adapters)
**Idea:** The core business logic sits at the center, completely isolated from external concerns (UI, database, APIs) via ports and adapters — making it easy to swap infrastructure without touching business logic.
**Example:** A payment processing core that can swap between a REST API adapter, a CLI adapter, or a test adapter, without changing core logic.

## 13. Serverless Architecture
**Idea:** Application logic is deployed as individual functions that run on-demand, with infrastructure fully managed by a cloud provider.
**Example:** AWS Lambda functions triggered by file uploads to S3, or API Gateway routes.

---

## Quick comparison table

| Style | Best for | Trade-off |
|---|---|---|
| Layered | Simple, well-understood apps | Can become rigid; changes ripple across layers |
| Client-Server | Basic distributed apps | Server can be a bottleneck |
| Microservices | Large, independently scaling teams/systems | High operational complexity |
| Monolithic | Small teams, simple deployment | Hard to scale/maintain as it grows |
| SOA | Enterprise integration | ESB can become a bottleneck/single point of failure |
| Event-Driven | Reactive, real-time systems | Harder to trace/debug causality |
| Microkernel | Extensible platforms (IDEs, browsers) | Core must be carefully designed upfront |
| Pipe-and-Filter | Data transformation pipelines | Not ideal for interactive/stateful systems |
| P2P | Decentralized, resilient systems | Harder to secure and coordinate |
| Space-Based | High-scale, low-latency systems | Complex to implement correctly |
| Hexagonal | Testable, infrastructure-agnostic core logic | More upfront design effort |
| Serverless | Event-driven, sporadic workloads | Cold starts, vendor lock-in |

There's no strict "official" number (you'll see courses teach anywhere from 5 to 15+), but the ones above are the styles that show up consistently across software architecture textbooks (Bass, Clements & Kazman; Richards & Ford) and industry practice.



Good question — yes, it's exactly that: a **different level of abstraction**, and the relationship is more "microservices *use* these patterns internally and *are themselves* an architecture-level pattern" than "microservices vs. these patterns."

## The abstraction hierarchy

```
Architecture Style   ← Microservices lives HERE
        ↓
Design Pattern        ← Factory, Builder, Facade, Adapter, etc. live HERE
        ↓
Code / Implementation
```

**Microservices is an architecture style** (like layered, client-server, or event-driven) — it's a system-level decision about how to decompose an *entire application* into independently deployable services. It answers: "How do I structure my whole system?"

**GoF patterns are design patterns** — they solve *localized, recurring problems* inside a single component or class. They answer: "How do I structure this piece of code?"

So a single microservice, internally, might use Factory, Strategy, or Observer in its codebase — the two concepts operate at different zoom levels and aren't competitors.

---

## Where each pattern actually shows up inside/around microservices

| Pattern | Microservices equivalent / usage |
|---|---|
| **Facade** | An **API Gateway** is essentially a Facade at the architecture level — it gives clients one simplified entry point that hides the complexity of dozens of backend services. |
| **Adapter** | Used when integrating a legacy service or third-party API whose interface doesn't match your service contracts — an **Anti-Corruption Layer** in DDD is basically an Adapter between microservices. |
| **Strategy** | A service might use Strategy internally to swap algorithms (e.g., different pricing rules per region), or at the architecture level, **client-side load balancing** (round-robin vs. least-connections) is a Strategy choice. |
| **Observer** | This is huge in microservices — **event-driven architecture** (pub/sub via Kafka, RabbitMQ) is essentially Observer at scale: services subscribe to events instead of being tightly coupled via direct calls. |
| **Factory** | Used for creating service clients/connections dynamically, or in **service discovery**, where you don't hardcode which instance you're talking to. |
| **Builder** | Common in constructing complex configuration objects — e.g., building an HTTP request or a Kafka message with many optional headers/fields. |
| **Iterator** | Less architecture-relevant; stays mostly internal to a service's code (e.g., paginating through a result set from a database call). |

---

## The key conceptual difference

- **Design patterns** solve problems of **object collaboration and code structure** — scoped to a class, module, or single process.
- **Architecture styles** (microservices, layered, event-driven, SOA) solve problems of **system decomposition, deployment, and communication** — scoped to the whole application, often across networks and process boundaries.

A useful way to remember it: **design patterns are "in-process" solutions; architecture styles are "cross-process" (or cross-system) solutions.** Microservices architecture is often *built out of* many instances of these smaller patterns, just applied at a coarser granularity — e.g., Facade becomes API Gateway, Observer becomes a message broker, Adapter becomes an anti-corruption layer.

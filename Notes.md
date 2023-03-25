# Microservices

a microservices architecture is an approach in which a large application is split up into a set of smaller services. Each service runs in its own process and communicates with other processes using protocols such as HTTP/HTTPS, WebSockets, or AMQP.

each microservice should own its related domain data model and domain logic, and could be based on different data storage technologies (SQL, NoSQL) and different programming languages.

# Orchestrator

As introduced previously, in a **microservice-based** approach, each microservice owns its model and data 
so it will be autonomous from a development and deployment point of view. 

These kinds of systems are complex to scale out and manage; therefore, you absolutely need an orchestrator if you want to have a production-ready and scalable multi-container application.

The orchestrator helps with composing applications consisting of many microservices into one deployable unit. That unit is then moved — or deployed — to a host.

# Docker Compose

a tool that lets them build multiple Docker images together as a single unit and then deploy that unit

---

# Container Orchestrator

A container orchestrator is a system that automatically deploys and manages containerized apps.

# Kubernetes

Kubernetes is a portable, extensible open-source platform for managing and orchestrating containerized workloads.

---

# Domain-Driven Design (DDD) design pattern

DDD is a design pattern whereby the structure and language of your code, including class names, methods, and variables, matches the business domain

The pattern describes independent problem areas as bounded contexts, and emphasizes a common language to describe these problems.

*Split the code based on the domain problem*

---

# Resiliency

Resiliency is the ability to recover from transient failures.

## Code-based resiliency

uses Polly, 

### Retry policy

The request is retried after a short wait if an error response is received.

### Circuit Breaker policy

A Circuit Breaker policy gives the target service a break after a repeated number of failures.

## Infrastructure-based resiliency

To implement infrastructure-based resiliency, you can use a **service mesh**. Aside from resiliency without changing code, a service mesh provides traffic management, policy, security, strong identity, and observability.

Architecturally speaking, a service mesh is composed of two components: a control plane and a data plane.

The control plane component has a number of components that support managing the service mesh.

The data plane component consists of proxies that are transparently injected alongside each service—a pattern known as the Sidecar pattern.

Some popular service mesh options for Kubernetes clusters include Linkerd, Istio, and Consul.

---

# Logging and Monitoring

In a microservices architecture, a solution is needed that can:

1. Aggregate log traces from several microservices.
2. Correlate the log traces.
3. Carry additional contextual information, like the hosted infrastructure, to efficiently debug the app.

## Structured Logging

Structured logging is an approach in which logs are written in a consistent message format optimized for machine readability. These messages abide by a predefined schema, which allows the logs to be parsed and treated as data sets.

Each microservice requires a different instrumentation key.
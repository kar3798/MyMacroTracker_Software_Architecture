# ADR 5: Deployment Strategy - Monolithc Vs. Modular Service Design
As we gear up to construct and deploy MyMacroTracker, it's time to think about how we can structure and deploy the backend. The backend will handle, user accounts, meal tracking, AI suggestions, fitness sync, and eventually, possibly some coaching tools.

Given that we are a small team building an MVP, our priority is simplicity and speed, while still ensuring that we can scale and improve the system. 

## Decision 
We will begin with a modular monolith approach - deploying the entire back end as a single service, but architecting the code base into separate modules (e.g., user service, meal planner, AI service, and integration with fitness integration). This allows us to maintain the simplicity of monolithic deployment in the early stages of building during the MVP, but also allows us to split services out later.

## Rationale 
A monolithic deployment keeps things simple and manageable in early development. We can avoid the overhead of maintaining multiple services, reduce DevOps complexity, and focus on building core features. By structuring the code modularly within the monolith, we leave the door open for service separation in the future as the product scales.

Rejected Alternatives:

- Using full microservices from the beginning: While they provide better scalability and fault isolation, they are too complex for a small team building an early stage product. More of their time will be spent on service coordination, deployment, and monitoring than feature building.
 
- Pure monolith with no modular design: Easier in the short term, but would create technical debt and make future refactoring more difficult as the app grows.

## Status
Accepted

## Consequences
- Enables more rapid development and easier deployment for the early use

- Reduces the complexity of DevOps and infrastructure concerns while also validating foundational features of the product

- Codebase will be modularized allowing future concerns about transitioning to microservices later 

- All features are running with the same lifecycle for deployment, meaning any update or failure can affect the entire system of users

- Scalability is compromised short term, but a burden that can be managed for a beta or early adoption approach

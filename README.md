# MyMacroTracker_Software_Architecture

Repo for managing the project deliverables for SE577.

## Deliverable 1: Press Release + FAQ

This deliverable follows the Amazon "Working Backwards" approach. It includes:

- A one-page press release announcing *MyMacroTracker*, a cross-platform meal planning and macro tracking app designed for fitness-focused users.
- A set of FAQs (3 external, 3 internal) addressing key questions from users and stakeholders.

The goal is to define the product vision from a customer-first perspective before technical development begins.

---

## Deliverable 2: Architecture Decision Records (ADRs)

This deliverable includes five key ADRs that define critical architectural decisions for the system:

- Frontend Architecture: React Native vs. Native
- AI Integration: External API vs. In-House Model
- Backend Framework: FastAPI vs. Flask
- Data Storage: PostgreSQL vs. MongoDB
- Deployment Strategy: Monolithic vs. Modular Design

Each ADR outlines the decision context, trade-offs, rationale, and consequences. These decisions establish the foundation for the system’s technical direction and scalability.

---

## Deliverable 3: Architecture Model

This deliverable presents a visual and textual representation of the solution architecture using C4 modeling.

Included diagrams:
- **System Context Diagram**: High-level overview of users and external systems
- **Container Diagram**: Breakdown of frontend, backend, database, and external integrations
- **Component Diagram**: Internal structure of the FastAPI backend, highlighting major service modules

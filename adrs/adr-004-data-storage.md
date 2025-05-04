# ADR 4: Data Storage - Flask Vs. FastAPI
MyMacroTracker needs to store a variety of user data, including profiles, macro goals, meal logs, ingredients, and integration records from fitness platforms. The data is mostly structured and relational, for example, users are linked to their meals, and meals contain multiple ingredients. We need to decide whether to go with a relational database like PostgreSQL or a document-based NoSQL option like MongoDB. This decision will affect how we model our data, query performance, and how easily we can scale the system later on.

## Decision 
We will proceed with using PostgreSQL as the primary database for MyMacroTracker, as it supports relational data modeling along with a strong consistency, and complex queries, all of which align perfectly with our data structure.

## Rationale 
PostgreSQL is proven to be a reliable relational database system that supports joins, constraints, transactions, and structured data modeling. Since our data has clear relationships (users, meals, ingredients, logs), a relational model makes it easier to maintain integrity and write efficient queries.

Rejected Alternatives:

- MongoDB: Flexible and great for unstructured or rapidly evolving data, but probably not ideal when the data is extremely relational. Additionally, ensuring consistency across collections (e.g., syncing meals and users) adds a level of complexity when you're developing your backend.
 
- Firebase/Firestore: It was considered due to the ease of use, but since we're building a custom backend, we can maintain less control over the data schema and indexing.

## Status
Accepted

## Consequences
- Relational data structures enable you to enforce consistency between users, meals, and other objects very easily

- PostgreSQL is widely available and integrates nicely with FastAPI and most Object-Relational Mappers (ORMs)

- Schema changes and updates require advance setup time, but ultimately give you more control 

- Querying complex data, such as user meal history over time, is much easier

- Having a single, structured data model makes debugging and analytics easier as your application grows

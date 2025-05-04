# ADR 2: AI Integration - External API Vs. In-House AI Model
One of the core aspects of MyMacroTracker is to recommend intelligent, personalized meals based on user goals and ingredient availability. This would require the application of some form of AI to drive natural language processing and context-sensitive meal creation. The question must be answered regarding whether or not to build and maintain a tailored AI model internally or make use of an available external AI solution (i.e., OpenAI API). The major drivers behind this decision are development complexity, cost, precision, time to market, scalability, and ultimate control of the AI logic.

## Decision 
Our meal suggestion capability will be further enhanced by an external artificial intelligence API, such as OpenAI's GPT, and the like, in beta and initial releases. This would enable us to add AI capability quickly without training and maintenance fee or hassle of with an In-House AI Model.

## Rationale 
The use of an external API offers the ability to scale, make the application production ready, and offers an easy way to integrate it into our backend. This drastically cuts down on our development time and saves us from the overhead of managing infrastructure for the training, tuning, or scaling of AI models. For a startup-stage product, this allows us to concentrate on delivering a working user experience while leveraging the power of AI.

## Rejected Alternatives:

- In-House AI model creation: This approach was ruled out due to its expense of high computational resources, its complexity, and the need for an expanded team with advanced skill sets. Though bringing better controls and potential cost savings in the long run, it is not viable for MVP or first development.

- Rule-based meal recommendation engine: This was taken as a fall back but ruled out for failing to provide flexible and contextual responses together with personalization.

## Status
Accepted

## Consequences
- Faster delivery of AI features with little work on the engineering part 

- Introduces external dependecies, along with a recurring API usage cost

- Limits control over the behaviour of the model and the customization of the responses 

- Careful handling of user data is required, to follow the terms of privacy and security standards

- Allows for a possible transition to an In-House AI Model as the product scales

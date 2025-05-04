# ADR 1: Frontend Architecture - React Native Vs. Native Development
The MyMacroTracker app must have both mobile and web users catered for. Because of the fitness orientation of the app, most users will access it on their phones, but desktop support will assist with meal planning and the coaching component. We must choose an option that balances development time, code maintainability, user experience, and cost. The biggest trade-off is between developing native apps individually (iOS/Android) and a cross-platform solution. Familiarity with the team, code reusability, and the need for rapid iteration on a startup-level project are also involved in this decision.

## Decision 
We will use React Native for the mobile app (iOS and Android) and React for the web application. Shared logic and components will be reused to reduce development effort and maintain consistency across platforms.

## Rationale 
React Native allows us to build a high-quality cross-platform mobile experience with a single codebase, which is ideal for a small team. It enables rapid development, faster iteration, and code sharing with the React-based web frontend. The ecosystem is mature, and the development team has strong familiarity with JavaScript/TypeScript.

Rejected Alternatives:

- Native iOS and Android apps: Offer strong performance and native UX, but require maintaining two separate codebases, increasing both cost and development time.

- Flutter: Explored as a cross-platform option, but set aside due to limited team experience and weaker alignment with our existing web stack.
## Status
Accepted

## Consequences
- Quicker development and simpler onboarding with common tech stack

- Possible performance compromises in UI-heavy features (e.g., animations, camera support)

- Ability to keep consistency between mobile and web experiences

- Long-term ability to replace individual components with native modules when needed

- Simplifies complexity in the MVP and early release phases

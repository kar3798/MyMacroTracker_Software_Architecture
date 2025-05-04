# ADR 3: Backend Framework - Flask Vs. FastAPI
A Python Web Framework for the backend services needs to be selected. The goal of the backend is to serve APIs, analyze data, authorize users, and interact with third-party applications along with a focus on fitness trackers and AI APIs. The two primary contenders are Flask and FastAPI. Both of which are lightweight and developed in Python, there are differences between both with regards to performance, asynchronous capabilities, and developer experience. Therefore selecting the best candidate will maintain and ensure system efficiency and ultimately a productive team, as well as response time of the entire system.

## Decision 
FastAPI will be the web framework that acts as the backend for MyMacroTracker. FastAPI offers modern, high-performance with automatic documentation, asynchronous support built-in, and performance that is significantly better than Flask.

## Rationale 
FastAPI is built on modern Python standards (ASGI) and supports asynchronous programming out of the box, which will help us handle concurrent operations more efficiently, especially while calling external APIs like OpenAI or fitness trackers. It also auto-generates OpenAPI documentation, which is useful for developers onboarding and third-party integration.

Rejected Alternatives:

- Flask:  Straightforward and established, but it lacks built-in asynchronous capabilities and requires more setup for tasks such as data validation and API documentation.

- Djnano: Considered too weighty for our use case, as it has features (like templating and assumptions about ORM) that are not intrinsic to our service-oriented architecture.

## Status
Accepted

## Consequences
- FastAPI provides better performance and asynchronous capabilities for handling concurrent requests

- Built-in data validation and API documentation improve the developer experience and reduce setup time

- Team members will need to become comfortable with FastAPI's asynchronous syntax and type hints 

- Some external libraries may still be built with Flask in mind, requiring minor workarounds

- This helps us build a more scalable backend that can support increased traffic over time

# Senior Software Engineer Technical Assessment

This assessment consists of two parts that evaluate both your hands-on coding skills and system design thinking.

## Part 1: Code Implementation

### Description

Today we are mapping a SpaceX rocket to a unified model.

This application represents a [Unified API](https://blog.apideck.com/what-is-a-unified-api) with two configured endpoints:

- GET `/hello`
- GET `/space/rockets/{rocket-id}`

If you try out the current app locally using cURL, Postman or another API Client, you'll see that only one is implemented. It's your task to implement the other endpoint.

### Steps to take:

1. Find a working SpaceX API, it's publicly available.
2. Add an [OpenAPI spec](https://swagger.io/specification/) of the SpaceX API that contains all the needed info to connect to it. This spec should be added to the `/src/services/spaceX` folder. Only add the needed info, the full spec is not needed. As our own API is also based on OpenAPI, you can use that as a reference.
3. Add the `rocketsOne` operation to the code base and implement the logic to execute the SpaceX request. Try to use your newly created spaceX spec for this, you can use one or more functions in the utils folder to use this spec.
4. Map the incoming SpaceX response to the Unified model described in the JSON schema you find in the `/unify` folder


## Part 2: System Design Questions

Please answer the following questions about scaling and architecting this unified rocket API. Keep answers concise but specific.

Answer the following questions

#### **Domain & Business Logic**

The system needs to handle different types of APIs (Space, Weather, Transport) each with multiple providers.
  - How would you model and organize the business logic for these different domains?
  - How would you handle shared concepts between domains while maintaining clear boundaries?
   - How would you ensure each domain can evolve independently?


#### **Scalability & Architecture**

How would you design this system to handle 100x more space agencies and traffic? What components would you add/modify in your architecture?

#### **Real-time Updates**

Customers needs real-time updates about changes in different domains (Space, Weather, Transport), How would you solve that?


#### **Error Handling & Reliability**

How would you handle failures from different space agency APIs?


Format for each answer:
- Brief explanation of approach
- Key technical decisions
- Main trade-offs considered
- Simple diagram if relevant

## Submission Guidelines

1. Create a new private repository using this repository as a template:
   - Click the "Use this template" button at the top of this repository
   - Select "Create a new repository"
   - Make sure to set the repository as "Private"
   - Choose a name for your repository
   - Click "Create repository from template"

2. Once you've completed the assessment:
   - Grant repository access to `engineering@apideck.com`
   - Send an email to the hiring manager with your repository URL

## Evaluation Criteria

Your submission will be evaluated on:
1. Code quality and implementation
   - Proper error handling
   - Test coverage
   - Clean code principles
   - Type safety

2. System design answers
   - Clear technical communication
   - Understanding of distributed systems
   - Practical feasibility
   - Recognition of trade-offs

Good luck!
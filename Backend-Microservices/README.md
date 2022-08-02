# Audit-Management-Microservices
### To genrate jar files use `maven clean` on Spring Tool Suite or Command Line.

## Authorization Microservice
- This microservice is used with anonymous access to Generate JWT. Also, this module is used for the Authorization & Validation. And, it provides the endpoints for Authentication and Validation.
- ## Methods:
  - GET: /auth/health-check
  - POST: /auth/authenticate
  - POST: /auth/validate

## Benchmark Microservice
- Audit benchmark Module is a Middleware Microservice that provides the acceptable number of answers with 'NO' as the answer for various audit types.
- ## Methods:
  - GET: /benchmark/AuditBenchmark
  - GET: /benchmark/health-check

## Checklist Microservice
- Audit checklist Module is a Middleware Microservice that provides a list of 'YES/NO' type of questions for the audit based on the audit type. Which will evantually be consumed by the User interface to display the questions on the portal.
- ## Methods:
  - GET: /checklist/AuditCheckListQuestions
  - GET: /checklist/health-check

## Severity Microservice
- Audit Severity Microservice gets the audit response and analyzes the project execution status by getting the Audit benchmark details communicating with other Microservice, compares the current project data and determine project execution status and the duration in which remedial action should be taken.
- ## Methods:
  - POST: /severity/ProjectExecutionStatus
  - GET: /severity/health-check

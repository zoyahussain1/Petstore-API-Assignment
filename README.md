# API Testing Assignment - Petstore

This repository contains a beginner-friendly API testing assignment focused on the Swagger Petstore API. The goal is to build solid fundamentals in functional, negative, performance, and security testing using free public APIs.

## Assignment Overview

You will build and execute a mini test suite for the Swagger Petstore API `/pet` endpoints using Postman and supporting tools.

### Scope
- Endpoints: `/pet`
- Methods: `POST`, `GET`, `PUT`, `DELETE`
- Test types: Functional, Negative, Performance, Security

## Public APIs Covered (For Practice)
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/)
- [ReqRes](https://reqres.in/)
- [Swagger Petstore](https://petstore.swagger.io/)
- [SWAPI](https://swapi.dev/)
- [OpenWeatherMap](https://openweathermap.org/api)
- [GitHub REST API](https://docs.github.com/en/rest)

---

## Test Plan

**Objective**  
Verify that the `/pet` endpoints in the Swagger Petstore API work correctly under normal and edge conditions.

**Environment**  
- Base URL: `https://petstore.swagger.io/v2`
- Tool: Postman

**Test Data Examples**
- Valid Pet ID: `123456`
- Invalid Pet ID: `999999999`
- SQL Injection: `"DROP TABLE pets"`
- Missing Name Test: `{ "status": "available" }`

**Tests Performed**
- ✅ Create Pet
- ✅ Get Pet by ID
- ✅ Update Pet
- ✅ Delete Pet
- ✅ Invalid ID
- ✅ Missing fields
- ❌ Performance (Response > 200ms)
- ✅ SQL Injection

---

## Postman Collection

- API Test Collection](https://zoya-3668638.postman.co/workspace/zoya's-Workspace~75af44f9-5353-4682-8aba-0b528ec10e17/collection/44329802-f9823beb-26bf-4c05-8275-946863887121?action=share&creator=44329802)

> Includes pm.test() scripts for CRUD, error handling, security, and performance checks.

---

## Test Summary

| Test                        | Status | Response Time (ms) | Notes                        |
|----------------------------|--------|--------------------|------------------------------|
| Create Pet                 | ✅     | 323                | ID saved                     |
| Get Pet by ID              | ✅     | 301                | Correct info returned        |
| Update Pet                 | ✅     | 303                | Status changed to "sold"     |
| Delete Pet                 | ✅     | 323                | Deleted successfully         |
| Invalid ID (Negative)      | ✅     | 427                | Proper error message         |
| Missing Fields (Negative)  | ✅     | 424                | Handled without error        |
| Performance (20 GETs)      | ❌     | >200ms             | Failed 95th-percentile limit |
| SQL Injection (Security)   | ✅     | 277                | No crash or bad behavior     |

---

## Tools Used
- Postman for API testing
- Newman for CI collection execution
- JSON Schema Validator (Postman)
- JMeter / Artillery (performance testing)

---

## Bug Reporting Template

Use the following format for any bugs found:

- **Title**: Short summary
- **Steps to Reproduce**:
- **Expected Result**:
- **Actual Result**:
- **Request/Response**:
- **Severity**:
- **Priority**:

---

## Learning Outcomes

This assignment strengthens:
- API test planning
- Functional and negative test case design
- Response validation and schema checks
- Performance testing basics
- Simple security checks
- Bug reporting best practices

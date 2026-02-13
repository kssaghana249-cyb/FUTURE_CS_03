# API Security Risk Analysis Report – Task 3

Intern Name: Saghana K S  
Track: Cybersecurity  
Task Code: FUTURE_CS_03  
Internship Program: Future Interns  
Date: 06-02-2026  

---

## Project Overview

This project focuses on basic API security testing and risk analysis using Postman. The objective was to analyze API behavior, inspect HTTP methods and headers, review server responses, and identify potential security risks without performing exploitation.

Public endpoints from httpbin.org were used to safely simulate API testing scenarios.

---

## Objective

- Test API endpoints using GET and POST methods  
- Inspect HTTP status codes and JSON responses  
- Analyze request and response headers  
- Identify potential API security risks  
- Classify risks based on severity  

---

## Tools Used

- Postman (API Testing Tool)  
- httpbin.org (Public API Testing Service)  
- Manual observation and response inspection  

---

## Testing Methodology

The assessment was conducted using a safe and controlled testing approach:

1. Sent HTTP requests (GET and POST) using Postman  
2. Inspected response status codes  
3. Analyzed JSON response structure  
4. Examined request and response headers  
5. Documented observations  
6. Identified potential security weaknesses  

No exploitation or harmful testing was performed.

---

## Test Case 1 – GET Request

**Endpoint:** https://httpbin.org/get  
**Method:** GET  
**Status Code:** 200 OK  
**Response Type:** JSON  

### Observation:

The server successfully returned data without requiring authentication, indicating an open endpoint.

---

## Test Case 2 – POST Request

**Endpoint:** https://httpbin.org/post  
**Method:** POST  
**Payload:** Username and password in JSON format  
**Status Code:** 200 OK  
**Response Type:** JSON (echoed data)

### Observation:

The API accepted and processed the submitted data successfully. No authentication or input validation mechanisms were enforced.

---

## Test Case 3 – Header Analysis

**Endpoint:** https://httpbin.org/headers  
**Method:** GET  
**Custom Header Added:** Authorization: Bearer sampletoken123  
**Status Code:** 200 OK  

### Observation:

The server reflected the Authorization header without validating it, demonstrating how APIs receive authentication-related headers but may not enforce validation.

---

## Identified Security Risks

| Risk Identified | Description | Severity |
|-----------------|------------|----------|
| Open Endpoints | API accessible without authentication | Medium |
| Missing Authentication | No enforcement of authentication tokens | High |
| Header Misuse | Authorization headers accepted without validation | Medium |
| Input Validation | User input accepted without checks | Medium |
| Rate Limiting | No visible rate limiting mechanism | Low |

---

## Risk Severity Classification

- High Risk: Missing authentication mechanisms  
- Medium Risk: Open endpoints, header misuse, input validation issues  
- Low Risk: Lack of rate limiting enforcement  

---

## Suggested Remediation Steps

- Implement proper authentication and authorization  
- Use secure token-based authentication (JWT or OAuth)  
- Validate and sanitize user inputs  
- Apply rate limiting to prevent abuse  
- Restrict access to sensitive endpoints  
- Monitor and log suspicious API activity  

---

## Key Learning Outcomes

- Understanding API request/response structure  
- Practical exposure to HTTP methods and status codes  
- Risk identification and classification  
- Basic API security assessment methodology  

---

## Ethical Considerations

This API security analysis was performed strictly for educational purposes as part of the Future Interns Cybersecurity Internship.

Public testing endpoints (httpbin.org) were used to ensure no real system was impacted. No exploitation, brute force, or intrusive testing techniques were performed.

---

## Repository Contents

- API Security Risk Analysis Report (PDF)
- Evidence screenshots (inside Evidence folder)
- Documentation of testing methodology

---

## Disclaimer

This project was conducted for academic and internship evaluation purposes only.

All API testing was performed on publicly available test endpoints designed for safe experimentation. No real-world systems, confidential data, or private APIs were accessed or compromised.

This repository demonstrates fundamental API security testing concepts only.


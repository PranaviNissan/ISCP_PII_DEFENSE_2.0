# Deployment Strategy – Project Guardian 2.0

## Overview

The PII redacting system should be deployed to prevent sensitive data leaks in real time. E-commerce platforms handle sensitive data: names, addresses, phone numbers, payment info, even IP addresses. Redacting PII ensures that this data isn’t exposed in logs, error messages, customer support transcripts, or analytics dashboards.

## Suggested Deployment Layers

1. **API Gateway Plugin / Middleware**
   - Place the code at the ingress layer of APIs.
   - This redacts sensitive data before it reaches logs or downstream systems or personnel
   - This deploymnet gives centralised control and is also quite easy to scale

2. **Sidecar Container**
   - Deploy the code alongside critical services.
   - This has the chance to intercept outbound data streams.
   - We can provide service-level isolation while making few to no changes to main application code.

3. **DaemonSet (Kubernetes)**
   - Monitor logs across pods and redact PII in real time.
     

## Choice Justification

- **Scalability:** as mentioned above this can handle multiple microservices using the same redacting engine.
- **Latency:** Lightweight regex and JSON parsing can effectively ensure minimal delay.
- **Cost-effectiveness:** Open-source Python implementatio nwhich means no heavy infrastructure required.
- **Ease of Integration:** Minimal changes to existing applications


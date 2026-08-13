# WindBorne
Machine Learning Infrastructure Engineer @ WindBorne — Application Challenge

1. Reconsidered Infrastructure Decision
I initially coupled model inference directly inside our primary API monolith for speed. Under load, long GPU jobs blocked main threads and crashed web instances. I pivoted to decoupling model serving into an async worker microservice using Redis/RQ and ONNX Runtime. Isolating compute-heavy workloads protected platform stability and dropped workflow failure rates.

2. Outside Core Responsibilities
Noticing researchers lost days manually troubleshooting failed cluster runs, I took the initiative to build an automated telemetry and error-classification tool using Redis queue state tracking. I was driven by empathy for users whose science was stalled by infrastructure opacity. It eliminated manual monitoring for 500+ users and saved thousands of compute hours across 10,000+ runs.

3. Evolving LLM Workflows
I shifted from relying on raw LLM prompt completions to structured function calling and Model Context Protocol (MCP) tool orchestration. I observed that unstructured outputs led to fragile JSON parsing and unhandled edge cases in automated workflows. Adding explicit schemas and deterministic tool interfaces restored runtime reliability and eliminated non-deterministic pipeline crashes.

4. Bringing Systems Structure
I bring structure through spec-first engineering: clear API contracts, strict typing, automated CI/CD checks, and actionable telemetry. When teams face chaos, I replace ad-hoc troubleshooting with explicit interfaces, failure domain isolation, and shared operational metrics. Systems thinking turns reactive firefighting into predictable, high-velocity engineering.

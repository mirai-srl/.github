# **MirAI**

**AI Governance. Human Vision.**

MirAI is a Venice-based organization engineered to orchestrate the secure transition from unstructured, vulnerable applications of artificial intelligence to governed, transparent, and accountable agentic operations. Our repositories house the infrastructure required to deploy engineered governance, mitigating systemic risks while establishing deterministic controls over stochastic Large Language Models (LLMs).

## **Architectural Mandates & Engineering Standards**

All repositories within the MirAI organization are subject to the architectural mandates outlined in the MirAI Software Engineering Standards. We prioritize static typing constraints, deterministic dependency resolution, immutable containerization, and unparalleled resilience in LLM integration.

### **Language Semantics and Frameworks**

* **Strict Static Typing:** Python 3.12+ is the mandatory execution environment. Development requires strict static typing (PEP 695, PEP 692). The use of the Any type is explicitly prohibited to ensure deterministic API contracts.  
* **Framework Determinism:** FastAPI is the established standard for async-first API development. Engineers must utilize Annotated dependencies and manage resources exclusively via the lifespan parameter.

### **Infrastructure and Pipeline Logistics**

* **Dependency Resolution:** The Rust-based uv package manager is strictly mandated to enforce deterministic lockfiles and maximum resolution speed within CI/CD pipelines.  
* **Immutable Containerization:** Deployment artifacts must be constructed using multi-stage Docker builds. The final runtime image is restricted to distroless architectures (specifically Chainguard Wolfi) executed by non-root users, functionally eliminating broad categories of supply chain vulnerabilities.  
* **Distributed CI/CD:** CircleCI serves as the designated enterprise deployment platform, leveraging Docker Layer Caching (DLC) and granular matrix parallelization to improve operational velocity.

### **Resilient LLM Orchestration**

* **Prohibition of Direct Requests:** Direct HTTP requests to AI providers are strictly forbidden to prevent systemic failures caused by upstream latency spikes and token limits.  
* **Gateway Routing:** All inference traffic must route exclusively through the Bifrost LLM Gateway.  
* **Network Resilience:** The gateway natively implements exponential backoff with jitter, stateful circuit breakers, and semantic caching layers to enforce structural reliability.

### **Quality Assurance and Observability**

* **Structured Telemetry:** System logging is fully structured via structlog, maintaining context across asynchronous boundaries and guaranteeing seamless injection into OpenTelemetry (OTel) pipelines.  
* **Automated LLM Evaluations:** The DeepEval framework is integrated directly into CI/CD pipelines to automatically score generative outputs on factual consistency, relevance, and toxicity.  
* **Property-Based Testing (PBT):** Deterministic logic must be hardened using Hypothesis to generate randomized edge-case inputs and break structural invariants.  
* **Behavioral Debt Management:** CodeScene is deployed as an automated quality gate within the PR workflow. Pull Requests containing severely degraded code or unresolved "hotspots" will be systematically halted.

### **Security Protocols**

* **Zero Trust AI:** Systems must implement strict input sanitization and delimiter isolation to prevent Prompt Injection.  
* **Agency Constraints:** Absolute Human-in-the-Loop (HITL) checkpoints are required to mitigate the risk of Excessive Agency, in strict adherence to OWASP LLM Top 10 mitigation strategies.

## **System Integration**

We collaborate with enterprises seeking to eliminate unregulated "Shadow AI" practices. By capturing user workflows within our secure, institutionally sanctioned Walled Garden environments, we realign daily operations with corporate security mandates.

To discuss integration, architectural blueprints, or the deployment of our Design System Protocol (DSP), consult the directory below.

## **Directory**

* 📧 **Email:** [info@mir-ai.it](mailto:info@mir-ai.it)  
* 🌐 **Website:** [mir-ai.it](https://mir-ai.it)  
* 📍 **Location:** Venice, Italy  
* 💼 **LinkedIn:** [MirAI on LinkedIn](https://www.linkedin.com/company/mir-ai-srl/)

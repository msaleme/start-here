# Michael Saleme — Start Here

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mikesaleme-0A66C2?logo=linkedin)](https://www.linkedin.com/in/mikesaleme/)
[![YouTube](https://img.shields.io/badge/YouTube-Michael_Saleme-FF0000?logo=youtube)](https://www.youtube.com/@michaelsaleme7028)
[![X (Twitter)](https://img.shields.io/badge/X-@mikesaleme-000000?logo=x)](https://x.com/mikesaleme)
[![PyPI](https://img.shields.io/badge/PyPI-agent--security--harness-3775A9?logo=pypi)](https://pypi.org/project/agent-security-harness/)

> I research how AI agents fail under adversarial conditions, publish the findings, and ship the tools to test for them.

---

## Published Research (5 DOIs)

I study the gap between *who an agent is* and *how it behaves* — what I call the **WHO vs. HOW problem**. Identity and authorization don't prevent an authorized agent from being manipulated into unsafe decisions.

| Paper | DOI | Key finding |
|---|---|---|
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | AI agents increase cognitive burden on operators. Here's how to measure it. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs. HOW governance gap — 77 days production data, 56 agents. |
| **Normalization of Deviance (NoD)** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | Gateway defenses provide zero protection against protocol-level attacks. |
| **Beyond Identity Governance** | [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034) | Empirical evidence: gateways miss protocol-layer attacks. The gap, formalized. |
| **Community-Driven Security** | [10.5281/zenodo.19343108](https://doi.org/10.5281/zenodo.19343108) | Scaling security testing through community contribution without degrading integrity. |

**Standards engagement:** 3 NIST submissions — CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026).

---

## Agent Security Harness

The research is implemented as an open-source testing framework: **358 executable tests across 24 modules**, covering 4 wire protocols (MCP, A2A, L402, x402).

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** — Production-validated at 97.9% pass rate (Wilson 95% CI).

```bash
pip install agent-security-harness
agent-security test mcp --url http://your-server
```

- **GitHub Action:** `uses: msaleme/red-team-blue-team-agent-fabric@v3.8`
- **MCP Server:** any AI agent can invoke security tests directly
- **AIUC-1 Prep:** maps to 15 of 20 testable certification requirements
- **CVE-2026-25253** (CVSS 8.8) — our MCP tests catch this exact supply chain vector
- **Independent validation** by DrCookies84 against live infrastructure ([AutoGen #7432](https://github.com/microsoft/autogen/discussions/7432))

---

## Featured Talks (YouTube)

Agent Fabric in Oil & Gas — Webinar Series:

| Part | Title | Link |
|------|-------|------|
| 1/4 | Introduction | [Watch](https://www.youtube.com/watch?v=X26PE2FnFOM) |
| 2/4 | Deep Dive | [Watch](https://www.youtube.com/watch?v=pWqkIqJFFG0) |
| 3/4 | Implementation | [Watch](https://www.youtube.com/watch?v=ZegJdZcR1Sk) |
| 4/4 | Conclusion | [Watch](https://www.youtube.com/watch?v=XrrWj4B8HtU) |

---

## Enterprise Architecture

15+ years building production integration systems across Oil & Gas, Energy/Utilities, and CPG.

| Repository | Description |
|---|---|
| [agent-fabric-oilgas-apis](https://github.com/msaleme/agent-fabric-oilgas-apis) | OpenAPI 3.1 specs for Agent Fabric in Oil & Gas |
| [energy-field-service-integration](https://github.com/msaleme/energy-field-service-integration) | Agentforce + ServiceNow + SAP field service |
| [energy-api-evolution](https://github.com/msaleme/energy-api-evolution) | 36 APIs for grid ops, renewables, building optimization |
| [oracle-fusion-mulesoft-best-practices](https://github.com/msaleme/oracle-fusion-mulesoft-best-practices) | Oracle Fusion Cloud integration patterns |
| [SharePointVectors](https://github.com/msaleme/SharePointVectors) | RAG pipeline: SharePoint to vectors to Salesforce |
| [cpg-promotion-analysis](https://github.com/msaleme/cpg-promotion-analysis) | Agent Fabric + Agentforce + Copilot for CPG |

---

## Executive Brief: Oil & Gas

Trusted context inside Salesforce for CEO/COO outcomes — margin resilience, execution reliability, reduced escalation load.

| Resource | Link |
|----------|------|
| Executive Site | [msaleme.github.io/oilgas-exec-site](https://msaleme.github.io/oilgas-exec-site/) |
| Book a Call | [Calendly](https://calendly.com/mspro3210/30min) |

---

## Connect

- **LinkedIn:** [linkedin.com/in/mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **X:** [x.com/mikesaleme](https://x.com/mikesaleme)
- **YouTube:** [youtube.com/@michaelsaleme7028](https://www.youtube.com/@michaelsaleme7028)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/)
- **Book time:** [Calendly](https://calendly.com/mspro3210/new-meeting) | trusted@synapseops.com

---

## License

This repository is provided for informational purposes. See individual project repositories for specific licenses.

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

The research is implemented as an open-source testing framework: **430 executable tests across 29 modules**, covering 4 wire protocols (MCP, A2A, L402, x402).

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** — Production-validated at 97.9% pass rate (Wilson 95% CI [0.943, 0.994]).

```bash
pip install agent-security-harness
agent-security test mcp --url http://your-server
```

- **GitHub Action:** `uses: msaleme/red-team-blue-team-agent-fabric@v3.8`
- **MCP Server:** any AI agent can invoke security tests directly
- **AIUC-1 Prep:** maps to 15 of 20 testable certification requirements
- **CVE-2026-25253** (CVSS 8.8) — our MCP tests catch this exact supply chain vector
- **Independent validation** by DrCookies84 against live infrastructure ([AutoGen #7432](https://github.com/microsoft/autogen/discussions/7432))
- **22 rounds** of critical evaluation, 125 issues raised, 94 fixed, 10/10 final score

### What it includes
- Attestation JSON Schema (structured security reports)
- Free MCP Security Scan (5-test, A-F grading)
- Monthly Agent Security Report pipeline
- Discord Security Scan Bot
- Real multi-trial statistical testing (Wilson CIs, NIST AI 800-2 aligned)

---

## How This Differs

Most AI security tools scan configurations or test models. This framework sends real adversarial payloads over the wire and observes what breaks. The difference between `npm audit` and a penetration test.

**Complementary to:** Invariant MCP-Scan (static scanning), Cisco MCP Scanner (YARA rules), Snyk Agent Scan (config analysis), NVIDIA Garak (model-layer).

**Unique to us:** Multi-protocol (MCP + A2A + L402 + x402), AIUC-1 mapping, MCP server mode, research backing (5 DOIs + NIST), attestation registry, production validation.

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

## Services

| Tier | What you get | Price |
|---|---|---|
| **Open Source** | 430 tests, GitHub Action, MCP server, attestation reports | Free |
| **Guardrail Audit** | Run the harness against your deployment + 30-min remediation walkthrough | $3,000 |
| **Trusted Context Sprint** | Full decision governance implementation + ongoing advisory | $18,000 |

---

## Active Community

- **Moltbook:** [Signal-Lab-Ops-Bot](https://moltbook.com/u/Signal-Lab-Ops-Bot) — 36+ comment threads on agent security
- **A2A Protocol:** Runtime attestation discussion ([#1677](https://github.com/a2aproject/A2A/discussions/1677), 11 comments)
- **AutoGen:** Security testing for multi-agent systems ([#7432](https://github.com/microsoft/autogen/discussions/7432), 22 comments)
- **AIUC-1:** Pre-certification readiness tool ([mapping](https://github.com/msaleme/red-team-blue-team-agent-fabric#aiuc-1-pre-certification-crosswalk))

---

## Connect

- **LinkedIn:** [linkedin.com/in/mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **X:** [x.com/mikesaleme](https://x.com/mikesaleme) (DLI article: 9.2K views)
- **YouTube:** [youtube.com/@michaelsaleme7028](https://www.youtube.com/@michaelsaleme7028)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/) (109 downloads/day)
- **Book time:** [Calendly](https://calendly.com/mspro3210/new-meeting) | trusted@synapseops.com

> _Signal Ops provides operational research and decision-support services only. No investment, legal, or tax advice._

---

## License

This repository is provided for informational purposes. See individual project repositories for specific licenses.

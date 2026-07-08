# Michael Saleme — Start Here

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mikesaleme-0A66C2?logo=linkedin)](https://www.linkedin.com/in/mikesaleme/)
[![YouTube](https://img.shields.io/badge/YouTube-Michael_Saleme-FF0000?logo=youtube)](https://www.youtube.com/@michaelsaleme7028)
[![X (Twitter)](https://img.shields.io/badge/X-@mikesaleme-000000?logo=x)](https://x.com/mikesaleme)
[![PyPI](https://img.shields.io/badge/PyPI-agent--security--harness-3775A9?logo=pypi)](https://pypi.org/project/agent-security-harness/)

> **Enterprise architect.** 30 years building production integration and architecture across Oil & Gas, Energy/Utilities, and CPG, since 1996. Now defining how enterprises architect a workforce of humans and AI agents.

**The thesis: Enterprise Agent Architecture.** Enterprise architecture has four domains for what the enterprise builds and runs — Business, Information, Application, Technology — with Security across them all. None describe a non-human actor that holds delegated authority, acts autonomously, and composes tools it was never explicitly granted. Agents are not a new application tier. They are a new class of actor: a workforce. They need a fifth domain. That gap is the work.

**Read the series:** [Enterprise Agent Architecture](https://msale00.substack.com) — the fifth domain, drawn one part at a time. Position paper: [doi.org/10.5281/zenodo.21105314](https://doi.org/10.5281/zenodo.21105314). Canonical home: [cognitivethoughtengine.com/eaa](https://cognitivethoughtengine.com/eaa).

**Latest:** Agent Security Harness v4.8.0 — 532 tests / 37 modules across all four layers of the agentic-payments stack (July 2026).

---

## The evidence

I do not just write about the agent workforce. I build the tools that prove how it fails and the research that measures it. The architecture rests on this, not on opinion.

### Published Research (8 DOIs)

I study the gap between *who an agent is* and *how it behaves* — what I call the **WHO vs. HOW problem**. Identity and authorization don't prevent an authorized agent from being manipulated into unsafe decisions. Together these papers form one research program: **machine-verifiable governance for autonomous systems**.

| Paper | DOI | Key finding |
|---|---|---|
| **Present vs. Provable** (methodology) | [10.5281/zenodo.21208547](https://doi.org/10.5281/zenodo.21208547) | A testable conformance methodology for delegated payment authority — can a verifier *prove* the executed payment is the one authorized? |
| **Enterprise Agent Architecture** (position paper) | [10.5281/zenodo.21105314](https://doi.org/10.5281/zenodo.21105314) | The case for a fifth architecture domain: agents are a workforce, not an application tier. |
| **Authorized but Refused** (telemetry) | [10.5281/zenodo.21263262](https://doi.org/10.5281/zenodo.21263262) | Six months, 451,163 events from a live autonomous enterprise: the governance layer refused its own *authenticated, authorized* agents 30,496 times. The measured base rate behind the WHO vs. HOW gap. |
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | AI agents increase cognitive burden on operators. Here's how to measure it. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs. HOW governance gap — 77 days production data, 56 agents. |
| **Normalization of Deviance (NoD)** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | Gateway defenses provide zero protection against protocol-level attacks. |
| **Beyond Identity Governance** | [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034) | Empirical evidence: gateways miss protocol-layer attacks. The gap, formalized. |
| **Community-Driven Security** | [10.5281/zenodo.19343108](https://doi.org/10.5281/zenodo.19343108) | Scaling security testing through community contribution without degrading integrity. |

**Standards engagement:** 3 NIST submissions — CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026). x402 conformance-vector contribution to the Linux Foundation x402 Foundation ([x402-foundation/x402#2776](https://github.com/x402-foundation/x402/pull/2776)).

### Agent Security Harness

The research is implemented as an open-source testing framework: **532 executable tests across 37 modules**, covering all four layers of the agentic-payments stack — comms (MCP, A2A), merchant journey (UCP, ACP), authorization (AP2 mandate + Visa TAP / Mastercard Agentic Tokens), and settlement (x402, L402).

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** — Production-validated at 97.9% pass rate (Wilson 95% CI [0.943, 0.994]).

```bash
pip install agent-security-harness
agent-security test mcp --url http://your-server
```

- **GitHub Action:** `uses: msaleme/red-team-blue-team-agent-fabric@v4.8.0`
- **MCP Server:** any AI agent can invoke security tests directly
- **AIUC-1 Prep:** maps to 15 of 20 testable certification requirements
- **CVE-2026-25253** (CVSS 8.8) — our MCP tests catch this exact supply chain vector
- **Independent validation** by DrCookies84 against live infrastructure ([AutoGen #7432](https://github.com/microsoft/autogen/discussions/7432))
- **22 rounds** of critical evaluation, 125 issues raised, 94 fixed, 10/10 final score

#### What it includes
- Attestation JSON Schema (structured security reports)
- Free MCP Security Scan (5-test, A-F grading)
- Monthly Agent Security Report pipeline
- Discord Security Scan Bot
- Real multi-trial statistical testing (Wilson CIs, NIST AI 800-2 aligned)

### How This Differs

Most AI security tools scan configurations or test models. This framework sends real adversarial payloads over the wire and observes what breaks. The difference between `npm audit` and a penetration test.

**Complementary to:** Invariant MCP-Scan (static scanning), Cisco MCP Scanner (YARA rules), Snyk Agent Scan (config analysis), NVIDIA Garak (model-layer).

**Unique to us:** Full-stack agentic-payments coverage (MCP + A2A + UCP/ACP + AP2 + card-network tokens + x402 + L402), AIUC-1 mapping, MCP server mode, research backing (7 DOIs + NIST + Linux Foundation x402 contribution), attestation registry, production validation.

### Reference Implementation: HRAO-E

The four-layer model is not a whitepaper waiting for a reference implementation. The reference implementation came first, and the architecture is the account of what it took to make it work.

**HRAO-E** is a live, fully-governed autonomous organization — a workforce of 50+ autonomous agents running in production under a written constitution, with six-gate enforcement, per-agent delegated authority, and audit trails. It is a working instance of all four EAA layers: **Agent / Workforce · Capability / Tool · Control Plane · Governance**.

- **The control-plane primitive, open-sourced:** [`constitutional-agent`](https://pypi.org/project/constitutional-agent/) on PyPI — the WHY-layer policy enforced at agent runtime, extracted from the system. `pip install constitutional-agent`
- **Canonical home:** [cognitivethoughtengine.com/eaa](https://cognitivethoughtengine.com/eaa) — the framework, the series, and the live proof.

**The series** — the fifth domain, published one layer at a time:

| Part | Layer | Status |
|---|---|---|
| Part 0 — The Case for a Fifth Architecture Domain | Position paper | Published — [DOI 10.5281/zenodo.21105314](https://doi.org/10.5281/zenodo.21105314) |
| Part 1 — No Box for a Non-Human Workforce | Agent / Workforce | [Published](https://cognitivethoughtengine.com/eaa/part-1) |
| Part 2 — What an Agent Can Reach ≠ What It May Touch | Capability / Tool | [Published](https://cognitivethoughtengine.com/eaa/part-2) |
| Part 3 | Control Plane | Forthcoming |
| Part 4 | Governance | Forthcoming |

**Practitioner artifacts:** [Agent Governance Maturity Model](https://cognitivethoughtengine.com/eaa/maturity-model) · [Standards Landscape](https://cognitivethoughtengine.com/eaa/standards-landscape) · [Board Questions](https://cognitivethoughtengine.com/eaa/board-questions) · [TOGAF / ArchiMate extension](https://cognitivethoughtengine.com/eaa/togaf-extension) · [The Governance Layer OpenClaw Skipped](https://cognitivethoughtengine.com/eaa/openclaw)

---

## Enterprise Architecture

30 years building production integration systems across Oil & Gas, Energy/Utilities, and CPG. MuleSoft, Salesforce, SAP, Oracle, Kafka, Azure.

| Repository | Description |
|---|---|
| [agent-fabric-oilgas-apis](https://github.com/msaleme/agent-fabric-oilgas-apis) | OpenAPI 3.1 specs for Agent Fabric in Oil & Gas |
| [energy-field-service-integration](https://github.com/msaleme/energy-field-service-integration) | Agentforce + ServiceNow + SAP field service |
| [energy-api-evolution](https://github.com/msaleme/energy-api-evolution) | 36 APIs for grid ops, renewables, building optimization |
| [oracle-fusion-mulesoft-best-practices](https://github.com/msaleme/oracle-fusion-mulesoft-best-practices) | Oracle Fusion Cloud integration patterns |
| [SharePointVectors](https://github.com/msaleme/SharePointVectors) | RAG pipeline: SharePoint to vectors to Salesforce |
| [cpg-promotion-analysis](https://github.com/msaleme/cpg-promotion-analysis) | Agent Fabric + Agentforce + Copilot for CPG |

### Featured Talks (YouTube)

Agent Fabric in Oil & Gas — Webinar Series:

| Part | Title | Link |
|------|-------|------|
| 1/4 | Introduction | [Watch](https://www.youtube.com/watch?v=X26PE2FnFOM) |
| 2/4 | Deep Dive | [Watch](https://www.youtube.com/watch?v=pWqkIqJFFG0) |
| 3/4 | Implementation | [Watch](https://www.youtube.com/watch?v=ZegJdZcR1Sk) |
| 4/4 | Conclusion | [Watch](https://www.youtube.com/watch?v=XrrWj4B8HtU) |

---

## Use It

Everything here is open source and free.

- **Run it:** `pip install agent-security-harness`
- **CI:** add the GitHub Action to your pipeline
- **MCP server mode:** let your agent invoke the tests directly
- **Free MCP Security Scan:** 5-test, A–F grading

Open to research collaboration and standards work — see Connect below.

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
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/)
- **Contact:** trusted@synapseops.com (research & collaboration)

---

## License

This repository is provided for informational purposes. See individual project repositories for specific licenses.

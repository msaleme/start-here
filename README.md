# Michael K. Saleme — Enterprise Agent Architecture & Evaluation Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mikesaleme-0A66C2?logo=linkedin)](https://www.linkedin.com/in/mikesaleme/)
[![PyPI](https://img.shields.io/badge/PyPI-agent--security--harness-3775A9?logo=pypi)](https://pypi.org/project/agent-security-harness/)
[![PyPI](https://img.shields.io/badge/PyPI-constitutional--agent-3775A9?logo=pypi)](https://pypi.org/project/constitutional-agent/)
[![PyPI](https://img.shields.io/badge/PyPI-ace--experiment--framework-3775A9?logo=pypi)](https://pypi.org/project/ace-experiment-framework/)
[![X (Twitter)](https://img.shields.io/badge/X-@mikesaleme-000000?logo=x)](https://x.com/mikesaleme)

I design decision-safe architectures and adversarial evaluation systems so enterprises can scale autonomous agents without losing control.

Across 30 years of enterprise architecture — production integration across Oil & Gas, Energy/Utilities, and CPG since 1996 — I have worked at the boundary between delegated authority, integration, governance, and operational evidence. My current work defines the architecture, implements decision governance, and tests whether the resulting controls actually hold.

| Workstream | What it proves | Start here |
|---|---|---|
| **Architect** | Autonomous agents require an enterprise-architecture domain built around delegated authority | [Enterprise Agent Architecture](https://cognitivethoughtengine.com/eaa) |
| **Evaluate** | Security and governance claims can be tested adversarially, over the wire | [Agent Security Harness](https://github.com/msaleme/red-team-blue-team-agent-fabric) |
| **Govern** | Authorized actions can be evaluated before commitment — and across sessions | [`constitutional-agent`](https://pypi.org/project/constitutional-agent/) |
| **Assess** | Empirical optimization claims can be assessed against a declared contract and retained evidence | [`ace-experiment-framework`](https://pypi.org/project/ace-experiment-framework/) |

> **One body of work:** I define the architecture, implement the governance mechanism, test protocol behavior adversarially, and assess empirical claims against retained evidence.

---

## Start here in five minutes

Four inspectable proofs, one per workstream:

1. **Read the argument** — the Enterprise Agent Architecture series, the case for a fifth architecture domain: [cognitivethoughtengine.com/eaa](https://cognitivethoughtengine.com/eaa) (Parts 0–4, complete).
2. **Run the evaluation** — send adversarial protocol traffic at an agent endpoint and grade what breaks:
   ```bash
   pip install agent-security-harness
   agent-security test mcp --url http://your-server
   ```
3. **Inspect the governance** — the runtime WHY-layer, including cross-session risk composition: `pip install constitutional-agent`. Live gate states, agent activity, and audit evidence: [cognitivethoughtengine.com/eaa](https://cognitivethoughtengine.com/eaa).
4. **Assess an experiment claim** — apply a declared experiment contract to retained trial evidence:
   ```bash
   pip install ace-experiment-framework
   ace assess experiment.yaml retained-trials.json --output ./ace-assessment
   ```

---

## The thesis: Enterprise Agent Architecture

Enterprise architecture has four domains for what the enterprise builds and runs — Business, Information, Application, Technology — with Security across them all. None describe a non-human actor that holds delegated authority, acts autonomously, and composes tools it was never explicitly granted. Agents are not a new application tier. They are a new class of actor: a workforce. They need a fifth domain. That gap is the work.

**The series — the fifth domain, one layer at a time. All four layers now published:**

| Part | Layer | Status |
|---|---|---|
| Part 0 — The Case for a Fifth Architecture Domain | Position paper | Published — [DOI 10.5281/zenodo.21105314](https://doi.org/10.5281/zenodo.21105314) |
| Part 1 — No Box for a Non-Human Workforce | Agent / Workforce | [Published](https://cognitivethoughtengine.com/eaa/part-1) |
| Part 2 — What an Agent Can Reach ≠ What It May Touch | Capability / Tool | [Published](https://cognitivethoughtengine.com/eaa/part-2) |
| Part 3 — A Rule the Runtime Doesn't Enforce Is Theater | Control Plane | [Published](https://cognitivethoughtengine.com/eaa/part-3) |
| Part 4 — When the Agent Acts, the Enterprise Answers | Governance | [Published](https://cognitivethoughtengine.com/eaa/part-4) |

**Practitioner artifacts:** [Agent Governance Maturity Model](https://cognitivethoughtengine.com/eaa/maturity-model) · [Standards Landscape](https://cognitivethoughtengine.com/eaa/standards-landscape) · [Board Questions](https://cognitivethoughtengine.com/eaa/board-questions) · [TOGAF / ArchiMate extension](https://cognitivethoughtengine.com/eaa/togaf-extension) · [The Governance Layer OpenClaw Skipped](https://cognitivethoughtengine.com/eaa/openclaw)

---

## The evidence

I do not just write about the agent workforce. I build the tools that prove how it fails and the research that measures it. The architecture rests on this, not on opinion.

**Dated claims and evidence boundaries:** [PubPoint Facts & Evidence](https://pubpoint.com/facts-evidence/) — what the counts below mean, how they're measured, and what they don't prove.

**Research map:** [the canonical reading path](https://pubpoint.com/research-map/) connects the research from decision context and enterprise architecture through runtime governance, adversarial evaluation, evidence, and the executable harness.

### Govern: `constitutional-agent`

[`constitutional-agent`](https://pypi.org/project/constitutional-agent/) on PyPI (**v0.8.0**) — the WHY-layer policy enforced at agent runtime, extracted from the reference implementation. `pip install constitutional-agent`

It evaluates authorized actions *before commitment*, and it composes risk **across sessions**: individually acceptable actions can accumulate into an unacceptable risk trajectory, so an agent that passes every per-call gate but crosses a cumulative threshold is still caught.

> A July 2026 review of selected public product documentation did not identify an equivalent cross-session aggregate-risk decision mechanism. This is a dated documentation review, not a source audit.

### Evaluate: Agent Security Harness

An open-source framework that sends real adversarial payloads over the wire and observes what breaks — covering all four layers of the agentic-payments stack: comms (MCP, A2A), merchant journey (UCP, ACP), authorization (AP2 mandate + Visa TAP / Mastercard Agentic Tokens), and settlement (x402, L402).

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** — adversarial agent-security test harness with AIUC-1 test mappings and JSON audit reports.

- **Current release:** v4.19.0 — **611 tests across 44 test-bearing modules**.
- **GitHub Action:** `uses: msaleme/red-team-blue-team-agent-fabric@v4.19.0`
- **MCP server mode:** any AI agent can invoke the tests directly.
- **AIUC-1 crosswalk:** maps to the testable certification requirements — [see the mapping](https://github.com/msaleme/red-team-blue-team-agent-fabric#aiuc-1-pre-certification-crosswalk).
- **Independently exercised** by a community user against live infrastructure ([AutoGen discussion](https://github.com/microsoft/autogen/discussions/7432)).

**How it differs.** Unlike configuration scanners, the harness sends adversarial protocol traffic and evaluates the resulting behavior. It complements static scanning and does not replace a scoped penetration test. Complementary to Invariant MCP-Scan (static), Cisco MCP Scanner (YARA), Snyk Agent Scan (config), NVIDIA Garak (model-layer). Distinct in full-stack agentic-payments coverage, AIUC-1 mapping, MCP server mode, and research backing.

### Assess: ACE Experiment Framework

**[ACE Experiment Framework](https://github.com/msaleme/ace-experiment-framework)** is available on [PyPI](https://pypi.org/project/ace-experiment-framework/). It evaluates an empirical optimization claim against a declared experiment contract and retained JSON or CSV trial evidence, producing a claim-scoped decision pack.

ACE does not run the workload, create measurements, fill in missing evidence, or turn a narrow result into a general performance claim. It helps make a result reviewable before it earns a chart. ACE’s first public reference application is [Token-Bleed R5](https://doi.org/10.5281/zenodo.22100920), a synthetic opaque-schema runtime characterization on a single local Ollama OpenAI-compatible configuration using `qwen3-coder:30b`. At 0% candidate-generator misses, its oracle-controlled bundled route changes both candidate membership and representation; it used 96.9%–97.9% fewer mean prompt tokens and higher mean F1 than verbose full context. The lexical token-efficiency/value claim was rejected under the frozen 3× rule. This is not production, customer-data, ROI, cross-model, or independently raw-reproducible evidence. See the [retained-evidence workflow](https://github.com/msaleme/ace-experiment-framework/blob/main/docs/RETAINED_EVIDENCE_WORKFLOW.md), [source release](https://github.com/msaleme/token-bleed-benchmark/releases/tag/r5-preprint-2026-08-25.1), and [pinned release commit](https://github.com/msaleme/token-bleed-benchmark/commit/c4cf83c3259c87712e21aa3eda6f6428e4d26fd4).

### Research preprints and evaluation methods

I study the gap between *who an agent is* and *how it behaves* — the **WHO vs. HOW problem**. Identity and authorization don't prevent an authorized agent from being manipulated into unsafe decisions. This is the complete current set of public Zenodo research records. They are preprints, not peer-reviewed; several are directly implemented as harness test modules. For the recommended sequence and the relationship among them, use the [research map](https://pubpoint.com/research-map/).

| Paper | DOI | Focus |
|---|---|---|
| **Enterprise Agent Architecture** | [10.5281/zenodo.21207197](https://doi.org/10.5281/zenodo.21207197) | The case for a fifth architecture domain: agents are a workforce, not an application tier. |
| **Authorized but Refused** (telemetry) | [10.5281/zenodo.21263263](https://doi.org/10.5281/zenodo.21263263) | Six months, 451,163 events from a live autonomous enterprise: the governance layer refused its own *authenticated, authorized* agents 30,496 times — the measured base rate behind the WHO vs. HOW gap. |
| **Authorized but Composed** (composition) | [10.5281/zenodo.21401743](https://doi.org/10.5281/zenodo.21401743) | Cross-session composition addresses a blind spot in per-call governance: individually acceptable actions can accumulate into an unacceptable risk trajectory. |
| **Present vs. Provable** (methodology) | [10.5281/zenodo.21262985](https://doi.org/10.5281/zenodo.21262985) | A testable conformance methodology for delegated payment authority — can a verifier *prove* the executed payment is the one authorized? |
| **Claim-Level Negative Testing** (evidence) | [10.5281/zenodo.21418702](https://doi.org/10.5281/zenodo.21418702) | Negative testing at the claim level: does a governance receipt actually prove what it asserts, or merely that a check was present? |
| **Signing Is Not Authorization** (receipts) | [10.5281/zenodo.21535453](https://doi.org/10.5281/zenodo.21535453) | A cryptographic signature proves origin, not permission — signed agent actions still require an authorization decision. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs. HOW governance gap — 77 days production data, 56 agents. |
| **Beyond Identity Governance** | [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034) | Empirical evidence that gateways miss protocol-layer attacks — the gap, formalized. |
| **Detecting Normalization of Deviance in Multi-Agent Systems** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | A graph-based approach to behavioral drift detection in multi-agent systems. |
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | DLI examines decision load in AI-augmented work — and how to measure it. |
| **AI News Evidence Pack** | [10.5281/zenodo.19826561](https://doi.org/10.5281/zenodo.19826561) | A bounded empirical evidence pack on sentiment-conditioned news-driven drift in 10 AI movers. |
| **Community-Driven Security for AI Agents** | [10.5281/zenodo.21297453](https://doi.org/10.5281/zenodo.21297453) | How an adversarial evaluation framework can accept contributions while preserving integrity and trust boundaries. |
| **Agent Security Harness** | [10.5281/zenodo.21839184](https://doi.org/10.5281/zenodo.21839184) | The executable adversarial test artifact that operationalizes the protocol and governance research. |

**Standards engagement:** 3 NIST submissions — CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026). x402 conformance-vector contribution to the Linux Foundation x402 Foundation ([x402-foundation/x402#2776](https://github.com/x402-foundation/x402/pull/2776)).

### Reference Implementation: HRAO-E

The four-layer model is not a whitepaper waiting for a reference implementation. The reference implementation came first; the architecture is the account of what it took to make it work.

HRAO-E is a live governed reference environment for constitutionally governed autonomous operations — a workforce of 50+ agents under a written constitution, with six-gate enforcement, per-agent delegated authority, and audit trails. It publishes operational status, agent activity, gate states, and audit evidence, and is a working instance of all four EAA layers: **Agent / Workforce · Capability / Tool · Control Plane · Governance**. Canonical home and live proof: [cognitivethoughtengine.com/eaa](https://cognitivethoughtengine.com/eaa).

---

## Connect

- **LinkedIn:** [linkedin.com/in/mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **X:** [x.com/mikesaleme](https://x.com/mikesaleme)
- **Research record:** [Zenodo](https://zenodo.org/search?page=1&size=20&sort=newest&q=metadata.creators.person_or_org.identifiers.identifier%3A0009-0003-6736-1900) · [ORCID 0009-0003-6736-1900](https://orcid.org/0009-0003-6736-1900)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/) · [constitutional-agent](https://pypi.org/project/constitutional-agent/) · [ace-experiment-framework](https://pypi.org/project/ace-experiment-framework/)
- **Community:** [A2A runtime attestation](https://github.com/a2aproject/A2A/discussions/1677) · [AutoGen security testing](https://github.com/microsoft/autogen/discussions/7432)
- **Correspondence:** [contact@pubpoint.com](mailto:contact@pubpoint.com?subject=Research%20correspondence) — research, speaking, and professional correspondence.

---

## License

This repository is provided for informational purposes. See individual project repositories for specific licenses.

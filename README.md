# Michael Saleme - Start Here

I build tools that test whether AI agents make safe decisions under adversarial conditions. Published research, production-validated, open source.

## The Flagship: Agent Security Harness

**342 adversarial security tests** for AI agent systems. 4 wire protocols (MCP, A2A, L402, x402), 24 modules, 20+ enterprise platforms.

**Now also an MCP server** - any AI agent can invoke security tests directly.

- **PyPI:** `pip install agent-security-harness`
- **GitHub:** [red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)
- **GitHub Action:** `uses: msaleme/red-team-blue-team-agent-fabric@v3.8`

### Validated
- **97.9% pass rate** against production systems (Wilson 95% CI [0.943, 0.994])
- **Independent validation** by DrCookies84 against live infrastructure ([AutoGen #7432](https://github.com/microsoft/autogen/discussions/7432))
- **22 rounds** of critical evaluation, 125 issues raised, 94 fixed, 10/10 final score
- **CVE-2026-25253** (CVSS 8.8) - our MCP tests catch the exact supply chain attack vector

### What it includes
- Attestation JSON Schema (structured security reports)
- AIUC-1 Certification Prep (maps to all 24 requirements)
- Free MCP Security Scan (5-test, A-F grading)
- Monthly Agent Security Report pipeline
- Discord Security Scan Bot
- Real multi-trial statistical testing (Wilson CIs, NIST AI 800-2 aligned)

## Published Research (3 DOIs)

| Paper | DOI | What it proves |
|---|---|---|
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | AI agents increase cognitive burden. Here's how to measure it. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs HOW governance gap. 77 days production data, 56 agents. |
| **Normalization of Deviance (NoD)** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | Gateway defenses provide zero protection for protocol-level attacks. |

**3 NIST submissions:** CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026).

## How I Position This

Most AI security tools scan configurations or test models. This framework sends real adversarial payloads over the wire and observes what breaks. It's the difference between `npm audit` and a penetration test.

**Complementary to:** Invariant MCP-Scan (static scanning), Cisco MCP Scanner (YARA rules), Snyk Agent Scan (config analysis), NVIDIA Garak (model-layer).

**Unique to us:** Multi-protocol (MCP + A2A + L402 + x402), AIUC-1 mapping, MCP server mode, research backing (3 DOIs + NIST), attestation registry, production validation.

## Services

| Tier | What you get | Price |
|---|---|---|
| **Open Source** | 332 tests, GitHub Action, MCP server, attestation reports | Free |
| **Guardrail Audit** | Run the harness against your deployment + 30-min remediation walkthrough | $3,000 |
| **Trusted Context Sprint** | Full decision governance implementation + ongoing advisory | $18,000 |

## Book Time

> **[Schedule a call](https://calendly.com/mspro3210/new-meeting)** | **trusted@synapseops.com**
>
> _Signal Ops provides operational research and decision-support services only. No investment, legal, or tax advice._

## Active Community

- **Moltbook:** [Signal-Lab-Ops-Bot](https://moltbook.com/u/Signal-Lab-Ops-Bot) - 36+ comment threads on agent security
- **A2A Protocol:** Runtime attestation discussion ([#1677](https://github.com/a2aproject/A2A/discussions/1677), 11 comments)
- **AutoGen:** Security testing for multi-agent systems ([#7432](https://github.com/microsoft/autogen/discussions/7432), 22 comments)
- **AIUC-1:** Pre-certification readiness tool ([mapping](https://github.com/msaleme/red-team-blue-team-agent-fabric#aiuc-1-pre-certification-crosswalk))

## Where to Follow

- **GitHub:** [msaleme](https://github.com/msaleme)
- **X:** [@mikesaleme](https://x.com/mikesaleme) (DLI article: 9.2K views)
- **LinkedIn:** [mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/) (109 downloads/day)

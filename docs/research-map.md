# Michael K. Saleme - Research Map

## Core proposition

Enterprise agent systems need governance that evaluates more than who is authorized. It must also assess how an authorized agent behaves, what evidence supports an action, and how risk compounds across sessions. This body of work moves from decision context to enterprise architecture, runtime governance, and executable adversarial evaluation.

## Scope and evidence status

Every link below resolves to a public Zenodo record. The individual records are labelled as preprints, reports, working papers, or software where applicable. They are not peer-reviewed unless a record explicitly says otherwise.

## Canonical reading path

### Context: why decision load matters

**Decision Load Index: A Conceptual Framework for Measuring Cognitive Burden in Knowledge Work**  
<https://doi.org/10.5281/zenodo.18217577>

An optional entry point for the human and organizational context: unresolved decisions, inputs, commitments, and scope create cognitive burden. It frames why decision quality and operating context matter before the discussion turns to autonomous systems.

### 1. The governance problem: authorization is not behavior

**Constitutional Self-Governance for Autonomous AI Agents: A Framework Observed in 77 Days of Production**  
<https://doi.org/10.5281/zenodo.19162104>

Introduces the WHO vs. HOW gap: authentication, access control, and audit logging are necessary, but do not by themselves constrain an agent's decisions under changing conditions.

### 2. The architecture: agents are a workforce, not an application feature

**Enterprise Agent Architecture: The Case for a Fifth Architecture Domain for the Agentic Enterprise**  
<https://doi.org/10.5281/zenodo.21207197>

Places autonomous agents within enterprise architecture as actors with delegated authority, capabilities, control-plane dependencies, and governance obligations.

### 3. The operational control: systems must be able to refuse authorized actions

**Authorized but Refused: Six Months of Runtime Governance Telemetry from an Autonomous Enterprise**  
<https://doi.org/10.5281/zenodo.21263263>

Provides the operational-telemetry layer: governance is credible only when a running system can constrain, record, and explain decisions made under granted authority.

### 4. The runtime risk: individually authorized actions can compound

**Authorized but Composed: Cross-Session Risk Composition as an Agent-Governance Control**  
<https://doi.org/10.5281/zenodo.21401743>

Explains why per-call approval is insufficient when sequences of individually acceptable actions accumulate across sessions.

### 5. The observable failure mode: behavioral drift and normalization of deviance

**Detecting Normalization of Deviance in Multi-Agent Systems: Empirical Evidence for Graph-Based Behavioral Drift Detection**  
<https://doi.org/10.5281/zenodo.19195516>

Extends runtime governance into monitoring: gradual behavioral drift can be missed by stateless or threshold-only monitoring.

### 6. The evaluation boundary: identity controls do not test protocol behavior

**Beyond Identity Governance: A Protocol-Level Security Testing Framework for Multi-Agent AI Systems**  
<https://doi.org/10.5281/zenodo.19343034>

Moves from architecture and monitoring to adversarial evaluation across MCP, A2A, L402, and x402. The question is how an agent system behaves when those protocol boundaries receive hostile traffic.

### 7. The evidence standard: a receipt must prove what it claims

**Present vs. Provable: A Conformance-Testing Methodology for the Authority Layer of Agentic Payments**  
<https://doi.org/10.5281/zenodo.21262985>

**Claim-Level Negative Testing for Agent-Governance Evidence**  
<https://doi.org/10.5281/zenodo.21418702>

**Signing Is Not Authorization: Claim-Level Negative Vectors for Agent-Payment Receipts**  
<https://doi.org/10.5281/zenodo.21535453>

These works define the evidence layer. Signatures, receipts, and checks do not alone establish that an executed action was authorized or that an artifact supports the claim it makes.

### 8. The executable implementation

**Agent Security Harness**  
<https://doi.org/10.5281/zenodo.21839184>

The practical evaluation instrument: executable adversarial security tests that operationalize protocol and governance claims.

### 9. The ecosystem model

**Community-Driven Security for AI Agents: Evolution of an Adversarial Testing Framework**  
<https://doi.org/10.5281/zenodo.21297453>

Sets out an approach for accepting adversarial-evaluation contributions while preserving integrity and trust boundaries. This is version 1.1, which corrects a CVE misattribution in version 1.0.

## Supporting research

**AI News Evidence Pack: Sentiment-Conditioned Tests of News-Driven Drift in 10 AI Movers (2024-2026)**  
<https://doi.org/10.5281/zenodo.19826561>

A bounded empirical evidence pack. It supports the broader interest in observable behavior and evidence discipline, but is not a prerequisite for the agent-governance path.

## Public positioning

> I research how autonomous agents can fail after authorization is granted, then build the architecture, governance mechanisms, and adversarial tests needed to make their behavior and evidence more inspectable.

## Placement guidance

- **Zenodo:** archival record, DOI source, and version history.
- **ORCID:** curated identity and discovery record that links to canonical DOIs.
- **PubPoint:** canonical public version of this full map and its supporting context.
- **GitHub start-here:** a concise entry point that links here and to the relevant implementation.
- **Substack:** use individual sections as reader-guide or essay-sequence material, with each piece adapted to the audience rather than duplicated mechanically.
- **Technical channels:** point to the relevant implementation or test artifact, not the complete map every time.

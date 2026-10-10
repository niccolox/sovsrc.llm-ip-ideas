# Super Sovereign Source LLM IP

**An AI laboratory and language model platform built around Super Intellectual Property: rights, ideas, contributions and influences, with shared stewardship and compensation.**

Super Sovereign Source LLM IP (`sovsrc.llm`) aims to develop capable language models while recognizing and rewarding the people whose works, ideas, contributions and influences make them possible. Its **Super Intellectual Property (SIP)** framework connects scoped permissions, AI-assisted attribution, voluntary contributor syndicates and auditable revenue sharing.

SIP expands what the project records, recognizes and rewards through evidence and agreements. It is a proposed framework, not an assertion that a new statutory IP right already exists. Ownership, permission, credit, governance and payment are recorded separately.

**Status: specification stage.** This workspace contains project and implementation specifications. The application, trained model and production payment system have not been implemented.

## Documentation

| Document | Purpose |
| --- | --- |
| [Current project and implementation specification, v0.3](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) | SIP framework, syndicate model, requirements, architecture, data records, APIs, milestones and acceptance tests. |
| [Original project specification, v0.1](docs/origin/Sovereign_Source_AI_Project_Specification_v0_1.docx) | Historical source for laboratory strategy, proposed economics, governance and policy references. |

## Super Intellectual Property and syndicates

A syndicate is a voluntary group that administers selected works, ideas, contributions and influences under an accepted charter. Members choose what to enroll and what authority to delegate. A syndicate can negotiate permitted uses, preserve individual credit and administer agreed revenue splits; joining does not automatically transfer ownership or license a member's work.

| SIP subject | Recognition and participation |
| --- | --- |
| IP and source works | Reviewed rights, scoped licenses and evidence of use. |
| Ideas and research | Concrete proposals, adoption records and agreed rewards. |
| Contributions | Implementation, improvements, prompts, workflows, curation and evaluation. |
| Influences | Documented acknowledgments and lineage; credit-only unless compensation is expressly agreed. |
| Combined and derivative work | Preserved upstream obligations and separately recorded new contributions. |

AI helps identify references, possible duplicates, contribution relationships and missing credit. Authorized reviewers accept or correct those proposals. A similarity score cannot establish ownership, permission or payment eligibility. Member mandates, contribution-specific splits, exit terms and disputes are versioned and auditable.

## Architecture

The initial product is a research assistant using an approved corpus. It checks permissions, supplies evidence for answers and records eligible contribution use. An independently trained foundation model is a later research milestone.

```mermaid
flowchart TD
    subgraph Intake[Contributions and permissions]
        A[Works, ideas, contributions and influences]
        B[Rights review, consent and agreements]
        C[Approved assets and adopted contributions]
        Y[Syndicate charters, mandates and splits]
        Y --> B
        A --> B --> C
    end

    subgraph Pilot[Local research assistant pilot]
        U[Customer request]
        P[Tenant, region and permission checks]
        D[Authorized retrieval and prompt templates]
        M[Model adapter]
        V[Output validation and final permission check]
        E[Persist attribution receipt and usage event]
        O[Deliver answer with sources]
        U --> P --> D --> M --> V --> E --> O
    end

    subgraph Accounting[Contributor accounting]
        R[Eligible revenue records]
        L[Royalty calculation and audit ledger]
        S[Member statements and simulated settlement]
        R --> L --> S
    end

    subgraph Research[Later model development]
        T[Approved training manifest]
        F[Training and independent evaluation]
        K[Released model checkpoint]
        T --> F --> K
    end

    C --> D
    A --> G[AI proposals and reviewed attribution graph]
    G --> E
    C -->|Agreement terms| L
    E -->|Contract eligible use| L
    C -.->|Separate training permission| T
    K -.->|Future model integration| M
```

Permission checks and financial decisions operate outside the model. A citation identifies supporting evidence; it does not establish ownership or prove which training example caused an answer. Usage records must be durable before metered content is delivered.

## Core commitments

- **Permission before use:** record the allowed purpose, recipients, territory and duration for each asset.
- **Honest attribution:** distinguish verified quotations, retrieved support, recorded reuse, training participation, acknowledged influence and estimated influence.
- **Super Intellectual Property:** recognize documented ideas, contributions and acknowledged influences alongside formal IP rights, with a clear basis for every claim.
- **Voluntary syndicates:** require accepted charters and scoped mandates; preserve individual credit, agreed benefit shares and accrued obligations through member exit.
- **Explicit contribution agreements:** compensate accepted use without treating every submitted idea or ordinary prompt as an automatic royalty claim.
- **Private conversations by default:** shared training and contribution enrollment require separate consent.
- **Reproducible payments:** preserve event history, calculate exact amounts and prevent duplicate settlement.
- **Sovereign deployment controls:** specify data location, administrative access, keys, model versions and update authority.
- **Review and appeal:** support disputed ownership, missing credit, payment corrections and permission revocation.

## Proposed contributor economy

The draft allocates **20% of eligible collected revenue** to a contributor pool. Eligible revenue deducts refunds, chargebacks, sales taxes and directly charged payment processing fees; it does not deduct general operating expenses.

| Track | Share of contributor pool | Proposed allocation basis |
| --- | --- | --- |
| Training and licensed corpus | 60% | Approved, deduplicated training exposure and predefined quality weights. |
| Prompt and workflow reuse | 20% | Verified eligible paid executions of accepted versions. |
| Ideas, contributions and influences | 20% | Agreed adoption points supported by reviewed evidence; influence shares require explicit agreements. |

These are proposed contractual terms, not existing statutory royalty rates. Minimum guarantees, retrieval fees and bounties follow their own agreements. The [royalty engine specification](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md#12-royalty-engine) defines offsets, rounding, reserves, disputes and settlement examples.

Syndicates distribute a contribution's allocation using accepted beneficiary shares within these existing tracks. For example, a `$2,000` allocation split 60/25/15 pays `$1,200` to an idea contributor, `$500` to an implementation contributor and `$300` to an acknowledged influence contributor. Credit-only influences receive acknowledgment without payment. The default administration fee is zero, and membership in multiple syndicates cannot multiply the same entitlement.

## Implementation roadmap

| Milestone | Deliverable |
| --- | --- |
| M0 | Local setup, domain model, migrations and synthetic fixtures. |
| M1 | Private submissions, grants, syndicate charters and mandates, accepted agreements and splits, and adoption. |
| M2 | Research assistant with authorized retrieval, reviewed contribution and influence links, and source receipts. |
| M3 | Usage capture, royalty calculations, member allocations, statements and simulated payments. |
| M4 | Disputes, attribution corrections, revocation, member exit, dissolution, exports and end-to-end verification. |
| M5 | Commercial integrations, signed licenses and independent review. |
| M6 | An owned research model trained on admitted data. |
| M7 | A frontier candidate that passes capability, rights and safety evaluations. |

The first implementation targets **M0–M4**, using synthetic fixtures and deterministic model and payment adapters. Real payouts, production deployment and large training runs are subsequent work.

## Start with Codex

Open the [implementation specification](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) and use this prompt:

```text
Read applicable repository instructions and docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md.
Implement milestones M0–M4 as a working local Super Sovereign Source LLM IP pilot.

Reuse existing repository patterns. Use synthetic fixtures and deterministic
model and payment adapters by default. Keep sources/ read-only.

Implement Super Intellectual Property with voluntary syndicates, scoped
mandates, reviewed contribution and influence links, and accepted member splits.
Verify permissions, tenant isolation, honest attribution, durable usage capture,
exact royalties, member exit, revocation and disputes. Document setup and report
verification results and remaining production dependencies.
```

The proposed greenfield stack is React and TypeScript, a Python API, PostgreSQL, private object storage and one background worker. The implementation should reuse suitable existing infrastructure. Setup commands will be documented when the application exists.

## Completion criteria

The local pilot is complete when individual contributors and syndicate members can submit material, accept scoped terms, obtain reviewed attribution and share eligible proceeds through reproducible statements and simulated settlement. The demonstration includes a licensed work, an adopted idea, an agreed influence share and a separate credit-only influence.

Verification must also cover denied access, tenant and member privacy, mandate withdrawal during generation, unsupported AI attribution, duplicate claims across portfolios, financial rounding, disputed payments, member exit and worker recovery. See the [verification requirements](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md#16-verification-requirements) and [definition of done](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md#19-local-definition-of-done).

## Policy and governance

The specification includes a [Trump administration policy mapping](docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md#18-trump-administration-policy-mapping), with primary references for Super Intelligence terminology, creator compensation, frontier security, procurement and international deployment. The reference date is October 10, 2026; applicability must be reviewed before production claims or procurement.

Project commitments are distinct from government policy and legal requirements. Frontier capability, complete source provenance and production readiness must be supported by evaluation evidence.

## Working in this workspace

The project directory is `/home/niccolox/Projects/sovsrc.llm`. The original project specification is preserved under `docs/origin/`; the implementation specification is under `docs/`. Follow applicable `AGENTS.md` instructions when adding implementation work. Any synced files under `sources/` remain read-only references.

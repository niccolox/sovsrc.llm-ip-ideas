# Minions and Community Compute for Sovereign Source

**Research date:** 13 October 2026. **Status:** analysis and proposed experiment; no implementation or deployment performed.

**Recommendation:** evaluate a small, managed compute pool for asynchronous work after the core permission and accounting flows function. Keep the existing production serving and model-training plans. The opportunity is to let a syndicate administer both knowledge contributions and computing services, with separate agreements and earnings.

Brian Cardarella's [linked X post](https://x.com/bcardarella/status/2110039458032607486) says the subject overlaps with earlier DockYard research. It points to the paper assessed below. His statement is a claim about earlier work, not evidence by itself of copying, model training on that work, or an LLM transferring the idea.

## What the paper establishes

Apple-affiliated researchers published *Minions: A Dynamic and Distributed Virtual GPU Cloud Built on Idle Apple Silicon Devices* on 9 October 2026. It distributes independent inference subtasks across Macs through a server, PostgreSQL, object storage, executors and a recovery watchdog. Workloads include embeddings and Ollama completions; workers pull tasks and interrupted work is reassigned. Team preferences can fall back to a global queue. Reported queue waits improve from hours to minutes. Training is future work. [Paper, sections 2–5](https://arxiv.org/html/2610.12970v1).

The evaluation gives operational observations without a reproducible hardware, model, throughput or cost breakdown. Its “zero” infrastructure-cost description should not become a total-cost assumption. The reviewed paper links no implementation repository. Its publication license is not a commercial software license. It describes distributed execution with shared coordination, rather than one pooled GPU memory space. [Paper and publication metadata](https://arxiv.org/abs/2610.12970).

## Where it fits the platform

The following are Sovereign Source design proposals, not capabilities demonstrated by the paper.

| Workload | Proposed fit | Conditions for use |
| --- | --- | --- |
| Batch embeddings and corpus enrichment | Strong first experiment | Admit the exact model and source versions; restrict which hosts may process them; validate results. |
| Offline evaluation and attribution suggestions | Useful secondary experiment | Keep held-out evaluations separate; treat suggested influences as unverified until reviewed. |
| Synthetic training examples | Conditional later use | Independently approve teacher, input and output-use rights; preserve generation lineage and quality review. |
| Interactive customer answers | Keep on reserved capacity initially | Intermittent devices need measured availability and latency before supporting a customer commitment. |
| Frontier pretraining or Nemotron Ultra adaptation | Retain the separate research infrastructure | Do not replace the existing memory, networking and checkpoint plan with an aggregate count of Macs. |

For an early product, completing corpus preparation overnight may be more valuable than promising instant inference on volunteer devices. A professional association or research group with existing managed machines offers a clearer starting point than an unrestricted public network.

This does not resolve model selection. US hardware or a US operator does not establish US-only learned lineage, permission to train a competing model, or rights to a corpus. Every model, tokenizer, embedding artifact and synthetic teacher still goes through the [existing admission process](MODEL_SELECTION_RESEARCH_SUMMARY.md).

## Integration with the existing stack

Extend the [production system plan](PRODUCTION_SYSTEM_PLAN.md) with one optional execution adapter. Keep policy and money in the existing core.

| Existing component | Proposed responsibility |
| --- | --- |
| Rust and Axum | Authenticate devices, authorize each task lease, enforce tenant and region policy, accept validated results and commit financial events. |
| PostgreSQL | Store authoritative task state, lease generation, attempts, permission decisions, result references and separate payables. |
| Python and Pydantic | Define task envelopes, validate payloads and run bounded local executors. |
| Pydantic AI | Coordinate approved model calls or propose attribution; never select beneficiaries or override routing policy. |
| Prefect | Orchestrate corpus preparation and evaluation batches, reconcile progress and publish operational status. |
| Approved object storage | Hold encrypted, versioned inputs and attempt-specific outputs within the customer's permitted jurisdiction. |

Choose one authority for work ownership: the Axum/PostgreSQL service. Prefect should submit and monitor these batches without independently reclaiming the same device leases. The device agent receives neither database access nor payment credentials.

Each task envelope should bind the tenant, source versions, permission version, allowed purpose, eligible processor pool, model and runtime digests, budget and deadline. Device preferences may narrow this eligible set; they must never expand it. Empty eligibility means wait or return a controlled failure, rather than borrow a host from another syndicate.

For Ollama experiments, configure local-only operation, retain a loopback listener and limit the executor's outbound destinations. Ollama documents `OLLAMA_NO_CLOUD=1` and its default `127.0.0.1:11434` binding. Confirm the running configuration rather than assuming installation implies local processing. [Ollama FAQ](https://docs.ollama.com/faq).

## Sovereignty and execution safety

Start with organization-managed devices and public or synthetic inputs. Add confidential material only when the customer authorizes the specific processor pool and its device controls have been assessed. An owner or administrator of an ordinary worker machine may inspect data processed there. Transport encryption and a separate database do not remove that exposure.

Model sovereignty as several explicit decisions: device ownership, administrator access, geography, storage location, model provenance and contractual processing authority. A geographically dispersed pool can increase supplier choice while making residency harder to establish. Record verified deployment locations; a host's self-declared region is insufficient for a strict residency promise.

Use narrowly scoped input access and disable access when a task expires. For permissions requiring immediate revocation, prefer an access-checking gateway over a download URL that remains valid until its expiry. Recheck authorization before releasing a result. Download cancellation or cache deletion cannot prove that an untrusted recipient never retained a copy.

Approve executable task types and runtime packages centrally. Customer documents are untrusted data and must not become executable instructions or gain access to local files. Device owners need clear resource limits, pause controls and visibility into the work they accept.

## Correctness before compensation

A safe implementation must handle a worker that disappears, loses its lease and later returns. Give each lease a monotonically increasing generation number. Store output under the attempt identity and accept it only if the generation and permission decision remain current. A late worker must not overwrite the accepted result or trigger another settlement.

Use short database transactions to claim work; do not hold a row lock while inference runs. PostgreSQL documents `SKIP LOCKED` as useful for consumers of queue-like tables while warning that it provides an inconsistent view for general queries. It can help select available tasks, but application lease expiry, stale-result rejection and payment idempotency remain separate responsibilities. [PostgreSQL SELECT documentation](https://www.postgresql.org/docs/current/sql-select.html).

Signed device receipts identify a reporting device, not the correctness of its answer. Validate shapes, versions and task-specific invariants; use sampled recomputation or independent review when justified by the workload. Measure validation overhead. Arbitrary LLM responses cannot be reliably verified by matching hashes when generation is nondeterministic.

## Separate markets for knowledge and compute

Sovereign Source could offer a governed community service in which members contribute knowledge, computing capacity, or both. The platform's value would be coordinating permissions, reliable work and understandable earnings.

| Contribution | Evidence | Proposed payment basis |
| --- | --- | --- |
| Licensed content | Admitted version, accepted grant and qualifying use | Existing content agreement or adopted creator-rewards terms. |
| Computing service | Authorized attempt, accepted result and approved rate schedule | A defined work-unit fee or separately contracted capacity payment. |
| Evaluation and curation | Accepted review or correction | A commission or service agreement. |
| Idea or documented influence | Reviewed relationship and accepted beneficiary agreement | Agreed participation; credit-only where no payment is adopted. |

Do not pay simply for self-reported GPU hours, tokens or heartbeat messages. Those quantities can reward waste or fabricated activity. Agree how retries, reserved availability, validation failures and interrupted work are paid before jobs begin. Replayed messages must not create duplicate liabilities, while a genuine additional use must retain any payment obligation its content agreement specifies.

Compute suppliers need their own budget. Under an agreement adopting the existing 20% creator pool, compute expense does not reduce eligible collected revenue or silently consume the corpus allocation. Preserve the [specified economics](SOVEREIGN_SOURCE_AI_CODEX_SPEC.md#proposed-economics) and price the combined service to cover both obligations.

An initial commercial offer could be a managed inference pool for one research community, charged through a platform subscription and clearly priced jobs. Revenue depends on useful, reliable output. Avoid promising passive income to every device owner before measuring paid demand and administration costs.

## What the post means for attribution

DockYard has documented earlier work on Nx and the Elixir machine-learning ecosystem, including Brian Cardarella's involvement in initiating that work. Its 2023 history supports that narrower claim, but does not establish a causal relationship to this specific Apple paper. [DockYard's Nx history](https://dockyard.com/blog/2023/11/08/three-years-of-nx-growing-the-machine-learning-ecosystem).

SIP should be able to register an earlier research artifact, preserve its version and date evidence, and invite a comparison of concrete design elements. Useful evidence could include dated repositories, publications, demonstrations and acknowledged references. Private evidence requires controlled access and the contributor's consent.

Keep distinct statuses for a claimant's assertion, evidence of earlier work, possible similarity, acknowledged influence and an agreed payment. Earlier documentation alone does not demonstrate another team's access or dependence. A timestamp or hash cannot settle authorship or independent invention. AI can help locate similarities; reviewers should preserve uncertainty and allow a response before making a public attribution claim.

For Sovereign Source's own implementation, credit this paper for the design inspiration actually used. Credit an earlier DockYard artifact if it is identified and consulted. The evidence available here does not establish a royalty obligation between the organizations.

## A bounded pilot

Use three to five consenting, managed Macs, one admitted model artifact and a fixed batch of public or synthetic inputs. If no artifact meets the project's admission requirements, exercise task ownership and settlement with a deterministic adapter before model execution.

Compare the same work with an approved central worker. Record startup time, completed work per hour, p95 completion time, failures, owner interruptions and result quality. Calculate cost per accepted task including contributor payments, electricity, storage, network transfer, administration, validation and retries. Report both incremental cash cost and allocated hardware cost; existing hardware still has an opportunity cost.

Acceptance requires no cross-tenant task delivery, rejection of stale attempts, successful permission-change handling and correct settlement under duplicate messages. Commercial adoption additionally requires acceptable output quality and either lower cost at the required deadline or a measurable capacity benefit. Set those targets before running the experiment; none has been demonstrated for Sovereign Source yet.

The strategic addition is an optional, governed compute service beside the knowledge marketplace. Prioritize permissioned content, reliable attribution and accounting first. Community compute becomes valuable when it helps that product deliver more useful work on terms both customers and contributors accept.

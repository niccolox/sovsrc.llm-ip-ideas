# Distillation as a Service for frontier labs and sovereign AI

**Project:** Super Sovereign Source LLM IP

**Research date:** October 14, 2026

**Scope:** Commercial distillation services, managed training platforms and self-hosted alternatives, assessed for independent deployment, source rights and content rewards.

**For Sovereign Source, the strongest direction is a portable distillation workflow using an expressly permitted teacher, admitted source material and an exportable student.** Evaluate Fireworks and Thinking Machines Lab's Tinker for managed experiments, Together AI as a training-platform alternative, and NVIDIA's documented distillation tooling for an environment controlled by the project. A suitable training provider does not automatically supply a suitable teacher or prove the student's ancestry.

AWS Bedrock offers a more packaged workflow for customers staying within its supported model and deployment paths. OpenAI documents distillation into its hosted fine-tuning service. These can be useful application-optimization products, but they do not establish an unrestricted route to an independently distributed competitor. Google documents exportable open-model distillation, although its currently listed teachers fail this project's no-Chinese-model requirement. [AWS workflow](https://docs.aws.amazon.com/bedrock/latest/userguide/model-distillation.html), [OpenAI fine-tuning guide](https://developers.openai.com/api/docs/guides/supervised-fine-tuning), [Google open-model tuning](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/tuning/open-model-tuning).

The commercial opportunity is to combine model specialization with **documented permission, portable artifacts, evaluated capability and contributor settlement**. That is a proposed Sovereign Source service, rather than a capability demonstrated by every vendor below. The [ten data brokers report](FRONTIER_AI_DATA_BROKERS_TOP_10_REPORT.md) covers the upstream supply side.

## What DaaS means here

Distillation as a Service transfers selected behavior from a teacher model into a student through a managed or assisted workflow. A complete service should identify the permitted teacher, generate or ingest examples, validate them, train the student, evaluate it and deliver a deployable artifact or endpoint.

Several related techniques have different requirements:

| Method | Learning signal | Commercial implication |
| --- | --- | --- |
| Response distillation | Teacher-generated answers become supervised examples. | Works with authorized text outputs; usually requires a generation pipeline plus supervised fine-tuning. |
| Logit distillation | Student learns from teacher token probabilities rather than only selected answers. | Requires appropriate teacher access, tokenizer treatment and training support; an ordinary answer API may be insufficient. |
| On-policy distillation | Teacher feedback is applied to sequences or trajectories produced by the student. | Adds sampling, scoring and iterative training costs. |
| Teacher-assisted reward learning | Teacher supplies preferences or scores used to improve the student. | Scores and critiques also need provenance and permission; changing the signal does not remove its origin. |

The foundational knowledge-distillation paper describes transfer from a larger model or ensemble into a smaller model. NVIDIA documents logit-based training, and Tinker publishes supervised and on-policy recipes. These establish mechanisms, not guaranteed performance for a proposed commercial deployment. [Hinton, Vinyals and Dean, 2015](https://arxiv.org/abs/1503.02531), [NVIDIA distillation](https://docs.nvidia.com/nemo-framework/user-guide/26.02/model-optimization/distillation/distillation.html), [Tinker recipes](https://tinker-docs.thinkingmachines.ai/cookbook/recipes/distillation/).

Ordinary fine-tuning is distillation only when a teacher supplies the relevant learning signal. Quantization changes numerical representation; retrieval supplies information at answer time. Neither is itself teacher-to-student learning. Most offerings below customize already pretrained students. Buying distillation does not mean training an independent foundation from random initialization, and success on one workflow does not demonstrate general frontier capability.

## Side by side provider comparison

This is a procurement landscape, not a market-share ranking. **Packaged** means the provider documents an integrated distillation workflow; **programmable** means the customer supplies important parts of the loop; **specialist** means a narrower platform or custom engagement; **self-hosted** means the customer operates the software. Model support, contract and region must be checked for the exact order.

| Provider | Offering and maturity evidence | Teacher and student scope | Export and sovereignty | Best use and principal limitation |
| --- | --- | --- | --- | --- |
| **Amazon Bedrock** | **Packaged:** documented model-distillation jobs, synthesis and student tuning. | Current table lists Amazon Nova and Meta Llama pairs. **Anthropic distillation is explicitly unavailable.** | Bedrock custom-model deployment is documented; independent weight export is not established by these pages. Check cross-region inference. | Quick AWS-contained pilot. Do not assume arbitrary teachers, arbitrary students or on-premises export. [Workflow](https://docs.aws.amazon.com/bedrock/latest/userguide/model-distillation.html), [supported pairs](https://docs.aws.amazon.com/bedrock/latest/userguide/prequisites-model-distillation.html) |
| **Google Cloud** | **Packaged:** open-model distillation through the GenAI SDK on Gemini Enterprise Agent Platform, formerly Vertex AI. | Listed teachers are DeepSeek, GLM, Kimi and Qwen; students include Gemma and Qwen. This is not a general Gemini-teacher grant. | Documentation explicitly permits exporting the tuned model from Cloud Storage. The global endpoint may choose a processing region. | Technically portable, but the listed teacher path fails this project's model-origin screen. [Product documentation](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/tuning/open-model-tuning) |
| **OpenAI** | **Packaged components:** documented larger-model outputs to smaller-model supervised fine-tuning. | Supported OpenAI teachers and hosted fine-tunable students; exact availability is model-specific. | Documented result is an API model ID; no downloadable weights are offered in this workflow. | Optimize an OpenAI application. Independent competing-model training requires a different permission basis. [Guide](https://developers.openai.com/api/docs/guides/supervised-fine-tuning) |
| **Fireworks AI** | **Programmable:** Training API explicitly includes distillation; also offers managed jobs and Fireworks Lab engagements. | Customer-controlled loop on supported models; serverless and dedicated modes differ. | Advertises checkpoint export. Prove that the delivered base or adapter can run independently; managed training still uses provider infrastructure. | Strong managed prototype candidate. Do not confuse the distillation API with a one-click managed distillation product. [Training offering](https://fireworks.ai/training) |
| **Thinking Machines Lab Tinker** | **Programmable:** published distillation recipes and training/sampling primitives. | Recipe and live catalog constrain available pairs; examples are not an approved SIP model selection. | Documents local checkpoint download and adapter merging. Data processing remains hosted during training. | Strong research-control candidate with an explicit export path. Audit teacher/student licenses and current catalog. [Recipes](https://tinker-docs.thinkingmachines.ai/cookbook/recipes/distillation/), [weights](https://tinker-docs.thinkingmachines.ai/tutorials/core-concepts/weights/) |
| **Together AI** | **Programmable adjacent platform:** current Custom Training offers SFT, RL and custom losses; RL is labeled beta. | Bring authorized teacher-generated data and use supported open-model training. | Published fine-tuning offering supports checkpoint download; confirm the selected Custom Training mode's deliverables. | Managed training alternative. Scope generation, verification and settlement separately rather than assuming a turnkey DaaS service. [Custom Training](https://www.together.ai/custom-training), [checkpoint portability](https://www.together.ai/blog/introducing-fine-tuning-platform) |
| **NVIDIA NeMo and Model Optimizer** | **Self-hosted tooling:** documented knowledge-distillation training. Older Microservices product has a sunset notice. | Requires compatible checkpoints and parallelism; support must be verified for the proposed model. | Customer-operated training can retain artifacts and data within a chosen boundary. Support and infrastructure are separate purchases. | Best architectural fit for strict operational control, with more engineering responsibility. [Framework guide](https://docs.nvidia.com/nemo-framework/user-guide/26.02/model-optimization/distillation/distillation.html), [Microservices notice](https://archive.docs.nvidia.com/nemo/microservices/25.12.0/fine-tune/tutorials/distillation-customization-job.html) |
| **Arcee AI** | **Specialist/custom-model lead:** published distillation work, DistillKit and enterprise-model offerings. | Historical SuperNova describes Llama distillation; do not generalize that ancestry to every Arcee model. | Enterprise materials describe deployment in customer environments; require an artifact and support schedule for the actual engagement. | Consider an engineering-led custom-model bid. Evidence of a technique is not a current standard SaaS package. [SuperNova research](https://www.arcee.ai/blog/arcee-supernova-training-pipeline-and-model-composition), [enterprise direction](https://www.arcee.ai/blog/arcee-ai-announces-new-strategic-funding-round) |
| **distil labs** | **Specialist platform:** documented teacher evaluation, synthetic data, student training and evaluation. | Includes gpt-oss teachers and Llama, LFM and Gemma students, alongside Chinese-origin models. Recommended examples use GLM/Qwen. | Targets deployable small models; confirm downloadable artifacts, operator jurisdiction and processing region in the agreement. | Evaluate narrow tasks using an explicitly selected permitted pair; the default tutorial is not a lineage approval. [Workflow](https://www.distillabs.ai/docs/reference/platform/), [model catalog](https://www.distillabs.ai/docs/reference/supported-models/) |

These vendors are not all equivalent SaaS businesses. NVIDIA's tooling and Arcee's research/custom-model route are included because sovereign buyers may value operational control more than a fully hosted experience. No reviewed offering establishes a ready-made SIP syndicate ledger and upstream influence-reward system.

## Current product changes that matter

AWS's current prerequisite page expressly removes Anthropic distillation without a restoration date. It still contains a lower-page note mentioning Claude deployment; the explicit availability warning and supported-pairs table should govern procurement, rather than that residual note or earlier launch blogs. [Current prerequisites](https://docs.aws.amazon.com/bedrock/latest/userguide/prequisites-model-distillation.html).

NVIDIA's archived Microservices tutorial states a sunset date of **October 1, 2026**. Its successor link redirects to **NeMo Helix**, whose current description is an agent improvement control plane. Do not infer a drop-in replacement for the old distillation API. Evaluate the documented Framework/Model Optimizer route and obtain a current support position before specifying a managed NVIDIA service. [Sunset notice](https://archive.docs.nvidia.com/nemo/microservices/25.12.0/fine-tune/tutorials/distillation-customization-job.html), [Helix repository](https://github.com/NVIDIA-NeMo/nemo-helix).

Tinker's catalog marks several older Llama models retired in June 2026 while listing gpt-oss models. Pin active model identifiers and preserve checkpoint export before relying on a provider for repeated training. A recipe's historical model name is not evidence of present availability. [Models and retirement table](https://tinker-docs.thinkingmachines.ai/tinker/models/models_and_pricing/).

## Frontier model permissions

The permission to operate a training platform and the permission to learn from a teacher are separate. A DaaS supplier's API compatibility, invoice or promise of model ownership does not override the teacher contract.

| Teacher route | Published boundary | Handling for Sovereign Source |
| --- | --- | --- |
| OpenAI hosted services | Services Agreement 3.3 restricts competing-model development using outputs, subject to defined exceptions. These include certain non-distributed classification models and customization within listed OpenAI services. | Do not treat hosted distillation as permission to publish a competing independent LLM. Obtain a governing exception for the actual workflow. [Agreement](https://openai.com/policies/services-agreement/) |
| Anthropic commercial services | Section D.4 restricts using the service to build competing products, including competing models, unless expressly approved. | Require express approval; a broker or cloud intermediary does not create an exception. [Commercial terms](https://www.anthropic.com/legal/commercial-terms) |
| Gemini through Google Cloud | Section 17 distinguishes competitive use, model substitution and extraction; the distillation exception concerns Modified Google Models. Third-party offerings have separate terms. | Review the exact service and model. The open-model product above is not blanket permission to distill Gemini into a competitor. [Cloud terms](https://cloud.google.com/terms/service-terms) |
| Downloadable teacher operated independently | The artifact license and applicable usage policies govern this route, plus the rights in prompts and other source material. | Candidate route, subject to release-specific rights, provenance and lineage review. See the [model decision](MODEL_SELECTION_RESEARCH_SUMMARY.md). |
| Proprietary teacher licensed by negotiated agreement | The owner can grant a defined commercial distillation right within its authority. | Specify model/version, artifacts, students, territory, hosting, redistribution, term and continuing rights after service termination. |

These are product and contract findings, not a judgment on enforceability. The project's [OpenAI](OPENAI_COMPETING_MODEL_RESTRICTIONS_RESEARCH.md) and [Gemini](GEMINI_COMMERCIAL_RESTRICTIONS_RESEARCH.md) reports provide deeper route-specific analysis. Publicly downloadable gpt-oss is a separate licensing route from hosted ChatGPT, not a way to relabel previously restricted ChatGPT outputs.

Distillation also **does not establish a clean-room defense or erase source ancestry**. If a teacher or student has learned from excluded sources, a smaller student does not automatically satisfy a no-lineage requirement. Regional hosting, US corporate origin, rights in source works and learned model lineage are four different properties.

The existing selection of **Nemotron 3 Ultra** remains unchanged. Its recorded Qwen/DeepSeek ancestry conflict also remains. This report does not approve it as a teacher for a strict no-Chinese-lineage track, or certify any alternative teacher as fully traceable. See the [consolidated model decision](MODEL_SELECTION_RESEARCH_SUMMARY.md) and [architecture](SOLUTION_ARCHITECTURE.md).

## The market opportunity

Commercial DaaS currently overlaps with fine-tuning, synthetic-data production, managed GPU training and model-development consulting. The reviewed public material does not support a defensible standalone DaaS revenue total or market-share ranking. A generic AI-training market estimate would mix materially different products.

| Customer | Job to be done | Likely purchasing model | Evidence needed to win |
| --- | --- | --- | --- |
| Frontier lab owning its teacher | Produce cheaper model tiers, transfer specialized behavior, or distribute licensed domain students. | Compute consumption, engineering engagement or controlled teacher license. | Research flexibility, throughput, isolation and measured transfer quality. |
| Enterprise using frontier APIs | Reduce the cost and latency of a stable, repeated workflow. | Paid pilot followed by training and operational fees. | Total cost per successful task, regression coverage and a viable fallback. |
| Sovereign operator | Retain control of weights, processing, updates and deployment. | Private-environment delivery plus support and periodic retraining. | Independent execution, jurisdiction and access evidence, complete artifact delivery. |
| Professional or community syndicate | Convert authorized knowledge into a specialist model while preserving contributor interests. | Source license, expert-work fees and agreed recurring participation. | Source and beneficiary records, transparent receipts and correction rights. |

These buying patterns are strategic inferences from the documented offerings, not announced contracts with Sovereign Source. For frontier labs, distilling their own teacher can be an internal efficiency strategy or a licensed distribution product. For independent builders, the teacher permission is often a gating commercial input. The business must price both situations explicitly.

A useful proposed offer is **a licensed domain model with a portable evidence package**: approved sources, teacher permissions, student artifacts, independent evaluation and contributor statements. Competing only on synthetic token generation would leave Sovereign Source exposed to larger training platforms. Its intended differentiation is the trustworthy relationship between knowledge contributors and model operators.

## Pricing and unit economics

Compare the whole pipeline:

`project cost = source licenses + expert work + teacher inference + validation + student training + evaluation + delivery`

`ongoing cost = serving + fallbacks + monitoring + retraining + support + agreed contributor payments`

AWS warns that its data-synthesis process can add teacher calls. Google separately bills teacher inference, student training and related services. Fireworks distinguishes token-billed serverless training from time-billed dedicated capacity. Tinker publishes separate prefill, sampling and training prices. These are different units; a low training-token rate is not an all-inclusive distillation quote. [AWS billing behavior](https://docs.aws.amazon.com/bedrock/latest/userguide/model-distillation.html), [Google billing](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/tuning/open-model-tuning), [Fireworks modes](https://fireworks.ai/training), [Tinker pricing](https://tinker-docs.thinkingmachines.ai/tinker/models/models_and_pricing/).

For a concrete public reference, Tinker's listed standard-context gpt-oss-20b rates are **$0.18 per million prefill tokens, $0.45 per million sampled tokens and $0.396 per million training tokens**, checked October 14, 2026. Checkpoint storage is listed separately at **$0.10 per GB per month**. These are service-unit prices, not a project budget or proof that this model meets SIP requirements. [Published pricing](https://tinker-docs.thinkingmachines.ai/tinker/models/models_and_pricing/).

### Illustrative break even calculation

Assume one million requests per month, a teacher-only baseline of $0.02 per request, and a student costing $0.002 for every request. Assume 10% still need a teacher fallback at the same teacher cost, plus $1,000 monthly incremental monitoring and support. All numbers are hypothetical.

| Item | Monthly cost |
| --- | ---: |
| Teacher-only baseline | $20,000 |
| Student on all requests | $2,000 |
| Teacher fallback on 10% | $2,000 |
| Additional monitoring and support | $1,000 |
| New operating total | $5,000 |
| Savings before additional royalties or retraining | $15,000 |

A $30,000 initial project would recover its cost in two months **only under these assumptions and equivalent acceptable quality**. Additional contributor payments, refresh costs, retries, idle capacity and higher fallback rates reduce savings. If the student is less accurate or traffic is low, distillation may not pay back at all.

For actual bids, compare against the cheapest acceptable current solution, which may be a smaller existing model, retrieval, caching or rules. Measure completed work at the required quality rather than tokens alone. Include rollout generation and teacher scoring in on-policy training estimates.

## Sovereignty acceptance criteria

A private endpoint is not sufficient evidence of sovereign control. Evaluate five independent dimensions:

| Dimension | Required evidence for the proposed service |
| --- | --- |
| Model control | Exportable weights or adapter plus accessible base; tokenizer, configuration, license and offline serving demonstration. |
| Data control | Permitted processing regions, subprocessors, retention/deletion, approved source uses and isolation between customers. |
| Operational control | Customer-controlled deployment credentials, keys, update approval, rollback and a documented exit procedure. |
| Legal and commercial control | Teacher and data rights covering training, serving, distribution and continued use; no incompatible exclusivity or withdrawal terms. |
| Economic and provenance control | Portable source IDs, accepted grants, transformation records, beneficiary schedules and settlement evidence. |

For a national deployment, teacher generation can be the point at which sensitive material leaves the jurisdiction. Local student inference does not retrospectively make that training pipeline domestic. Where external processing is forbidden, operate an approved teacher inside the required boundary or use authorized human-authored examples.

## Content rewards through distillation

The provenance chain should remain available after compression:

`source asset and grant → teacher generation event → reviewed example → training manifest → student checkpoint → eligible use and settlement`

Record known relationships without claiming to reconstruct every influence embedded in a teacher. A citation supports an answer; a manifest records training participation; neither establishes the causal contribution of a source to every output. Distillation should preserve accepted credit and payment obligations, not manufacture certainty about influence.

Proposed payment handling:

- Pay source owners or syndicates for the permitted generation and training uses defined in their agreement.
- Pay experts for original tasks, validation and corrections under their own terms.
- Record teacher-service fees separately; a teacher bill does not replace source compensation.
- Carry agreed beneficiary obligations to eligible student use. Do not multiply rewards simply because one example was paraphrased into many synthetic examples.
- Keep flat licensing fees, minimum guarantees and recurring shares separately identifiable, with offsets only when agreed.

SIP's existing creator-pool proposal remains unchanged. No new automatic royalty is created by this report. A supplier must not promise per-answer payments unless the agreement defines measurable qualifying use and the system can record it.

## Proposed implementation and pilot

The existing stack can support a vendor-neutral workflow:

| Component | Proposed responsibility |
| --- | --- |
| Python and Pydantic | Validate teacher permissions, source grants, example provenance, model identifiers and release manifests. |
| Pydantic AI | Orchestrate permitted generation and structured review; keep binding admission decisions outside model judgment. |
| Prefect | Run generation, quality checks, training, evaluation and export with reproducible job records. |
| Rust and Axum | Enforce tenant, purpose and region policy; authorize artifact release and record eligible use. |
| PostgreSQL | Preserve grants, source relationships, checkpoint lineage, beneficiary schedules and exact settlement records. |
| Training adapter | Connect the approved job to Fireworks, Tinker, Together or a self-hosted implementation without changing the rights ledger. |

Require a release package containing the model or adapter, required base, tokenizer, configuration, deployment instructions, permitted source manifest, generation records, evaluation results and license notices. Deliver private evidence to authorized reviewers without disclosing confidential sources publicly.

The first pilot should address one bounded task, such as extracting structured facts from an approved scientific corpus with supporting references. Compare an existing small model, an approved teacher and the distilled student on a held-out set authored independently of generation. Measure task accuracy, citation support, unsupported attribution, permission leakage, latency, total cost and fallback rate. Include source-family separation and realistic adversarial inputs. Keep retrieval for changing facts and evidence where needed.

Proceed in four steps:

1. **Establish permissions and the baseline.** Choose a source collection, exact teacher/student pair, independent test set and customer deployment boundary.
2. **Run a bounded paid experiment.** Contract a spending ceiling and acceptance rules. Generate only through approved routes and retain rejected-example reasons.
3. **Test portability and rewards.** Run the exported artifact in a second environment and reconcile simulated contributor statements against the manifest.
4. **Decide on production.** Expand only if quality, privacy, lineage, economics and exit tests pass. Otherwise retain the baseline or commission more original expert data.

For the strict no-Chinese-lineage track, unresolved ancestry is an unresolved admission gate. Neither a US vendor nor an open license is sufficient certification. The initial recommendation is therefore to **choose a controllable workflow first, approve the exact models second, and make rights and rewards part of the delivered product**.

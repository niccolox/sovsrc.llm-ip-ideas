# Meta Muse for Sovereign Source AI

Research date: 12 October 2026. Scope: Meta's Muse Wonder 1.0, Wonder Full 1.0, Spark 1.3 and the separately downloadable Muse Glimmer-30B.

**Recommendation: assess Wonder and Spark as external evaluation baselines. Add self-hosted Glimmer to the conditional model and teacher shortlist. None currently qualifies as a verified foundation under sovsrc's strict provenance and no-Chinese-model-lineage requirements.**

Muse is the family name; Wonder and Spark are models within it. For Super Sovereign Source LLM IP, the decisive questions are permission to develop a competing model, control over deployment, evidence about upstream training sources, and enforceable creator agreements. Model capability alone cannot establish these properties.

## Models and access

| Offering | Access and advertised context | Potential role in sovsrc |
| --- | --- | --- |
| Muse Wonder 1.0, `muse-wonder-1.0` | Meta API and Muse Code; 1 million tokens | Quality baseline for research and complex agent tasks. |
| Muse Wonder Full 1.0, `muse-wonder-full-1.0` | Muse Code subscription access; 1 million tokens | Interactive assessment; not an established API integration target. |
| Muse Spark 1.3, `muse-spark-1.3` | Meta API, Standard tier; 1 million tokens | Lower-cost evaluation baseline. |
| Muse Spark 1.3 Contributor, `muse-spark-1.3-contributor` | Meta API with training-use permission for Meta | Exclude from the default route for contributor material. |
| Muse Glimmer-30B | Downloadable weights and local inference | Conditional adaptation or synthetic-data teacher candidate. |

Meta positions Wonder for demanding coding and agent work and Spark for agentic workloads at lower cost. These roles are evaluation hypotheses, not results from a sovsrc benchmark. [Wonder product information](https://dev.meta.ai/models/muse-wonder), [Spark product information](https://dev.meta.ai/models/muse-spark), [Glimmer product information](https://dev.meta.ai/models/muse-glimmer).

Wonder's published evaluations use differing harnesses and reporting methods; some comparisons use a common internal harness while others preserve external configurations. Its SWE-Marathon comparison is not a controlled common-harness comparison. Do not transfer Wonder Full results to the Wonder API model or infer reliable source attribution from coding performance. [Wonder model card](https://research.meta.ai/static/muse-wonder-model-card/).

## Commercial permission to develop a competing model

Meta's API terms, updated 9 October 2026, §10.1(ix), require written authorization for competing-model training, distillation and dataset collection; the wording extends to competing products and services. Evaluation of one's own systems is expressly excepted. Section 10.1(xi) separately restricts public benchmarks that market competitors. Section 1 preserves separate self-hosted licenses. [Meta Model API terms](https://dev.meta.ai/legal/terms-of-service).

For sovsrc, the proposed agreement should cover demonstrations, preference labels, model critiques, derived datasets, commercial release and redistribution. Define whether results only measure performance or feed an optimization loop: those are different purposes. Keep evaluation artifacts outside training admission until their reuse rights are established.

Resolve Muse Code assistance for competing-product implementation in that agreement too. This analysis does not treat subscription access as permission for every downstream purpose.

## Pricing and the Contributor exchange

Published USD prices per million tokens, as of the research date:

| API model | Uncached input | Cached input | Output |
| --- | ---: | ---: | ---: |
| Wonder 1.0 | $4.00 | $0.20 | $20.00 |
| Spark 1.3 Standard | $1.25 | $0.15 | $4.25 |
| Spark 1.3 Contributor | $0.10 | $0.002 | $0.20 |

Wonder Full has subscription access rather than an advertised API token price. For an illustrative one million uncached input tokens plus one million output tokens, the API totals are $24.00, $5.50 and $0.30 respectively, excluding tools, taxes and additional calls. Actual cost per accepted answer requires measurement. [Meta pricing](https://dev.meta.ai/docs/pricing-rate-limits).

Contributor pricing exchanges lower fees for permission to use submitted content and responses to train and improve Meta systems. The pricing program does not establish source-by-source attribution, cash royalties, syndicate distributions or upstream influence payments. That makes it a useful economic comparison for SIP, but an inadequate substitute for SIP Creator Rewards. [Pricing and Contributor explanation](https://dev.meta.ai/docs/pricing-rate-limits).

Standard pricing excludes using request content to train Meta models. Establish retention and processing requirements separately before sending private material. [Standard service description](https://dev.meta.ai/docs/pricing-rate-limits).

**Muse Code subscriptions default to Contributor treatment regardless of the selected model; Standard treatment requires changing the account setting.** Wonder's Standard designation alone therefore does not establish subscription privacy. [Model designation policy](https://dev.meta.ai/legal/geographic-use-policy).

Sovsrc should route contributor material only according to the creator's accepted permissions. A retrieval license for answering a customer's question should not be treated as authorization to contribute that material to another lab's training. A discount received by the platform also needs an explicit agreement before it can count as compensation to the source creator.

## Glimmer is the relevant downloadable Meta alternative

Glimmer has approximately 29.6 billion parameters, accepts text and images, and generates text. Its model card explicitly lists synthetic-data generation for downstream model development as an intended use. It is **distilled from Muse Spark**. Its disclosed training sources include public material, third parties and Meta products and services; the card does not provide a complete source-license and teacher inventory. [Glimmer model card](https://huggingface.co/meta-models/Muse-Glimmer-30B).

The downloaded release carries Apache 2.0 and a published usage policy. Neither reviewed document contains the API's competing-model-training prohibition. This supports a conditional local teacher or adaptation route, subject to the policy, applicable rights and license obligations. The Apache grant does not certify that every upstream training item was licensed, nor does it create royalties for source creators. [Actual license file](https://huggingface.co/meta-models/Muse-Glimmer-30B/raw/main/LICENSE), [published usage policy](https://huggingface.co/meta-models/Muse-Glimmer-30B/raw/main/USAGE_POLICY.md).

Its Spark distillation ancestry makes a complete lineage audit necessary before adopting it under the strict project requirement. A US developer does not establish the absence of Chinese-developed teachers, filters or synthetic-data dependencies. There is no basis here to certify that absence, or to assert a specific undisclosed Chinese dependency.

Assess the exact weights, tokenizer, vision encoder, quantization and serving components separately. Record immutable revisions and hashes, source licenses, disclosed teachers, usage conditions and unresolved ancestry. Passing a capability benchmark cannot close those provenance questions.

## Ten decision parameters

This table applies the evidence above to sovsrc's requirements. “Unverified” means that adoption requires additional evidence.

| Parameter | Wonder and Wonder Full | Spark 1.3 | Self-hosted Glimmer |
| --- | --- | --- | --- |
| 1. US developer | Meta | Meta | Meta |
| 2. No Chinese model lineage | Unverified | Unverified | Unverified; Spark ancestry disclosed |
| 3. Independent deployment | Hosted access; no weight grant established | Hosted access; no weight grant established | Downloadable weights |
| 4. Competing-model teacher rights | Written authorization required | Written authorization required | Plausible under separate release terms |
| 5. Auditable training-source permissions | Insufficient for SIP certification | Insufficient for SIP certification | Broad categories disclosed; incomplete inventory |
| 6. Control over submitted content | Check subscription setting and contract | Standard versus Contributor is material | Local processing can be controlled by sovsrc |
| 7. Capability fit | Complex research and agent evaluation candidate | Lower-cost agent evaluation candidate | Must pass local quality evaluations |
| 8. Attribution evidence | Requires external source records | Requires external source records | Requires external source records |
| 9. Creator rewards and syndicates | Must be implemented by sovsrc | Contributor discount does not supply this | Must be implemented by sovsrc |
| 10. Adoption decision | Evaluation candidate | Standard-tier evaluation candidate | Conditional base or teacher candidate |

“Clean room” should describe a documented development process with admissible inputs and controlled access. Selecting any of these models alone cannot establish independent creation or clear third-party rights. Ideas and influences can receive contractual credit and agreed compensation within SIP without asserting new statutory ownership rights.

## Integration and acceptance criteria

Retain the existing [solution architecture](SOLUTION_ARCHITECTURE.md). Python and Pydantic should validate evidence and model responses; Pydantic AI can coordinate permitted model calls. Prefect should manage admission and evaluation workflows. Rust/Axum and PostgreSQL should remain responsible for permissions, accepted attribution records, syndicate shares and the financial ledger.

For a Meta evaluation, use the following sequence:

1. **Establish access rights.** Record the exact model, route, account setting and applicable terms. Obtain written permission for any hosted use beyond the established evaluation scope.
2. **Admit evaluation inputs.** Use synthetic fixtures or material with permission for the selected processor and purpose. Include disputed ownership, indirect influence, revoked access and conflicting syndicate mandates.
3. **Measure answer quality.** Test source-supported claims, accurate quotations, unsupported-credit rates, abstention and resistance to instructions embedded in retrieved content. Track latency and cost per accepted answer.
4. **Validate creator accounting independently.** Require durable receipts for eligible use. Test beneficiary splits, duplicate events, rounding and corrections without letting a model invent ownership or payout amounts.
5. **Qualify any local teacher separately.** For Glimmer, review the pinned release and lineage, constrain generation to admitted sources, check outputs for unsupported claims and copied material, and record the teacher and source manifests with each admitted example.

Reward contracts should specify whether they pay for corpus participation, recorded retrieval, accepted reuse or another measurable event. A generated citation or model-estimated influence score does not prove that a particular pretraining item caused an answer.

## Effect on the current model decision

Keep the [consolidated recommendation](MODEL_SELECTION_RESEARCH_SUMMARY.md): KL3M for a provenance-focused pilot and newly initialized OLMo-core for a future foundation trained on SIP-admitted material. Add Glimmer alongside self-hosted gpt-oss as a **conditional teacher candidate**, with its distinct license and Spark ancestry recorded. Neither receives a strict-lineage approval from this analysis.

Wonder and Spark are useful comparison points for quality and operating cost. This research does not change the recorded Nemotron 3 Ultra selection, resolve Ultra's disclosed ancestry conflict, or authorize a deployment or training run.

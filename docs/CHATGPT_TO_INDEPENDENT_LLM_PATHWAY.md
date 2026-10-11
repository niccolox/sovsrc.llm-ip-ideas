# From ChatGPT to an independent LLM with content rewards

**Project:** Super Sovereign Source LLM IP

**Reviewed:** October 10, 2026

**Scope:** Proposed US-oriented development and licensing pathway. Actual account agreements, jurisdiction and intended uses require project-specific legal review. No permission, contract amendment or clearance has been obtained by writing this document.

**Recommended direction:** develop Sovereign Source with independently authorized tools, model materials and contributions. If continued ChatGPT assistance is important to developing the competing model, first negotiate explicit permission covering that work. Creator rewards should come from accepted contribution agreements and recorded use.

The achievable objective is a model whose development and operation do not depend on restricted ChatGPT outputs, or whose relevant uses are expressly authorized. “Free from ChatGPT commercial restrictions” cannot responsibly mean free from every license, third-party right or contractual obligation. This research document is itself AI-assisted output; it is an issue map for independent verification, not an exemption or a certified independent model specification.

## 1. The contractual boundary

OpenAI's individual terms prohibit using output to develop competing models. They also preserve the user's rights in original inputs. Having discussed your own idea with ChatGPT does not, by itself, assign that idea to OpenAI or turn all of your independently authored work into OpenAI output. Generated additions and transformations need separate assessment. Owning output is distinct from having permission for a particular use. [Terms of Use, effective January 1, 2026](https://openai.com/policies/terms-of-use/).

The business agreement has a competing-model restriction in section 3.3(e). Its defined exception concerns certain internal categorization/classification/organization models and customization through specified OpenAI services; it is not general permission to release a competing LLM. Section 2.2 permits API-powered customer applications, and section 16.2 gives Order Forms priority in conflicts. Buying Business, Enterprise or API access is therefore not, by itself, a waiver. [Services Agreement, effective January 1, 2026](https://openai.com/policies/services-agreement/).

**Interpretation requiring review:** “develop” can reach further than inserting generated answers into a training dataset. Do not assume training code, architecture advice, synthetic labels, evaluator judgments or optimization feedback are exempt. The code-generation provisions provide no express competing-model exemption for Codex and recognize that third-party code licenses can apply. [Service Terms, updated September 29, 2026](https://openai.com/policies/service-terms/).

The [dedicated OpenAI report](OPENAI_COMPETING_MODEL_RESTRICTIONS_RESEARCH.md) analyzes the restrictions and commercial exposure. This pathway neither finds that earlier project work breached a contract nor establishes that a restriction is enforceable in every jurisdiction.

## 2. Route A: obtain explicit permission for ChatGPT-assisted development

Use this route if the business needs generated model-development work, including existing material. Prepare a workflow-specific request for an authorized OpenAI contracting representative. A support reply, sales statement or assistant answer should not substitute for a signed provision resolving the relevant restrictions and document precedence.

The proposed negotiation brief should cover:

| Term to resolve | Requested scope |
| --- | --- |
| Competing product | Name Sovereign Source, its intended market, independent hosting, commercial API and any downloadable weights. |
| Covered assistance | Specify design, code, training examples, annotations, evaluation, model selection, feedback and any distillation separately. |
| Existing material | Identify earlier accounts, dates and artifacts; request express treatment of those materials and any prior use. Do not assume retroactive permission. |
| Participants | Cover the actual company, authorized staff, contractors and data suppliers; specify downstream recipients. |
| Continuing rights | Resolve commercialization, modification, redistribution, duration, termination and rights in completed derivatives. |
| Remaining obligations | Identify retained restrictions, third-party rights, security duties, notices, fees, remedies and contractual priority. |

**Decision:** proceed only within the executed permission's scope. If the requested permission is unavailable or too narrow, use Route B for the affected work. Negotiation is an option, not a promise that OpenAI offers this arrangement.

## 3. Route B: establish independent development

This is the recommended procurement strategy when freedom from a hosted provider's competing-model restriction is essential. The steps below are proposed evidence and sourcing controls, not a legal safe harbor.

1. **Inventory existing assistance.** Preserve relevant versions and origin records. Separate human originals, third-party material and generated contributions. Identify which outputs have actually informed model work; do not limit the review to copied text.
2. **Select independently licensed development tools.** Require permission for the intended commercial model development and relevant output uses. For hosted tools, review service terms as well as the underlying model license. A model available to download can have different terms from a hosted endpoint serving it.
3. **Obtain model-development inputs independently.** Commission original expert work; obtain code and documentation from their original, appropriately licensed repositories; license datasets and evaluations for the actual use. Preserve source and authorship records. Public accessibility alone is not the project's admission standard.
4. **Review prior exposure honestly.** Where generated architecture, code or advice has materially shaped the work, have counsel assess authorization, replacement or independent redevelopment. A separate team may help establish facts where appropriate; it does not automatically erase prior use or transfer restrictions away.
5. **Admit each artifact for a specified purpose.** Review training, adaptation, evaluation, retrieval, quotation, external processing and distribution separately. Include synthetic-data teachers, judges, embeddings, filters and subcontractors in the evidence chain.
6. **Record a release decision.** Keep the permitted materials, excluded materials, accepted licenses, unresolved issues and approved release form together. The decision should be reproducible from records rather than an unsupported claim that the model is “clean.”

Human paraphrasing, removing provider names, changing file formats, paying a reseller or passing output through another model does not establish independence. Canceling a subscription is also not evidence of permission for earlier output reuse. The pathway should preserve truthful provenance, not obscure it.

Business writing and application software, such as contributor onboarding or billing, can be assessed separately from model development. That distinction needs to reflect actual use: describing a training-data generator as an application does not settle the contractual question. Keep any permitted ChatGPT-assisted application work within its assessed scope.

## 4. Treatment of this repository and earlier chats

The following are review instructions, not findings about the origin or admissibility of every existing file.

| Material | Proposed treatment |
| --- | --- |
| Your original content-rewards idea, notes and independently authored inputs | Preserve originals and evidence of authorship; assess any separate employer, collaborator or third-party obligations. Do not discard them merely because they appeared in a prompt. |
| `docs/CHAT_HISTORY.md` and generated research/specification text | Retain as historical and review material; no automatic training, evaluation or model-development clearance. Separate human inputs, generated replies and quotations. |
| Model recipes, architecture decisions, code, labels or evaluation feedback produced through restricted services | Identify actual use and dependencies; obtain scoped permission or an independently assessed replacement. Human editing alone is insufficient evidence. |
| Links to papers, libraries, datasets and model cards | Obtain the original artifact and its applicable terms directly. A reference is not a license, and independently obtaining it does not resolve unrelated prior output use. |
| Mixed files and supplier deliverables | Record contributions and terms at a useful level of detail; keep unresolved portions out of the proposed use until reviewed. |

A useful artifact record contains: identifier and digest; author or supplier; source location and acquisition date; source model/service where relevant; account and terms version; original inputs; generated transformations; intended uses and recipients; permission evidence; notices; credit/reward agreement; reviewer and decision date. Hashes establish version identity, not ownership or legal permission.

## 5. The Nemotron 3 Ultra route

The selected model remains `nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16`. NVIDIA currently identifies **OpenMDW-1.1** as its download license and discloses Qwen and DeepSeek sources. It therefore does not satisfy the earlier no-Qwen requirement; US vendor identity does not establish exclusively US model ancestry. Preserve that unresolved requirement in the release decision. [NVIDIA's model card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16).

OpenMDW-1.1 grants broad rights in the supplied model materials and imposes no restrictions on using, modifying or sharing their outputs. Distribution requires the license and applicable notices. It includes a litigation-triggered termination condition, disclaims warranties and assigns third-party rights clearance to the user. These are materially different terms from hosted ChatGPT, but they are not a guarantee that every input or output is cleared. [OpenMDW-1.1 license text linked by NVIDIA](https://raw.githubusercontent.com/OpenMDW/OpenMDW/refs/heads/main/1.1/LICENSE.OpenMDW-1.1).

**Proposed implementation choice:** use the independently licensed download, or a provider contract that expressly supports the intended development. Review the exact checkpoint, tokenizer, code, dependencies, training additions and deployment terms. Pin their versions and preserve notices. Independently licensed synthetic generation can be considered only after checking input rights and output provenance; it must not become a relay for restricted ChatGPT material.

Describe the resulting system as a **Nemotron derivative with reviewed added data and content rewards for enrolled contributions**. Do not describe all of Nemotron's historical training as SIP-authorized or compensated. A foundation model with entirely admitted training provenance would require a separate corpus and development program.

## 6. Make content rewards enforceable and measurable

Under US copyright law, ideas, scientific methods and mathematical principles are distinct from protected expression describing them. SIP can recognize and contractually reward a research contribution without asserting copyright ownership of the underlying idea. Other rights, including patents and confidentiality, need separate treatment where relevant. [Copyright Office Circular 31](https://www.copyright.gov/circs/circ31.pdf).

Use four explicit reward mechanisms:

| Mechanism | Evidence and earning event | What the record establishes |
| --- | --- | --- |
| Licensed retrieval | An authorized source version was supplied to a response under an accepted, deduplicated usage agreement. | Recorded source use; citation can support inspection but does not prove every assertion or causal influence. |
| Training participation | A licensed contribution entered an identified corpus/run under a fixed fee, minimum guarantee or agreed pool policy. | Participation and agreed compensation, not a precise share of each later answer's value. |
| Commission or adopted contribution | An expert deliverable or proposed idea met agreed acceptance/adoption criteria. | Contractual eligibility even where the idea itself is not copyrightable. |
| Upstream influence share | Identified beneficiaries and affected parties accepted a supported relationship and split. | An agreed allocation; resemblance or an AI suggestion alone creates no debt. |

Start with licensed retrieval and commissioned contributions, then introduce training participation when admission and accounting are proven. Do not present current attribution estimates as a reliable method of tracing every generated token to its historical training sources.

For each real agreement, specify the parties and authority; contribution versions; permitted uses, processors and release modes; attribution placement; qualifying events; revenue basis or fee; deductions; beneficiary shares; payment dates; corrections; withdrawal; surviving rights; and disputes. Separate permission to train from permission to retrieve or distribute source data. A publisher, employer, coauthor or syndicate may control relevant rights; an uploader's assertion alone is insufficient.

For example, an agreement allocating **$2,000** to a contribution with a **60/25/15** beneficiary split and zero administration fee pays **$1,200 / $500 / $300**. The upstream influence receives its $300 because the parties accepted that split. A separate acknowledgment can remain credit-only. This mirrors the existing [marketplace terms](../licenses/SYNDICATE-MARKETPLACE-TERMS-0.1.md); it establishes no new default rate.

Treat earned amounts as obligations under the agreement. Provide itemized statements, fraud review, narrowly scoped holds, independent appeals and payment reconciliation. Do not promise that withdrawing a work instantly removes its influence from distributed weights; agree future-use, retention and remediation terms before training.

## 7. Preserve open-source freedoms and the commons

Keep software/model licensing separate from optional paid services and contribution agreements. OSI's software definition requires free redistribution without a royalty for that sale and permits commercial fields of use. A compulsory marketplace enrollment or payment condition for exercising those software freedoms would conflict with that design. This is not a certification that a model or the custom SIP draft meets every open-source criterion. [Open Source Definition](https://opensource.org/osd).

The repository's [SS-SIP draft](../licenses/SS-SIP-0.1.md) is not OSI-approved and is not automatically applied to third-party works. Preserve upstream grants. For example, CC BY 4.0 permits licensed reproduction and adaptation subject to its conditions, including attribution when sharing; it does not grant every other person's rights. Do not add downstream conditions that restrict the licensed rights. [CC BY 4.0 legal code, sections 2–3](https://creativecommons.org/licenses/by/4.0/legalcode.en).

The ethical objective is to fund contributors while preserving lawful access to knowledge. Offer voluntary rewards for public-domain and openly licensed contributions without claiming exclusive ownership of facts or making nonparticipants owe royalties. Allow individual participation alongside syndicates. A syndicate represents only accepted mandates; it cannot claim all downstream ideas or set prices for nonmembers.

Licensing is the project's chosen admission policy, not a claim that permission is legally required for every possible use. US fair use depends on the facts and statutory factors; neither “research” nor a payment to a creator automatically resolves that analysis. Any exception-based admission needs a specific assessment rather than a blanket scraping rule. [Copyright Office Fair Use Index](https://www.copyright.gov/fair-use/).

## 8. Execution plan and release evidence

These are proposed stages, not completed activities or a guaranteed schedule.

| Stage | Responsible role | Concrete deliverable and exit condition |
| --- | --- | --- |
| Establish the boundary | Founder and qualified IP/technology counsel | Account/agreement inventory, artifact-use map, applicable jurisdictions and a written Route A or Route B decision. No assistant-generated approval substitutes for this review. |
| Secure inputs | Procurement lead and rights reviewer | Versioned model/tool terms, contributor grants, supplier creation-method disclosures, permitted-use matrix and unresolved-item register. Proposed model inputs have an evidenced basis. |
| Prove creator rewards | Product and finance leads | Small enrolled corpus, accepted agreements, visible source receipts, deduplicated usage records and reproducible statements. Pilot payouts remain simulated until real settlement is authorized and ready. |
| Develop the derivative | Model lead | Admitted training and evaluation manifests, dependency provenance, experiment records and documented inherited limits. No restricted or unresolved material enters the approved use. |
| Release commercially | Authorized release owner, counsel and finance | Approved release form, license/notice package, attribution manifest, supplier and payout reconciliation, customer terms, correction process and substantiated public claims. |

The review packet should identify the intended product, accounts and signed terms, prior assistance, independent sources, supplier warranties and evidence, model/data licenses, contributor agreements, syndicate mandates, reward calculations and intended API/weight distribution. Legal review should address concrete unresolved facts rather than merely approving the project name.

Before claiming independence, be able to answer:

- Which materials and tools support the released model, and what authorizes each intended use?
- What happened to earlier generated model-development material, including indirect feedback?
- Which contributors are covered by rewards, what earns money and who owes payment?
- Which upstream provenance and ancestry limits remain, and are the public claims accurate?
- Can attribution, permission decisions and statements be reconstructed without exposing private contributor or customer information?

Passing these checks would support a bounded, evidence-based release decision. It would not certify universal noninfringement or eliminate every commercial obligation.

## Primary sources and related project documents

Primary sources were checked on October 10, 2026. Current public terms do not establish which version governs an earlier account or transaction.

| Source | Role in this pathway |
| --- | --- |
| [OpenAI Terms of Use](https://openai.com/policies/terms-of-use/) | Individual output-use restriction and input ownership. |
| [OpenAI Services Agreement](https://openai.com/policies/services-agreement/) | Business restriction, exceptions and contractual priority. |
| [OpenAI Service Terms](https://openai.com/policies/service-terms/) | Additional conditions and generated-code licensing. |
| [NVIDIA Ultra model card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) | Selected artifact, stated license and disclosed training sources. |
| [OpenMDW-1.1](https://raw.githubusercontent.com/OpenMDW/OpenMDW/refs/heads/main/1.1/LICENSE.OpenMDW-1.1) | Model-material grants, notices, outputs and remaining responsibilities. |
| [Copyright Office Circular 31](https://www.copyright.gov/circs/circ31.pdf) | Ideas and methods versus protected expression. |
| [Copyright Office Fair Use Index](https://www.copyright.gov/fair-use/) | Fact-specific assessment of exceptions. |
| [Open Source Definition](https://opensource.org/osd) | Software freedoms and redistribution conditions. |
| [CC BY 4.0 legal code](https://creativecommons.org/licenses/by/4.0/legalcode.en) | Example public license and retained obligations. |

Read alongside the [project specification](SOVEREIGN_SOURCE_AI_CODEX_SPEC.md), [OpenAI restrictions research](OPENAI_COMPETING_MODEL_RESTRICTIONS_RESEARCH.md), [supplier research](UPSTREAM_AI_DATA_SUPPLIERS_RESEARCH.md) and [licensing guide](../licenses/README.md). These documents remain proposals and research; they do not replace executed agreements or an artifact-specific review.

# OpenAI restrictions on developing competing LLMs

**Project:** Super Sovereign Source LLM IP

**Research date:** October 10, 2026

**Status:** Public-contract research for product and procurement decisions; not a legal opinion on enforceability or a review of your signed agreements.

OpenAI's published terms restrict using its outputs to develop competing models. That matters directly to a proposed Sovereign Source model trained with ChatGPT-generated material. The restriction should not be restated as a universal prohibition on independently creating an LLM. Its application depends on the material used and the governing agreement. [Terms of Use, Using our Services](https://openai.com/policies/terms-of-use/).

This report separates contract language, OpenAI's product and enforcement statements, and proposed project controls. It complements the [frontier-lab terms audit](FRONTIER_LAB_IP_AND_CREATOR_REWARDS_AUDIT.md) and [upstream supplier research](UPSTREAM_AI_DATA_SUPPLIERS_RESEARCH.md). It does not change the project's model selection or determine that earlier project work breached an agreement.

## Source and version register

All sources below were reviewed on October 10, 2026. Publication dates do not establish which version governs a particular account.

| Source | Displayed date | Relevant scope |
| --- | --- | --- |
| [Terms of Use](https://openai.com/policies/terms-of-use/) | Effective January 1, 2026 | Individual services; separate EEA, Switzerland and UK terms are linked. |
| [Services Agreement](https://openai.com/policies/services-agreement/) | Updated December 1, 2025; effective January 1, 2026 | Business contract. |
| [Service Terms](https://openai.com/policies/service-terms/) | Updated September 29, 2026 | Additional product conditions. |
| [Early Access Terms](https://openai.com/policies/early-access-terms/) | December 20, 2024 | A specified frontier safety-research access program, including o3-mini. |
| [Model Distillation in the API](https://openai.com/index/api-model-distillation/) | October 1, 2024 | Product announcement, not an independent license. |
| [OpenAI open-weight models](https://help.openai.com/en/articles/11870455-openai-open-weight-models-gpt-oss) | Relative update label: two months ago | Official gpt-oss overview, not the complete license text. |
| [Distillation enforcement report](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign/) | September 30, 2026 | OpenAI's account of an enforcement incident. |

## The competing model restrictions

### Individual ChatGPT use

The Terms of Use prohibit:

> Use Output to develop models that compete with OpenAI.

The same section restricts automated extraction, reverse engineering and bypassing safeguards. The content section preserves existing input rights and assigns OpenAI's output interests, subject to law; ownership does not cancel use restrictions. No general research, nonprofit or open-source exception appears in the quoted rule. [Terms of Use, Using our Services and Content](https://openai.com/policies/terms-of-use/).

**Interpretation:** “develop” is broader wording than “train.” The clause does not precisely define competition or resolve every indirect contribution to model development. Treating all coding assistance as automatically permitted would be too categorical.

### Business and API use

The business route covers APIs and organizational services. Section 3.3(e), subject to its defined exception, prohibits:

> use Output to develop artificial intelligence models that compete with OpenAI’s products and services

The exception lists internal categorization/classification/organization models that are neither distributed nor commercially offered to third parties, and customization through specified OpenAI services. It does not generally authorize a competing public LLM.

Section 3.3 also restricts reverse engineering, unauthorized extraction, key transfers and circumvention; the reverse-engineering definition includes model extraction. Customers must not permit prohibited end-user activity. Section 2.2 permits API-powered customer applications. Section 16.2 gives Order Forms priority in conflicts.

**Commercial exposure:** sections 8 and 11 address suspension and termination; material-breach termination has a 30-day cure provision, while suspension can occur sooner. Section 14.1 excludes restriction breaches from its indirect-damages exclusion. Section 14.2 has a separate monetary cap and exceptions: a restriction breach is not automatically uncapped. Section 13.2 addresses third-party-claim indemnity. Section 11.3 can accelerate unpaid minimum commitments. [Services Agreement, sections 2.2, 3.3, 8, 11, 13–14, 16.2 and definitions](https://openai.com/policies/services-agreement/).

### Additional product conditions

The Service Terms take precedence over a conflicting underlying agreement according to their introduction. Their code-generation section says generated code can carry third-party licenses. It provides no express competing-model exemption for Codex-generated code. Its API output-indemnity provisions have substantial exclusions and should not be mistaken for permission to train a competitor.

Section 10 separately restricts certain delivered software packages and containers: permitted service connection, limited use and restrictions on modification or redistribution, with a component-specific open-source override. Downloadable service materials and independently licensed model weights must be distinguished. [Service Terms, introduction and sections 1, 4 and 10](https://openai.com/policies/service-terms/).

### The narrower early access program

The December 2024 Early Access Terms limit the specified program to safety research and expressly prohibit distillation, extracting OpenAI technology and training a model on outputs. They also permit prompt/completion review and access withdrawal.

This is a **program-specific condition**. Its blanket output-training prohibition should not be silently attributed to every ordinary API account or every later beta. Participation terms for the actual program must be checked. [Early Access Terms](https://openai.com/policies/early-access-terms/).

## Why OpenAI advertises distillation while restricting it

OpenAI's October 2024 announcement describes using outputs from larger OpenAI models to customize smaller models **within its platform**, integrating stored completions, evaluations and fine-tuning. The announcement supports that hosted workflow; it does not grant permission to move those outputs into a competing, independently hosted model. Its historical model names, pricing and promotional credits are not current procurement guidance. [Model Distillation in the API](https://openai.com/index/api-model-distillation/).

For this project, an OpenAI-hosted customization and an independently distributed Nemotron adaptation are different intended destinations. A documented workflow for the first does not establish authorization for the second.

## Downloadable OpenAI models have a different licensing route

OpenAI's gpt-oss overview describes downloadable models under Apache 2.0 and its gpt-oss usage policy, with commercial deployment, modification and redistribution supported. It describes these deployments separately from ChatGPT and the OpenAI API. This is material counterevidence to the claim that OpenAI prohibits every independently hosted model business. [Official open-weight overview](https://help.openai.com/en/articles/11870455-openai-open-weight-models-gpt-oss).

That distinction does not turn hosted ChatGPT outputs into unrestricted training material. Evaluate both the model artifact's license and the origin of any added data. A full license and policy review is required for a particular release; the overview alone is not that review. The current project target remains Nemotron 3 Ultra.

## Evidence that enforcement is operational

In its September 30, 2026 report, OpenAI describes a coordinated attempt to extract protected reasoning and says it restricted accounts, strengthened technical controls and coordinated with service partners. OpenAI characterizes unauthorized distillation as using outputs or reasoning to train, reproduce or improve another model. These are the company's reported observations and position, not a court judgment. [OpenAI enforcement report](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign/).

The reported activity involved deliberate extraction. It does not establish that routine coding help, ordinary evaluation or this project's documentation work received the same treatment. The operational lesson is that access continuity cannot be assumed when a model-development workflow depends on contested output reuse.

## Application to Sovereign Source

The table below gives **proposed handling decisions**, not findings that each activity is unlawful or contractually identical. It translates the evidence into questions for the project's existing permission and provenance process.

| Proposed activity | Handling decision | Evidence or question to resolve |
| --- | --- | --- |
| Train Nemotron on generated answers, explanations or worked examples | Do not admit by default. | Obtain permission that identifies the teacher, destination model, training use and commercial release. |
| Use generated rankings, critiques, labels or rewards to improve the model | Include these artifacts in the same provenance review. | Determine whether an apparently auxiliary signal is being used in competing-model development. |
| Use ChatGPT as an evaluator for model selection or iterative improvement | Separate one-time comparison from feedback feeding development; review the actual workflow. | The reviewed clauses do not provide a universal evaluation exemption or a precise boundary. |
| Generate model architecture code, training recipes or optimization advice | Record the assistance and seek a scoped interpretation before relying on it for a competing model. | General code ownership and the breadth of the development restriction are different questions. |
| Build a chat interface, billing system or creator-attribution ledger | Review as application software, including code provenance and third-party licenses. | Do not convert an application-development assessment into blanket approval for model development. |
| Import this project's Markdown chat archive | Preserve it as a historical record; do not automatically classify it as training data. | Identify original human inputs, generated replies and quoted third-party material separately. |
| Buy expert data from an upstream supplier | Request creation methods, source-model disclosures and the permission chain. | A supplier's paid invoice does not establish the provenance required by SIP. |
| Commission original expert tasks or license existing works directly | Use the project's ordinary asset-admission process. | Verify contributor authority, permitted use, attribution and agreed rewards independently. |

These controls are consistent with the [project specification](SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) and [supplier procurement research](UPSTREAM_AI_DATA_SUPPLIERS_RESEARCH.md). They do not claim that human editing, attribution, a new filename or a different supplier removes an earlier restriction. A reviewer should inspect the actual chain of creation and use.

## Commercial effect and unresolved legal questions

**Commercial interpretation:** the combination of the competing-model clause and OpenAI's hosted distillation offering favors certain complementary products and platform-contained customization over using hosted outputs to build an independent substitute. That is an inference about the arrangements above, not proof of OpenAI's subjective motive or a finding of unlawful conduct.

The distinction matters for describing the project accurately. “We need independently authorized sources for our model” is a supportable procurement position. “OpenAI legally prevents anyone from competing” overstates what these documents establish.

An enforceability or competition-law opinion would require additional work: the contracting entity, accepted versions, jurisdiction, negotiated amendments, specific conduct and applicable legal authorities. This report does not determine whether a restriction is enforceable, whether an exception applies to your particular implementation, or whether any provision violates competition law.

For a concrete legal or commercial review, resolve:

1. **What is the competing product?** Describe the model, intended users, distribution, hosting and revenue model, including whether weights will be public.
2. **What OpenAI material is used?** Identify examples, labels, critiques, grading signals, code, design advice and any third-party content carried in responses.
3. **What activity needs authorization?** Specify training, evaluation, model selection, adaptation, redistribution and supplier participation individually.
4. **Which agreement governs?** Identify the account and contracting party, accepted version, applicable product conditions and any signed amendments.
5. **What permission would be sufficient?** Request a signed, workflow-specific provision identifying allowed artifacts, destination models, recipients, duration and existing generated material.
6. **What commercial exposure is accepted?** Review access interruption, termination, commitments, indemnities, damages limitations and dispute procedures together.

These are questions for a scoped review or negotiation. No project-specific waiver was supplied for this review; a public product page or assistant answer is not a negotiated amendment.

## Proposed project record

For each externally generated artifact considered for model development, retain:

| Record | Purpose |
| --- | --- |
| Source service, model and date | Identify where the artifact originated. |
| Account and agreement version | Identify the asserted contractual basis. |
| Intended model and use | Make the proposed reuse specific. |
| Original inputs and intermediate contributions | Distinguish independently supplied work from generated or transformed material. |
| Permission evidence and reviewer decision | Explain why the intended use was admitted or withheld. |
| Downstream recipients and release form | Track whether the artifact supports private work, a hosted service or distributed weights. |
| Credit and compensation agreement | Preserve SIP commitments separately from authorization to train. |

These are proposed evidence fields, not implemented features. For the first independently trained release, favor original commissioned contributions and datasets whose agreements expressly address the intended model development. Preserve unresolved provenance as an unresolved issue rather than filling it with an assumed permission.

The repository's earlier chat export remains a historical snapshot. This research should be consulted alongside the current specification when deciding whether any generated project material can enter a training or model-development pipeline.

The [pathway from ChatGPT to an independent LLM with content rewards](CHATGPT_TO_INDEPENDENT_LLM_PATHWAY.md) turns these findings into two proposed routes: explicit contractual permission or independently authorized development. It includes treatment of prior assistance, contributor agreements and release evidence; it grants no waiver or model-development clearance.

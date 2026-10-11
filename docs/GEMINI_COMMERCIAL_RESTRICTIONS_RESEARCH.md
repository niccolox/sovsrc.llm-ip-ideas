# Gemini commercial restrictions on developing competing LLMs

**Project:** Super Sovereign Source LLM IP

**Research date:** October 10, 2026

**Scope:** Published US consumer and commercial terms. This is contract research for product decisions, not a legal opinion on enforceability or a review of signed agreements.

**Gemini is not an unrestricted teacher for an independent Sovereign Source LLM.** The developer terms prohibit using the service to develop competing models; the US consumer terms prohibit using generated content for machine-learning development more generally. [Gemini API terms](https://ai.google.dev/gemini-api/terms), [Google US terms](https://policies.google.com/terms?hl=en-US).

The proposed project decision is to keep Gemini-generated training material out of Nemotron adaptation unless a governing agreement expressly permits the intended workflow. This complements the [OpenAI restrictions report](OPENAI_COMPETING_MODEL_RESTRICTIONS_RESEARCH.md) and [frontier-lab audit](FRONTIER_LAB_IP_AND_CREATOR_REWARDS_AUDIT.md).

## Restrictions by access route

| Access route | Contract wording and practical boundary |
| --- | --- |
| Gemini API and Google AI Studio | The Use Restrictions state: “You may not use the Services to develop models that compete with the Services”. This covers service use, not merely copying responses into a dataset. [Additional terms](https://ai.google.dev/gemini-api/terms). |
| Gemini through Google Cloud, including Vertex AI | Section 17(a) restricts competitive service/output use; 17(b) separately restricts output use to replace Google models or create/improve similar models. Section 17(c) bars extraction. Suspected violations can trigger immediate suspension or termination under 17(a), 17(c) and 20(f). [Cloud service terms](https://cloud.google.com/terms/service-terms). |
| Gemini Apps under Google's US general terms | The abuse section prohibits “using AI-generated content from our services to develop machine learning models or related AI technology”. Competition is not a stated condition. [US terms](https://policies.google.com/terms?hl=en-US). Google's [service register](https://policies.google.com/terms/service-specific?hl=en) lists Gemini Apps under these terms. |
| Gemini under Workspace terms | Section 12.4 prohibits generated output as a material input to developing models competing with Workspace services, and output-based reverse engineering. Section 12.8 permits immediate suspension or termination for suspected violations. [Workspace service terms](https://workspace.google.com/terms/service-terms/). |
| Gemini Enterprise Business Edition | Its additional terms incorporate Google's general terms and distinguish this edition from Google Cloud Platform services. The business label does not establish a Cloud contract. [Business Edition terms](https://cloud.google.com/terms/gemini-enterprise/business?hl=en). |

Workspace account status matters: Google's guidance distinguishes Gemini as a core Workspace service from an additional service governed by general Google terms. Identify the actual edition and contract before assessing a use. [Work-account guidance](https://support.google.com/gemini/answer/14620100?hl=en-gw).

## What the Cloud exceptions actually cover

Section 17(b) allows output-based modification when the service offers fine-tuning or distillation, for use of **Modified Google Models**. Section 17(a)'s platform exception applies when no Google Pre-Trained Model is used. The current name is Gemini Enterprise Agent Platform, formerly Vertex AI Platform. Neither exception grants unrestricted Gemini-to-Nemotron distillation. Section 20(k) separately restricts training on and syndication of Search-grounded results. [Cloud service terms, 14 and 17–20](https://cloud.google.com/terms/service-terms).

**Interpretation for procurement:** distinguish renting infrastructure for an independently licensed model from obtaining Google's model behavior as a training resource. A provider offering both does not make their permissions interchangeable. The platform exception addresses 17(a), so the remaining clauses still need assessment for the actual workflow.

## Payment, confidentiality and attribution

Google disclaims ownership of API-generated content, while retaining use restrictions and applicable attribution duties. Paid API treatment excludes product-improvement use of prompts/responses; unpaid treatment generally permits it and human review, with an EEA/Swiss/UK exception. Billing status changes data handling, not the competitor clause. Search grounding separately limits training, collection, storage and display; Maps data cannot be used for training. [Gemini API terms, Generated Content, data and Grounding sections](https://ai.google.dev/gemini-api/terms).

Workspace separately promises not to train its supporting generative models on Customer Data without permission or instruction. That commitment governs Google's use of customer information; it does not remove the customer's output-use restriction. [Workspace service terms, 12.4 and 12.11](https://workspace.google.com/terms/service-terms/).

Google's prohibited-use policy also addresses third-party rights and misleading claims that generated content is entirely human-created. Its discretionary scientific/educational exceptions concern that policy, not a general waiver of contractual model-development restrictions. [Generative AI Prohibited Use Policy](https://policies.google.com/terms/generative-ai/use-policy).

**SIP implication:** treat permission, attribution and payment as separate decisions. Paying an API bill or compensating a creator cannot supply a missing license from another rights holder. Preserve required source references, but do not market citation display as proof that a training corpus is authorized. The syndicate marketplace should obtain its contribution permissions directly from parties able to grant them.

## Commercial consequences

The Google APIs terms reserve broad access-termination rights in section 8. Section 9 limits Google's liability and requires business users to indemnify specified Google parties for allegations or proceedings arising from misuse, terms violations or supplied content. These provisions make continuity and dispute exposure procurement issues. [Google APIs terms, 8–9](https://developers.google.com/terms).

The Cloud agreement permits immediate suspension for breaches of service-specific terms. Section 8.3 generally provides a 30-day material-breach cure period, with an exception for incurable customer breaches. Section 12 has liability limits and separate unlimited-liability categories, including indemnity, IP infringement and payment obligations. A contract breach is not automatically an IP infringement or an uncapped claim. Section 13 addresses indemnity; section 5.3 permits feedback use without an obligation to the customer. [Cloud agreement, 4, 5.3, 8 and 12–13](https://cloud.google.com/terms/).

**Commercial interpretation:** a training pipeline dependent on contested output reuse can face interruption, unusable data and replacement costs. The actual remedy depends on the applicable agreement and facts. No contractual clause described here establishes a general legal ban on independently competing with Google.

## Decisions for Sovereign Source

These are proposed project handling rules, not findings that every activity has the same contractual treatment.

| Intended use | Proposed handling |
| --- | --- |
| Generate synthetic answers, reasoning examples or demonstrations for Nemotron | Require explicit authorization covering the destination model, training and commercial release before admission. |
| Produce rankings, critiques, labels or reward signals | Review their downstream role in improvement; do not exempt them because they are not ordinary answer text. |
| Evaluate competing models | Distinguish a bounded comparison from repeated feedback feeding development. Obtain a scoped interpretation of the actual workflow. |
| Write model architecture, training code or optimization recipes | Do not assume a coding exemption. Record generated assistance and resolve the applicable development restriction. |
| Build attribution, licensing or payout software | Assess application work separately, including how generated material enters the model-development process. |
| Acquire a supplier's dataset | Require disclosure of generation services, contracts and transformations. A supplier's invoice is not provenance evidence. |
| Collect Search-grounded responses for the marketplace | Obtain an independently authorized content supply; do not treat grounding as a bulk syndication license. |

For an exception request, describe: the account and service; target checkpoint; generated artifacts; training versus evaluation; access by suppliers; commercial hosting versus public weights; attribution requirements; and continued use after termination. Seek a signed agreement that resolves the relevant restriction explicitly. Permission should cover existing material if it will be reused.

The [project specification](SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) already separates permission from credit and rewards. Apply that distinction to teacher-model outputs as well as original works. Retain agreement versions and artifact provenance with the admission decision. This report proposes handling rules; it does not implement an enforcement service.

## Gemma has a separate licensing route

Gemma must be checked by release. Google's Gemma terms page directs **Gemma 4** to Apache 2.0. For the older releases listed in its appendix, custom terms govern use and distribution; their derivative-model definition includes specified output-based distillation, and distribution obligations can follow the derivative. [Gemma terms, introduction and sections 1–3](https://ai.google.dev/gemma/terms).

The linked Apache 2.0 license permits modification and distribution subject to its conditions, including notice preservation; it grants no general trademark rights. This is a materially different starting point for independently deploying a model. It does not authorize adding restricted Gemini-service outputs to that model. [Gemma 4 license](https://ai.google.dev/gemma/apache_2).

The project target remains **Nemotron 3 Ultra**. Gemma is a licensing comparison here, not a replacement selection or a certification of training-data ancestry.

## Source and version register

Reviewed October 10, 2026. Displayed publication dates do not establish when a change became binding on a particular account. Signed contracts, accepted versions, renewal dates and regional provisions can alter the result.

| Instrument | Displayed date or version | Scope used |
| --- | --- | --- |
| [Gemini API Additional Terms](https://ai.google.dev/gemini-api/terms) | Effective March 23, 2026 | AI Studio and Gemini API |
| [Google APIs Terms](https://developers.google.com/terms) | Modified November 9, 2021 | API contract and remedies |
| [Google US Terms](https://policies.google.com/terms?hl=en-US) | Effective July 30, 2026 | Consumer generated-content restriction |
| [Google service register](https://policies.google.com/terms/service-specific?hl=en) | Live register | Gemini Apps contract mapping |
| [Google Cloud agreement](https://cloud.google.com/terms/) | Modified September 2, 2026 | Business obligations and remedies |
| [Cloud service terms](https://cloud.google.com/terms/service-terms) | Modified October 8, 2026 | AI/ML and generative service clauses |
| [Workspace service terms](https://workspace.google.com/terms/service-terms/) | Modified August 31, 2026 | Workspace generative services |
| [Workspace agreement page](https://workspace.google.com/terms/premier_terms/) | Modified September 2, 2026 | States transition to integrated Cloud terms at next renewal |
| [Work-account guidance](https://support.google.com/gemini/answer/14620100?hl=en-gw) | Live guidance | Core versus additional service |
| [Business Edition additional terms](https://cloud.google.com/terms/gemini-enterprise/business?hl=en) | Modified March 30, 2026 | Separate Enterprise Business Edition route |
| [Generative AI Prohibited Use Policy](https://policies.google.com/terms/generative-ai/use-policy) | Modified December 17, 2024 | Rights, provenance and policy exceptions |
| [Gemma terms](https://ai.google.dev/gemma/terms) | Modified April 1, 2026 | Listed older releases and Gemma 4 license pointer |
| [Gemma 4 license](https://ai.google.dev/gemma/apache_2) | Apache 2.0, January 2004 | License version, not model release date |

Enforceability requires jurisdiction-specific legal analysis. A provider's published restriction, a negotiated permission, and a court's assessment are different questions. None of the research establishes that prior project work breached a contract.

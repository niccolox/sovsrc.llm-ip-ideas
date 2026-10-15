# Sovereign Source specification versus patents and open standards

**Research date:** October 15, 2026  
**Project:** Super Sovereign Source LLM IP  
**Comparison baseline:** repository commit [`597883a`](https://github.com/niccolox/sovsrc.llm-ip-ideas/tree/597883a9923364295e6451eaaa0de06a44e213a0)

**The closest functional overlap is the planned combination of licensed retrieval, contributor rewards and provider reporting.** The specification has more explicit commitments to voluntary syndicates, accepted earning agreements, reviewed influence acknowledgments and reproducible accounting than the selected claim summaries. Those commitments help define the product, but they do not establish patent novelty or remove overlap with a claimed combination.

Sovereign Source also makes an important distinction: recorded use and accepted agreements determine rewards; an AI estimate of influence does not create an entitlement by itself. Several identified patents concern particular methods of estimating attribution. The present specification does not require those methods, although future attribution components could introduce them.

This document maps **planned requirements**, not operating software. The repository remains at specification stage; its initial M0–M4 plan uses deterministic model behavior, synthetic attribution proposals and simulated payments. This is a technical research comparison, not a legal opinion on infringement, validity or freedom to operate. Patent counsel should assess the implemented combination and relevant claims before commercial deployment.

## Baseline and reading guide

| Project document | Version reviewed | Role in this comparison |
| --- | --- | --- |
| [Product and implementation specification](SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) | v0.7, dated October 10, 2026; content at the baseline commit above | Proposed architecture, contribution graph, marketplace, reward engine and development milestones. References below use **Product §**. |
| [LLM Rights and Content Awards](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md) | LRCA 1.0, draft 0.1, October 15, 2026 | Normative requirements identified by RI, TR, AT, US, AW, AC, PS and SP codes. |
| [Sovereign Source Super Intellectual Property license](../licenses/SS-SIP-0.1.md) | SS-SIP-0.1 draft, October 10, 2026 | Attribution duties, permissions, the limited contributor patent grant and optional marketplace participation. |
| [Patent landscape research](SOVEREIGN_SOURCE_PATENT_LANDSCAPE_RESEARCH.md) | October 15, 2026 | Publication dates, priority dates, assignees, twelve primary documents and additional portfolio leads. |

**Close planned function** means the specification describes similar operations. **Implementation unresolved** means the exact mechanism is not sufficiently specified. **Mechanism not required** means the specification can be read without that particular mechanism; it does not prove that a future implementation omits it. **Later feature** means relevance principally arises in an expansion beyond the text-first pilot. None of these labels is a legal risk score.

Patent status below is the Google Patents index's reported status on the research date, not a certified check of USPTO prosecution, ownership, fees or litigation. Granted claims and published application claims are distinguished. A pending application is not a grant; conditional provisional rights can arise after issuance. The legal comparison concerns claim limitations and the actual product or process, rather than shared terminology alone. [USPTO patent rights](https://www.uspto.gov/patents/basics/manage), [USPTO application publication](https://www.uspto.gov/patents/basics/apply).

## Side-by-side comparison of the twelve primary documents

The claim descriptions are abbreviated and selective. They identify engineering questions rather than substitute for complete claim charts. Every document number links to its published claims.

| Patent or application | Sovereign Source requirement | Selected claimed mechanism | Alignment and material distinction | Practical review priority |
| --- | --- | --- | --- | --- |
| **Preferred Networks — [US20260228313A1](https://patents.google.com/patent/US20260228313A1/en)**. Pending. Claims 1, 33, 34. | Product §§6, 11–12; [LRCA §7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7) US-01/02, [§8](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-8) AW-01, [§9](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-9) beneficiary exports. | Question-based retrieval for generation with provider royalties; claim 33 separately covers provider-facing management data about information used. | **Close planned function.** SIP adds agreement, permission and accounting controls, but those additions do not remove retrieval, rewards or reporting. Claim 33 does not require a royalty to be granted. | First pending filing to review for the licensed-retrieval business. Assess both payment and reporting paths. |
| **Sureel — [US12013891B2](https://patents.google.com/patent/US12013891B2/en)**. Granted; indexed Active. Claim 1; also inspect independent claims 8 and 15. | Product §§11–12; [LRCA §6](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-6) TR-01 and [§12](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-12) SP-02. | Parameter changes during training measure content influence; creator aggregates form a static attribution vector used for compensation after generation. | **Mechanism not required.** SIP's corpus score uses capped, deduplicated exposure and predefined weights. A consumption manifest is not a parameter-change attribution calculation. | Reassess before using model-weight or gradient influence to allocate payments. |
| **Sureel — [US12314308B2](https://patents.google.com/patent/US12314308B2/en)**. Granted; indexed Active. Claim 1; also 7 and 14. | Product §11; [LRCA §7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7) AT-01 and [§8](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-8) AW-01/02. | CLIP/CLAP-derived creator representations, output/content embedding distances, creator aggregation, thresholding and compensation. | **Mechanism not required.** SIP permits AI proposals but does not mandate this pipeline or let similarity establish a payment entitlement. Human review alone would not necessarily remove the machine operations. | Chart the full algorithm before adding embedding-based creator valuation or buying an attribution service. |
| **Technica Pacifica — [US12657517B1](https://patents.google.com/patent/US12657517B1/en)**. Granted; indexed Active. Claims 1–2. | Product §§6, 11, 17; [LRCA §5](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-5) RI-01, [§10](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-10) PS-03. | Training data carries conditions linked by an identifier; intermediate model output contains the identifier; retrieved conditions cause response modification. Claim 2 adds payment. | **Implementation unresolved.** SIP keeps authority outside model reasoning, but M6 includes citation training. It does not categorically prohibit model-emitted identifiers or their downstream resolution. | Trace identifiers from training through generation and policy execution. Blockchain is not required by claims 1–2. |
| **BRIA — [US20260093745A1](https://patents.google.com/patent/US20260093745A1/en)**. Pending. Independent claim 41; dependent claims 49, 52–53. | Product §11 influence graph; [LRCA §6](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-6) TR-03/04 and [§7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7) AT-01. | Generate with auxiliary content, determine attribution degree and provide resulting information; dependent claims extend attribution through a second model's training sources. | **Partial; implementation unresolved.** Reviewed declarations and stored lineage differ from calculating degrees of output attribution. However, a source-scoring feature could introduce the independent claim's mechanism without automatic royalties. | Examine ordinary RAG attribution as well as multi-stage generated-source attribution. |
| **BRIA — [US20260087271A1](https://patents.google.com/patent/US20260087271A1/en)**. Pending. Claim 1. | Product §11; [LRCA §6](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-6) TR-01 and [§7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7) AT-01. | Compare properties of generated text and training texts to attribute the output to a nonempty proper subset of training examples. | **Mechanism not required.** SIP distinguishes training participation from causal attribution of an answer. Optional estimated influence remains an unresolved implementation area. | Review before claiming to identify which training passages produced an answer. |
| **Citibank — [US12587490B2](https://patents.google.com/patent/US12587490B2/en)**. Granted; indexed Active. Independent claims 1, 7, 14. | Product §§6–7; [LRCA §5](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-5) RI-01/02 and [§10](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-10) PS-03. | AI agents evaluate requested content interactions against stored policies, generate permitted access and save linked authorization artifacts in a distributed database. | **Partial; interpretation unresolved.** SIP requires structured authority and prevents the model from granting permissions. Rust implementation alone does not establish whether a component falls outside “AI-based agent” language. | Assess claim 14 as well as claim 1; inspect the actual decision service, persistence and deployment. |
| **BRIA — [US12033372B2](https://patents.google.com/patent/US12033372B2/en)**. Granted; indexed Active. Selected independent claims 1, 2, 16. | Product §17 modality expansion; [LRCA §7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7) attribution relationships. | Visual-output attribution to training examples and updates to source records; different independent claims use convolution, attribution degrees or embeddings. | **Later feature.** The text-first pilot does not require visual-output attribution. The broader LRCA data model could support it later. | Add a separate image-attribution assessment before multimodal expansion; do not rely only on claim 1's convolution limitation. |
| **Adobe — [US12675976B2](https://patents.google.com/patent/US12675976B2/en)**. Granted; indexed Active. Claim 1; also 8 and 14. | Product §17 future modalities; estimated influence under [LRCA §7](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-7). | Generated and training images pass through a shared base encoder with different mapping layers; vector similarity produces an influence score. | **Later feature; mechanism not required.** No such image-attribution architecture is prescribed. | Evaluate the grant, not merely its earlier application US20250104399A1, when selecting a diffusion-attribution component. |
| **BG Negev / Fujitsu — [US20260065071A1](https://patents.google.com/patent/US20260065071A1/en)**. Pending. Claim 1. | Product §§11, 17; [LRCA §6](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-6) training records. | Aggregate changes during model training into an attribution table and train an attribution model from that table. | **Mechanism not required.** Recording actual dataset consumption does not specify training a separate influence predictor from model changes. | Review instrumentation and derived attribution-model training before introducing this research path. |
| **Addepalli — [US11423454B2](https://patents.google.com/patent/US11423454B2/en)**. Granted; indexed Active. Claim 1. | Product §§7–8, 17; [LRCA §8](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-8) AW-03. | Secure model transfer, a repository and marketplace, with parallel model distribution for further training and merging of results. | **Partial; later feature.** SIP's initial syndicates administer contributions and contracts; they do not require this collaborative model-training combination. | Reassess if syndicates exchange, jointly train, merge or trade models. Marketplace terminology alone is insufficient. |
| **Huawei Cloud — [US11989260B2](https://patents.google.com/patent/US11989260B2/en)**. Granted; indexed Active. Claim 1. | Product §12; [LRCA §12](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-12) SP-02 and [§8](LLM_RIGHTS_AND_CONTENT_AWARDS_SPEC.md#lrca-section-8) AW-01. | Train on provider datasets, evaluate predictions using consumer test data, derive unit values, distribute incentives and share data. | **Mechanism not required.** Predefined corpus weights and reviewed adoption points do not mandate this model-evaluation-to-pricing pipeline. | Reassess automated dataset pricing or buyer-specific performance valuation. US patent relevance is independent of the project's US-model sourcing preference. |

## Four comparisons that deserve closer attention

These abbreviated element maps expose the most consequential unanswered questions. They are not complete legal charts, and an unspecified element is not a demonstrated omission.

### 1. Retrieval rewards and provider reporting

| Selected element | Planned specification counterpart | Assessment |
| --- | --- | --- |
| Question acquisition and information retrieval for generation — claims 1/34 | Product §11; LRCA US-02 serving sequence | Direct planned functional correspondence. |
| Provider royalty — claims 1/34 | AW-01 accepted earning agreement and Product §12 retrieval-fee mechanism | Correspondence depends on the chosen agreement and implemented qualifying event; not every fetch earns. |
| Generate using retrieved information; maintain per-item usage data — claim 33 | US-01 source/version/use records and US-02 generation | Direct planned functional correspondence. |
| Provide part of the management data to its provider — claim 33 | LRCA §9 beneficiary explanations and exports | Close when the beneficiary is the information provider and the export includes the relevant information-use records. |

**Consequence:** changing a payment label or using fixed fees is not a demonstrated solution to the reporting claim. Review the actual provider dashboard and export payload alongside reward calculation. [Preferred Networks claims 1, 33–34](https://patents.google.com/patent/US20260228313A1/en).

### 2. Rights identifiers emitted by the model

| Selected element | Planned specification counterpart | Assessment |
| --- | --- | --- |
| Train on data subject to machine-readable conditions; associate model/condition with an identifier | RI-01 permission records and TR-01 manifests | Related records exist; the precise claimed association is unresolved. |
| Intermediate model output contains the identifier | Product §17 M6 citation training | Possible future implementation, not a mandatory rights-token mechanism. |
| Resolve that identifier and use its condition to modify the response during generation | Product §11 citation validation and permission recheck; PS-03 authority boundary | Whether this specific causal sequence occurs is unresolved. External policy execution alone does not answer it. |
| Payment action — dependent claim 2 | Separate awards and settlement services | A link from this condition-processing path to payment is not specified. |

**Consequence:** preserve traces showing where source IDs originate, what the model emits, which trusted record authorizes action and when a response changes. The model must not become an authority merely because it produces a valid-looking ID. [Technica Pacifica claims 1–2](https://patents.google.com/patent/US12657517B1/en).

### 3. Attribution across generated intermediates

| Selected element | Planned specification counterpart | Assessment |
| --- | --- | --- |
| Generate using natural-language input and auxiliary content — claim 41 | Product §11 retrieval-assisted answers | Close planned function. |
| Determine attribution degree to auxiliary content and provide information based on it — claim 41 | AT-01 reviewed source relationships and optional influence estimates | A recorded support relationship need not calculate a degree; the estimator is unspecified. |
| Update a source record from that degree — claim 49 | Usage receipts and accepted graph records | Depends on whether a calculated degree drives the update. |
| Trace generated auxiliary material to a subset of a second model's training examples, with secondary degrees — claims 52–53 | TR-03 synthetic provenance; Product §11 supported upstream chains | Manifest/declaration lineage does not require this reconstruction algorithm. |

**Consequence:** keep evidence types distinct. A declared parent source, observed retrieval and estimated training influence should remain separate fields, with methods disclosed. This supports the existing specification and makes any algorithmic overlap assessable. [BRIA claims 41, 49, 52–53](https://patents.google.com/patent/US20260093745A1/en).

### 4. AI agents deciding permissions

| Selected element of claim 14 | Planned specification counterpart | Assessment |
| --- | --- | --- |
| Request identifies content and requested interactions | Product §7 permission-service inputs; RI-01 | Close planned function. |
| Distributed database holds linked content policies | PostgreSQL authority records | Persistence exists in the design; the relevant deployment and “distributed database” interpretation remain unresolved. |
| AI-based agents evaluate requests and generate an access set | Rust permission service; AI proposals cannot grant authority | Meaningful architectural distinction to investigate, not a conclusion based on programming language. |
| Store the request, permitted access and pointer to the content record | Versioned permission decisions and linked usage evidence | Functional resemblance; exact artifact structure requires implementation evidence. |

**Consequence:** assess the policy engine's behavior, not its name. Claim 14 should not inherit narrower limitations from independent claim 1, such as its cryptographic-identifier formulation. [Citibank claim 14](https://patents.google.com/patent/US12587490B2/en).

## Adjacent patents and disclosures

| Item | Side-by-side implication |
| --- | --- |
| **BRIA marking and usage recording:** [US20260087107A1](https://patents.google.com/patent/US20260087107A1/en), claim 101; [US20260087108A1](https://patents.google.com/patent/US20260087108A1/en), claim 121. Both indexed Pending. | These address attribution encoding and subsequent detection/decoding for source-record updates. LRCA AT-02 requires credit to survive supported exports but does not require a watermark or this detection chain. Review any embedded metadata or downstream monitoring implementation; metadata should not be assumed outside the claims. |
| **TrustLedger:** [US20260003939A1](https://patents.google.com/patent/US20260003939A1/en), indexed Pending. | Claim 1's provenance, royalty, zero-knowledge and monitoring combination has conceptual similarities to SIP. PS-02 requires integrity but no zero-knowledge verification. Independent claims 14–15 need separate review; omitting one claim's feature does not dispose of the application. |
| **DRSK AI:** [US20250258892A1](https://patents.google.com/patent/US20250258892A1/en), indexed Abandoned. | Claims 1/11 describe metadata and embedding comparisons for asset lineage. Compare with the optional AI relationship proposer, not the authoritative payment ledger. The disclosure remains a research lead; related applications and official status were not cleared. |
| **Additional Sureel grants:** [US12554767B2](https://patents.google.com/patent/US12554767B2/en) and [US12567396B2](https://patents.google.com/patent/US12567396B2/en). | Portfolio leads recorded in the landscape, not fully charted here. Do not treat the two primary Sureel rows as exhaustive coverage of an attribution supplier's patent position. |

## Open standards, research and licensing alongside the spec

| Existing work | What it provides | Sovereign Source addition or difference | Remaining work |
| --- | --- | --- | --- |
| **[W3C ODRL 2.2](https://www.w3.org/TR/odrl-model/)** | A model for expressing permissions, prohibitions, duties, parties, assets and agreements. | RI-01/02 specify operational admission and authority evidence; AW-01/03 add earning agreements and syndicate mandates; AC requirements add settlement behavior. | LRCA §14 proposes alignment. Define and test the actual profile and serialization before claiming ODRL interoperability. |
| **[W3C PROV-O](https://www.w3.org/TR/prov-o/)** | Entities, activities, agents and provenance relationships including use, derivation and attribution. | TR-01/04 distinguish actual training consumption, learned dependencies and surviving obligations. AT-01 distinguishes acknowledgment from influence estimates. | Formal mappings remain open. A provenance edge alone is not accepted permission or a payable obligation. |
| **[W3C Web Annotation](https://www.w3.org/TR/annotation-model/)** | Structured annotations connecting bodies and targets, including mechanisms for identifying relevant portions. | The contribution graph adds evidence basis, review state, uncertainty and accepted credit preferences. | Specify source-version and passage-selector bindings; the current draft does not supply a complete interoperable annotation profile. |
| **[Data Shapley](https://proceedings.mlr.press/v97/ghorbani19c.html)**, 2019 | A research approach to data valuation through contribution to predictive performance. | SIP-Pool-0.1 currently uses exposure, execution and reviewed adoption measures selected by agreement. It does not require Shapley valuation. | Any future valuation experiment needs defined objectives, evaluation and separate permission to use its result economically. Publication is not proof that every implementation is patent-cleared. |
| **[TracIn](https://arxiv.org/abs/2002.08484)**, 2020 | Estimates training-example influence using training checkpoints and gradient information. | SIP distinguishes such an estimate from observed use and an accepted reward entitlement. | Treat it as a disclosed research method, not an automatic ownership or payout determination. Any prior-art argument needs dated disclosure and claim-element analysis. |
| **[SS-SIP-0.1 §3](../licenses/SS-SIP-0.1.md#3-rights-granted)** | The draft already grants applicable patents controlled by a licensor and necessarily practiced by its covered contribution, alone or in its supplied combination. | This is an actual contributor patent-permission provision; it is not missing from the draft. | It does not license unrelated third-party patents or every later combination. Confirm authorized adoption and coverage for each contribution. The draft is not OSI-approved. |
| **[W3C Patent Policy](https://www.w3.org/policies/patent-policy/)** | Defined royalty-free commitments concerning essential claims within the policy's participation and scope rules. | LRCA is an independent W3C-style proposal, not a W3C Recommendation or an enrollment in those commitments. | A future standards effort would need its own disclosed participation, patent-licensing and disclosure arrangements. Formatting does not create a patent license. |

Publications can supply leads for prior-art research, but overlap in subject matter is not a finding that a particular claim is invalid. Conversely, a custom open-source license cannot confer rights its licensors do not control.

## What is distinctive about the proposed product

The strongest product differentiation is the combination of contribution governance and accountable operations. These are **specification commitments**, not a claim that no prior system contains them.

| Commitment | Exact specification basis | Commercial significance |
| --- | --- | --- |
| Recognize ideas, workflows, curation and acknowledged influences through accepted agreements | Product §§1, 8, 11; LRCA AT-01, AW-01 | Extends participation beyond selling a corpus while avoiding automatic ownership claims over abstract ideas. |
| Separate membership, licensing authority, collection authority and economic shares | Product §7; LRCA RI-02, AW-03 | A syndicate can administer selected assets without acquiring every member's work or every revenue stream. |
| Separate observation, attribution and award eligibility | LRCA US-01, AT-01, AW-01/02 | A retrieved source can be recorded without inventing a royalty; a payable use can follow its actual agreement. |
| Prevent duplicate liabilities across retries, portfolios and attribution paths | LRCA AW-02, AC-02 | Supports a marketplace where the same contribution appears in several administrative or evidential paths. |
| Reproduce calculations and distinguish balances from confirmed transfers | LRCA AC-01/04 and SIP-Pool-0.1 | Contributors can inspect how earnings were calculated and whether money actually arrived. |
| Preserve provenance, privacy and operational sovereignty | LRCA TR-02/04, PS-01/03 and §10 sovereign deployment profile | Supports deployment choices without presenting permissive model weights or a source citation as complete rights clearance. |

Adding these commitments to a system does not prevent that system from also practicing a narrower claimed process. They should be evaluated as customer value and implementation requirements, separately from a patentability argument.

## Recommended next specification and implementation decisions

These are proposals for a later revision; this comparison does not change the normative specifications.

1. **Document the licensed-retrieval and provider-reporting flow first.** Produce example receipts, provider exports and agreement variants, then chart Preferred Networks' independent claims against those concrete operations. Do not remove contributor transparency merely to assume a patent issue has disappeared.
2. **Make attribution methods replaceable and explicit.** Keep declaration-based lineage, observed use and research estimators distinct. Record each method and version; preserve the requirement that an estimate alone cannot create an earning agreement.
3. **Document the full identifier lifecycle.** Show whether an ID comes from ingestion, retrieval, a model response or an external service, and which trusted record is consulted before any effect on response delivery or payment. Include M6 citation training in the Technica Pacifica assessment.
4. **Specify permission-service behavior and deployment.** Record the roles of deterministic rules, AI assistance, authorized review and database topology. Use those facts to assess Citibank's independent claims rather than treating Rust or PostgreSQL as legal distinctions by themselves.
5. **Complete the open-standard bindings.** Add ODRL, PROV-O and Web Annotation mappings with representative fixtures. Keep rights assertions, provenance and accepted economic obligations separately identifiable.
6. **Extend component procurement evidence.** For attribution and metering suppliers, request the covered patent schedule, customer license scope, permitted deployment, output rights and any applicable indemnity. Review image attribution, learned dataset pricing and collaborative model trading when those features enter scope.

For a commercial launch review, replace these abbreviated mappings with full charts of relevant independent and dependent claims against actual code and service flows. Confirm current official records, family members, who performs each step and where, and applicable claim interpretation. The present evidence supports prioritizing retrieval/reporting, model-emitted conditions and attribution components; it does not support declaring the whole Sovereign Source platform either blocked or patent-cleared.

# Chat history: Update Super Sovereign Source LLM IP

**Project:** Super Sovereign Source LLM IP  
**Export date:** October 10, 2026  
**Chat ID:** `01a1271c-eba2-7522-ac4f-3e0ed974107d`  
**Time zone:** America/Los_Angeles

This export contains this conversation's available user messages, assistant answers and assistant progress updates, from the first message through the request to save the chats. It contains 14 user messages, 14 assistant answers and 46 progress updates across 14 turns. Both history pages were retrieved; no further page remained.

Message wording and links are preserved as returned by the chat-history service. Tool calls, tool outputs, internal reasoning, system instructions and application context are excluded. Turn timestamps indicate when each turn started, not the time of every individual message. The export operation's progress and completion messages are not included.

Historical recommendations may have been superseded later in this conversation. Current project documents are indexed in the [README](../README.md).

## Conversation

## Turn 1 — October 10, 2026 at 11:40:38 AM PDT

### User

update the spec to have a syndicate model for IP, ideas, contributions, influences and ideas, an expanded concept of IP rights and attribution enabled by AI, lets call it Super Intellectual Property and this Project Super Sovereign Source LLM IP

### Assistant — progress update

I’ll find the project spec and update it with the Super Intellectual Property syndicate model and the project name “Super Sovereign Source LLM IP.”

### Assistant — progress update

The current spec already covers licensing, contribution agreements, attribution and royalties. I’ll extend it with voluntary syndicates that manage permissions, credit and revenue sharing across works, ideas, contributions and influences. “Super Intellectual Property” will name that broader framework, with AI helping trace and review contributions.

### Assistant — progress update

The spec now defines syndicate charters, member mandates, contribution portfolios and agreed payment splits. It also distinguishes acknowledged influence from AI-estimated influence. I’m updating the milestones and acceptance checks so the local pilot must demonstrate those distinctions.

### Assistant — progress update

The spec and README are updated. I checked the document links, section numbering and sample payment split; all passed. The spec now includes requirements and acceptance checks for syndicate permissions, AI-assisted attribution and member compensation.

### Assistant — answer

Updated the [specification to v0.3](/home/niccolox/Projects/sovsrc.llm/docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md) and [README](/home/niccolox/Projects/sovsrc.llm/README.md) with:

- **Super Sovereign Source LLM IP** as the project name.
- **Super Intellectual Property (SIP)** covering IP, ideas, contributions and influences.
- Syndicate membership, permissions, governance and revenue sharing.
- AI-assisted attribution, reviewed influence records and correction workflows.
- Updated milestones and acceptance criteria.

Document checks passed.

---

## Turn 2 — October 10, 2026 at 11:48:32 AM PDT

### User

research a solution architecture using Python Pydantic Pydantic AI Prefect Rust Axum Postgres and use Nemotron as target for training

### Assistant — progress update

I’ll research how this stack fits the SIP platform, including Nemotron’s training options, then update the spec with a concrete architecture and staged implementation plan.

### Assistant — progress update

I’m using the write-page skill to save the research alongside the repository spec. The main design question is where to put authority: Rust/Axum can own permissions and accounting, while Python handles AI workflows and training. I’m also checking which Nemotron checkpoint and training recipe are practical for a first run.

### Assistant — progress update

NVIDIA provides both base and post-trained Nemotron checkpoints, plus a Megatron Bridge recipe for LoRA fine-tuning. I recommend Nemotron 3 Nano 30B-A3B as the first main training target. Its active parameter count reduces computation, but the full model still matters for memory planning. The spec will also distinguish SIP-controlled training additions from the upstream data already embedded in Nemotron.

### Assistant — progress update

The architecture now gives each tool a clear role: Axum owns permissions and financial records, Pydantic AI drafts answers and attribution proposals, Prefect runs background workflows, and Postgres stores authoritative state. I’ve also added a staged Nemotron training plan, with checks for GPU capacity, checkpoint conversion, restart recovery and citation quality before a larger run.

### Assistant — answer

Saved the [solution architecture](/home/niccolox/Projects/sovsrc.llm/docs/SOLUTION_ARCHITECTURE.md) and updated the [spec to v0.4](/home/niccolox/Projects/sovsrc.llm/docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md).

| Technology | Recommended role |
|---|---|
| Rust + Axum | API, permissions, syndicate decisions and accounting |
| Python + Pydantic | Shared contracts, validation and training data preparation |
| Pydantic AI | Research answers and attribution proposals |
| Prefect | Ingestion, training, evaluation and settlement workflows |
| PostgreSQL + pgvector | Authoritative records, retrieval and financial ledger |
| Nemotron + vLLM | Model training target and inference |

**Training recommendation:** start with Nemotron 3 Nano 30B-A3B BF16 and supervised LoRA adaptation through NVIDIA’s [Megatron Bridge recipe](https://docs.nvidia.com/nemo/megatron-bridge/latest/models/nemotron/nemotron3-nano.html).

The architecture includes diagrams, service boundaries, recovery behavior and staged training evaluations. It preserves the distinction between SIP-admitted training additions and Nemotron’s upstream provenance.

Document checks passed. Exact GPU sizing and dependency compatibility remain implementation gates; no training was run.

---

## Turn 3 — October 10, 2026 at 11:54:21 AM PDT

### User

update README with for an LLM respects IP and ideas

### Assistant — progress update

I’ll update the README’s opening to clearly describe an LLM that respects intellectual property and ideas.

### Assistant — answer

Updated the [README](/home/niccolox/Projects/sovsrc.llm/README.md) with **“An LLM that respects intellectual property and ideas.”** The introduction now emphasizes permission, attribution and contributor compensation.

---

## Turn 4 — October 10, 2026 at 11:56:29 AM PDT

### User

create a new Sovereign Source Super Intellectual Property license which is open source, enforces attributions and influences and creates a syndicate marketplace

### Assistant — progress update

I’ll draft the Sovereign Source Super Intellectual Property license and connect it to the project spec. I’ll research how open-source licensing can support attribution and documented influences, and how separate syndicate terms can govern the marketplace.

### Assistant — progress update

The key constraint is that open-source use cannot depend on marketplace membership or royalty payments. I’ll make attribution and documented influence notices part of the license, with separate opt-in terms for syndicate listings, services and revenue sharing. The custom license will be labeled as a draft for legal review, without claiming OSI approval. ([Open Source Definition](https://opensource.org/osd))

### Assistant — progress update

The draft now requires source access, contributor credit and notices for known, documented influences, with correction and enforcement clauses. The companion marketplace terms cover listings, commissions, services, additional permissions and agreed revenue splits. I’m adding adoption templates and updating the spec to distinguish public license grants from optional paid agreements.

### Assistant — progress update

The license package and spec updates are complete. Document checks passed, and the example order reproduces the $2,000 split exactly. The templates remain explicitly unaccepted, and the spec now preserves public license rights when a listing is removed or a member leaves a syndicate.

### Assistant — answer

Created **Sovereign Source Super Intellectual Property License v0.1**:

- [License draft](/home/niccolox/Projects/sovsrc.llm/licenses/SS-SIP-0.1.md): source sharing, required attribution, documented influences and enforcement provisions.
- [Marketplace terms](/home/niccolox/Projects/sovsrc.llm/licenses/SYNDICATE-MARKETPLACE-TERMS-0.1.md): syndicate authority, listings, commissions, revenue splits and disputes.
- [Adoption guide and templates](/home/niccolox/Projects/sovsrc.llm/licenses/README.md).

Updated the README and spec to v0.5. Checks passed.

Marketplace payments remain optional to preserve [open-source freedoms](https://opensource.org/osd). The custom license requires qualified legal review before adoption and is **not OSI-approved**.

---

## Turn 5 — October 10, 2026 at 12:05:10 PM PDT

### User

update language to borrow from X Content Rewards language

### Assistant — progress update

I’ll check X’s official creator-reward language and adapt the license, marketplace terms and README to that style while keeping the legal obligations precise.

### Assistant — progress update

X’s current wording centers on original content, eligibility, qualified activity, earnings and payouts. I’m adapting that vocabulary into **SIP Creator Rewards**, with qualified contribution use tied to the project’s existing agreements and attribution records. [X’s program overview](https://help.x.com/en/using-x/original-content-rewards) is the language reference.

### Assistant — progress update

The drafts now use **SIP Creator Rewards**, “qualified use,” “estimated earnings” and “payouts.” The wording keeps original contributions, licensed sources and credited influences distinct, and preserves the existing revenue split and payment obligations. I’m checking the documents for consistency and broken links.

### Assistant — answer

Updated the [README](/home/niccolox/Projects/sovsrc.llm/README.md), specification and licensing documents with **SIP Creator Rewards**, borrowing vocabulary from [X’s Original Content Rewards](https://help.x.com/en/using-x/original-content-rewards).

The language now emphasizes original contributions, eligibility, qualified use, earnings and payouts. Attribution obligations and agreed compensation remain intact.

Documentation and link checks passed.

---

## Turn 6 — October 10, 2026 at 12:10:52 PM PDT

### User

create a research document which audits frontier labs and their terms of conditions building sovereign source ai LLM that respects IP and ideas and gives content rewards, loyalties and attribution for an expanded universe of intellectual property

### Assistant — progress update

I’ll audit frontier labs’ published terms for training rights, ownership, attribution and creator compensation, then turn the findings into design requirements for Sovereign Source AI. I’ll distinguish what the terms actually promise from what the project would need to add.

### Assistant — progress update

The key distinction is between owning an output, having permission to train on it, and owing its contributors credit or payment. Those are separate questions in the terms. I’m comparing consumer services, business APIs and downloadable model licenses separately because their rules differ substantially.

### Assistant — progress update

Two findings directly affect the design: several hosted services restrict using outputs to train another model, and some feedback clauses permit reuse without compensation. The document will propose a distinct contribution channel for SIP, where training permission, credit and reward terms are accepted before use, alongside ordinary service feedback.

### Assistant — progress update

I’m drafting the report around eight organizations: OpenAI, Anthropic, Google DeepMind, xAI/Grok, Meta, Mistral, DeepSeek and NVIDIA. It will include a terms comparison, documented compensation precedents, the expanded SIP framework and release requirements for a Nemotron-based system. The recommendations preserve the distinction between SIP-approved training additions and the base model’s upstream data.

### Assistant — progress update

The draft now contains the eight-provider comparison and 28 primary sources, plus proposed controls for consent, attribution, royalties and syndicate payouts. One important Nemotron finding is a litigation-related termination clause that could matter to a project representing creators; the report flags it for review without treating the model choice as legally approved.

### Assistant — answer

Created the [research audit](/home/niccolox/Projects/sovsrc.llm/docs/FRONTIER_LAB_IP_AND_CREATOR_REWARDS_AUDIT.md) and linked it from README.

It covers eight organizations and 28 primary sources, comparing ownership, training permissions, attribution and compensation. It also proposes SIP royalties, creator rewards, syndicate controls and Nemotron release requirements.

Documentation checks passed. Legal uncertainties and review requirements are identified.

---

## Turn 7 — October 10, 2026 at 12:47:19 PM PDT

### User

create a side by side compare of the best frontier labs to create a sovereign source ai, if none are possible, explore nemotron, university labs like berkeley and private companies, prepare an index with a single page with 10 parameters and top 10 labs and 10 purely open source plays like nemotron or berkeley mit or stanford, no Chinese models, only USA

### Assistant — progress update

I’ll build a one-page comparison of 10 US labs and 10 US open-model options, scored across 10 criteria for Sovereign Source AI. I’ll check licenses, local deployment, training permissions and model lineage, including Chinese-model dependencies—not just where the organization is based.

### Assistant — answer

For “no Chinese models,” should the comparison also exclude US models built on Chinese checkpoints or trained with Chinese-model outputs?
- Yes—exclude Chinese bases and training teachers (recommended)
- US organizations only; disclosed training teachers are acceptable

### Assistant — progress update

The main constraint is model ancestry: NVIDIA’s Nemotron 3 Nano documentation explicitly reports Qwen use. I’m treating that checkpoint as excluded under the stricter reading of your request. I’m also separating open-source training tools from ready-made models, so the index won’t imply that ten fully auditable, frontier-ready US models exist.

### Assistant — progress update

I’m using the OpenAI Docs skill to check the distinction between OpenAI’s hosted services and its downloadable models. The index will rank suitability for this project—not general benchmark performance—and mark missing provenance evidence as unresolved.

### Assistant — progress update

The strongest path is an auditable training program built on US-led open-source projects. No reviewed release yet establishes all three requirements together: complete permission records, verified model ancestry, and creator rewards. I’m putting the comparison and source notes into one local index page, with Berkeley, Stanford and MIT clearly labeled by what they actually provide.

### Assistant — progress update

I’ve settled on ten lab/provider candidates and ten open-source paths: six baseline model families, Stanford’s training framework, and three supporting tools from Berkeley and MIT. The page will distinguish these from ten complete LLMs. I also found a useful licensing update: Gemma 4 uses Apache 2.0, while earlier Gemma releases have different terms.

### Assistant — progress update

The index is written and linked from the README. It includes source notes for every entry, and the project documents now mark Nemotron Nano as held under the ancestry requirement. I’ve verified the requested counts—10 parameters, 10 labs and 10 open-source paths—and am checking the page presentation and links.

### Assistant — answer

Created the [single-page comparison index](/home/niccolox/Projects/sovsrc.llm/docs/usa-sovereign-ai-index.html) and [Markdown edition](/home/niccolox/Projects/sovsrc.llm/docs/USA_SOVEREIGN_AI_INDEX.md):

- 10 US lab/provider candidates.
- 10 open-source paths, including Stanford, Berkeley and MIT.
- 10 parameters covering control, licensing, ancestry, attribution and rewards.

The research favors Ai2/Stanford training infrastructure. Nemotron Nano is held because NVIDIA discloses Qwen use. Models and supporting tools are clearly distinguished; ten fully cleared frontier models could not be verified.

README and specifications updated. Counts and links checked; browser preview was blocked by the local-file policy.

---

## Turn 8 — October 10, 2026 at 2:10:12 PM PDT

### User

Search again for Nemotron with no qwen

### Assistant — progress update

I’ll check earlier and alternative Nemotron checkpoints for a path without Qwen base weights or training teachers, using NVIDIA’s model cards and reports.

### Assistant — progress update

I found an older NVIDIA lineage worth reconsidering: Nemotron-4 → Minitron → Nemotron Mini. The published lineage names NVIDIA models rather than Qwen. I’m checking the training disclosures and licenses before adding these as candidates.

### Assistant — progress update

Minitron’s base models look like the strongest candidates for a small training experiment. Nemotron Mini adds a licensing complication: its linked terms impose production restrictions despite the card’s “commercial use” description. I’ll distinguish those choices in the research and keep the Qwen-dependent Nano checkpoint excluded.

### Assistant — progress update

The comparison now includes Minitron-4B and 8B Base as conditional research candidates, with a separate report covering their ancestry and license terms. The index still has ten providers and ten open-source paths, and its documentation links and comparison structure passed checks.

### Assistant — answer

Yes—older NVIDIA models offer candidates with **no disclosed Qwen ancestry**:

| Model | Published lineage | Suggested role |
|---|---|---|
| [Minitron-4B-Base](https://huggingface.co/nvidia/Minitron-4B-Base) | Nemotron-4 15B | First small training experiment |
| [Minitron-8B-Base](https://huggingface.co/nvidia/Minitron-8B-Base) | Nemotron-4 15B | Larger research comparison |
| [Nemotron-4-340B-Base](https://huggingface.co/nvidia/Nemotron-4-340B-Base) | NVIDIA Nemotron-4 pretraining | Substantial-compute alternative |

**My recommendation is Minitron-4B-Base for research.** Its card specifies R&D use. Public disclosures do not establish that every upstream training source and teacher was Qwen-free.

Updated the [research report](/home/niccolox/Projects/sovsrc.llm/docs/NEMOTRON_NO_QWEN_RESEARCH.md), comparison index, README and architecture. The Qwen-dependent Nano checkpoint remains excluded; the entire Nemotron family is not.

---

## Turn 9 — October 10, 2026 at 2:14:16 PM PDT

### User

Use Nemotron 3 ultra

### Assistant — progress update

I’ll check Nemotron 3 Ultra’s exact release and training disclosures, then update the project’s model target and note how it fits the earlier no-Qwen requirement.

### Assistant — progress update

NVIDIA’s Nemotron 3 Ultra release is the 550B model with 55B active parameters. I’ll make it the selected target. Its training disclosures include Qwen and DeepSeek, so I’ll record that it does not meet the earlier no-Qwen condition.

### Assistant — progress update

The specification and architecture now target Ultra, including its OpenMDW license and training recipes. The compute plan also reflects Ultra’s scale: NVIDIA’s published LoRA example starts at 32 H100 GPUs. Those are planning figures; no training job has been started.

### Assistant — answer

Set **Nemotron 3 Ultra** as the project target in the README, [specification](/home/niccolox/Projects/sovsrc.llm/docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md), architecture and comparison index:

- **BF16:** reference model and training.
- **NVFP4:** serving candidate.

Documentation checks passed.

NVIDIA discloses Qwen and DeepSeek training dependencies, so the earlier no-Qwen requirement remains explicitly unsatisfied. [Model card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16).

---

## Turn 10 — October 10, 2026 at 2:17:51 PM PDT

### User

Use https://www.bestaifor.com/blog/nemotron-3-super-vs-qwen-3-5-when-speed-and-accuracy-point-in-opposite-directions

### Assistant — progress update

I’ll read the article and add its relevant findings to the model comparison, keeping its Super results distinct from the selected Ultra target.

### Assistant — progress update

The article’s useful takeaway is to measure cost per successful result, including retries. It also needs a few qualifications: it compares Super rather than Ultra, mixes Qwen sizes, and incorrectly says Apache-2.0 has no attribution requirements. I’ll add the takeaway and document those limits.

### Assistant — progress update

The article is now reflected in the research review and Ultra evaluation criteria. I’m updating the single-page index and checking that the links, comparison tables, and model selection remain consistent.

### Assistant — answer

Incorporated the article into the [research review](/home/niccolox/Projects/sovsrc.llm/docs/NEMOTRON_PERFORMANCE_SOURCE_REVIEW.md), README, specification, architecture and comparison index.

**Nemotron 3 Ultra remains selected.** The review distinguishes the article’s Super results, checks its claims against primary sources, and adds evaluation by cost per verified outcome—including retries, validation and attribution quality.

Documentation links and index checks passed.

---

## Turn 11 — October 10, 2026 at 2:21:28 PM PDT

### User

What is the best commercial platform for building sovereign source ai llm for content rewards?

### Assistant — progress update

I’ll compare the commercial options against the project’s needs: control over Nemotron Ultra, source permissions, attribution, and creator payouts.

### Assistant — progress update

NVIDIA looks like the strongest fit for operating Ultra under your control. The rewards system needs a separate layer: TollBit supports licensed content access and usage payments, while ProRata offers attribution-based publisher revenue sharing. I haven’t found a platform that supplies your full syndicate and influence-rewards model out of the box.

### Assistant — answer

**For your project, I recommend NVIDIA AI Enterprise with NeMo as the commercial AI foundation**, running Nemotron 3 Ultra on US infrastructure under your control. It offers commercial support, deployment tooling and model customization; NVIDIA also publishes Ultra-specific training recipes. [AI Enterprise](https://www.nvidia.com/en-us/data-center/products/ai-enterprise/), [Ultra training support](https://docs.nvidia.com/nemo/megatron-bridge/latest/models/nemotron/nemotron3-ultra.html).

**The content-rewards system still needs to be built around it.** None of the platforms reviewed supplies your complete combination of source permissions, idea and influence attribution, syndicate ownership and royalty accounting.

| Platform | Best fit for your project | Main limitation |
|---|---|---|
| **NVIDIA AI Enterprise + NeMo** | My first choice for controlling and adapting Ultra | Requires GPU infrastructure and engineering; creator rewards remain your application’s responsibility. |
| **Databricks Mosaic AI + Unity Catalog** | Strong alternative when managed data governance and operational lineage matter most | Its lineage tracks data and model dependencies; that does not establish intellectual influence or royalty entitlement. [Documentation](https://docs.databricks.com/aws/en/data-governance/unity-catalog/data-lineage). |
| **TollBit** | Most practical integration candidate for purchasing licensed content and recording usage payments | Rights depend on the particular license; access for summarization does not automatically authorize training. [Licensing and rates](https://docs.tollbit.com/docs/setting-rates). |
| **ProRata** | Closest commercial match to your attribution-and-rewards vision | It advertises licensed content and 50% revenue sharing, but the reviewed material does not establish a self-hostable platform for your own Ultra model. [ProRata](https://prorata.ai/). |

I would build the first release with:

- **NVIDIA/NeMo:** model deployment and later adaptation.
- **Your Rust/Axum/Postgres SIP system:** permissions, attribution records, syndicate agreements and reward calculations.
- **TollBit or direct creator agreements:** licensed content supply.
- **Stripe Connect:** contributor onboarding and payouts across multiple recipients. [Connect](https://stripe.com/connect).

Start with licensed retrieval and rewards for **recorded content use**. Add training later. Keep estimated influence subject to review and agreed compensation rules.

One unresolved constraint remains: **Ultra discloses Qwen and DeepSeek training dependencies**, so this recommendation fits your Ultra selection but does not satisfy the earlier strict no-Qwen requirement. [Model disclosures](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16#training-and-evaluation-datasets).

---

## Turn 12 — October 10, 2026 at 2:41:36 PM PDT

### User

Update spec with this research

### Assistant — progress update

I’ll add the commercial-platform recommendation to the spec, including the roles of NVIDIA, content-licensing partners, and payouts, and keep the research separate from any purchasing decision.

### Assistant — progress update

I’m making NVIDIA AI Enterprise the recommended commercial foundation, with TollBit and Stripe Connect as integration candidates. The spec will retain Databricks and ProRata as alternatives and make clear that provider payments do not automatically grant training rights or determine SIP rewards.

### Assistant — answer

Updated the [specification to v0.7](/home/niccolox/Projects/sovsrc.llm/docs/SOVEREIGN_SOURCE_AI_CODEX_SPEC.md:213) with:

- NVIDIA AI Enterprise/NeMo recommendation and platform comparison.
- TollBit licensing and Stripe Connect payout requirements.
- Commercial acceptance checks for permissions, attribution, payments and deployment control.

Aligned the README and architecture. Documentation checks passed.

---

## Turn 13 — October 10, 2026 at 2:44:09 PM PDT

### User

Research the training data providers to the LLMs. Research the LLM development community, the companies, the suppliers that sell to Claude or ChatGPT. Not just the end product or the frontier labs themselves, but the suppliers to these labs. Find new sources, industry magazines, industry websites and blogs, private forums, groups, etc. Research the suppliers, the upstream to the frontier labs.

### Assistant — progress update

I’ll map the companies and communities supplying training data, licensed content, expert work, and evaluation services to frontier labs. I’ll separate confirmed supplier relationships from reported or undisclosed ones, and include trade publications, forums, and groups useful for following this market.

### Assistant — progress update

The upstream market has two distinct parts: companies that recruit experts to create training examples and evaluations, and rights holders that license existing content. I’m also checking the type of each lab relationship—a Claude implementation partner or search-content provider is not necessarily a supplier of model-training data.

### Assistant — progress update

I’ve found several useful upstream leads: Surge documents work with Anthropic and OpenAI; Turing describes supplying coding data to OpenAI; and reporting identifies Mercor and Invisible as data vendors. The market also extends beyond text datasets into expert-designed tasks and software environments, including a recently announced Synopsys–OpenAI partnership.

### Assistant — progress update

The supplier map is taking shape. Public evidence is strongest for specific projects and dated partnerships; it rarely reveals a lab’s complete supplier roster. I’m turning the findings into a report that distinguishes training suppliers, licensed-content sellers, and search or integration partners, with a separate directory of industry publications and gated communities.

### Assistant — progress update

The strongest opportunity for Sovereign Source is upstream too: creator syndicates could supply licensed works, expert-written training examples, and evaluation tasks. The report will distinguish those opportunities from ordinary chatbot integrations and show where attribution and contributor-payment terms still need to be negotiated.

### Assistant — answer

Created the [upstream supplier research report](/home/niccolox/Projects/sovsrc.llm/docs/UPSTREAM_AI_DATA_SUPPLIERS_RESEARCH.md) and linked it from the README and terms audit. It maps **24 suppliers and related organizations**, plus publications and development communities.

The strongest findings:

| Company | Evidence of upstream work |
|---|---|
| **Surge AI** | Documents human-feedback work for Anthropic and creation of OpenAI’s GSM8K mathematics dataset. [Anthropic case study](https://surgehq.ai/blog/anthropic-surge-ai-rlhf-platform-train-llm-assistant-human-feedback), [OpenAI project](https://surgehq.ai/blog/how-we-built-it-openais-gsm8k-dataset-of-8500-math-problems). |
| **Turing** | Says OpenAI engaged it to supply coding data for ChatGPT in 2022. [Company account](https://help.turing.com/articles/2834113361-the-turing-story). |
| **Mercor** | Supplies expert-created data and evaluations; WIRED identifies OpenAI and Anthropic as customers. [Reporting](https://www.wired.com/story/meta-pauses-work-with-mercor-after-data-breach-puts-ai-industry-secrets-at-risk/). |
| **Invisible Technologies** | Reuters reports expert-training work for OpenAI, with the relationship described by the supplier and additional sourcing. [Investigation](https://www.marketscreener.com/quote/stock/MICROSOFT-CORPORATION-4835/news/If-your-AI-seems-smarter-it-s-thanks-to-smarter-human-trainers-47959189/). |
| **Created by Humans / Defined.ai** | Relevant content-licensing candidates; this research did **not** verify either as an OpenAI or Anthropic supplier. [Created by Humans](https://www.createdbyhumans.ai/), [Defined.ai](https://defined.ai/dataset-type/text). |

The report also covers Handshake, Labelbox, Snorkel, micro1, publishers, and historical relationships such as Scale and Sama.

For ongoing industry research, the useful sources include **Digiday, The Scholarly Kitchen, Interconnects, Reuters and supplier research blogs**. Community routes include the Dataset Providers Alliance, MLOps Community, Prime Intellect, MLCommons and contributor platforms. Gated groups are identified; private discussions were not accessed.

**My recommendation:** explore Sovereign Source as an upstream supplier too—syndicates could sell permissioned works, expert training examples and evaluation tasks with explicit attribution and contributor-payment agreements.

---

## Turn 14 — October 10, 2026 at 3:34:27 PM PDT

### User

save all chats as a markdown

---

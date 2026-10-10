# USA Sovereign Source AI Index

**Super Sovereign Source LLM IP · Research snapshot: October 10, 2026**  
**10 lab/provider candidates · 10 open-source paths · 10 comparison parameters**  
[Single-page browser edition](usa-sovereign-ai-index.html) · [Detailed terms audit](FRONTIER_LAB_IP_AND_CREATOR_REWARDS_AUDIT.md) · [Architecture](SOLUTION_ARCHITECTURE.md)

**Recommendation:** prioritize Ai2's auditable training ecosystem and Stanford-origin Marin/Levanter for a model trained from scratch on SIP-admitted material. Evaluate downloadable US-company models only after ancestry and rights review. None of the reviewed releases establishes the complete SIP combination of source permission, verified ancestry, attribution and contractual creator rewards. This is a finding about available evidence, not proof that no suitable private arrangement exists.

**Nemotron decision:** hold the previously proposed Nemotron 3 Nano 30B-A3B checkpoint. Its official card says it was improved using Qwen, so it fails the strict model-ancestry screen used here. NVIDIA remains a potential infrastructure supplier; that does not qualify this checkpoint. [NVIDIA model card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B-BF16).

## Scope and how to read the index

“USA” means a US-headquartered provider or a project led by or originating at a US institution. It does not certify every collaborator, training location or data source as American. Google is included through its US parent/provider; Google DeepMind is an international organization with UK origins. A requirement for exclusively US research operations would exclude that route and require additional institutional diligence elsewhere.

**Working interpretation of “no Chinese models”:** exclude Chinese-developed checkpoints and their derivatives, including synthetic training teachers. Record model-based data transformations, reward models, embeddings and evaluation judges too. Unknown ancestry is **pending**, never a pass. Chinese language, an author's name and contributor ethnicity are not evidence of model origin. This is a project selection rule, not a restriction added to public open-source licenses.

The ten labs are a project-specific shortlist spanning frontier providers and open-model research, not a claim that all ten have equivalent frontier capability. Entries compare the **named route**, not every product a company offers. Order favors inspectability and independent deployment; no numerical capability ranking is asserted. Older releases are deliberate research baselines, not recommendations for frontier-quality production assistants. No models were benchmarked in this review.

The open-source list contains **six baseline model families, one training framework route and three supporting tools**. It does not claim ten fully verified, purely open-source frontier LLMs exist. Software licenses, model licenses and training-data permissions are assessed separately. Apache/MIT weights alone do not establish a complete open-source AI system: the OSI definition also requires training code and adequate data information. Nor does open-source status establish permission for every training work. [OSI Open Source AI Definition 1.0](https://opensource.org/ai/open-source-ai-definition).

## The ten parameters

| Parameter | Question answered |
| --- | --- |
| **1 · Capability** | What does the selected release actually provide: assistant, base model, training or serving tool? |
| **2 · Local control** | Can we operate the selected weights or software on infrastructure we control? |
| **3 · License** | What license or service agreement governs that selected artifact? |
| **4 · Adaptation** | Can we modify/train locally, or only customize a managed service? |
| **5 · Redistribution** | Can we commercially distribute the selected weights or code, subject to its terms? |
| **6 · Training visibility** | Are training code, data information and recipes available for inspection? |
| **7 · Model ancestry** | Does the evidence clear the no-Chinese-base/teacher screen? |
| **8 · Source permission** | Is there asset-level evidence sufficient for SIP's permission standard? |
| **9 · Creator rewards** | Is the full SIP attribution, influence and royalty system supplied? |
| **10 · SIP decision** | What role should this route have in the project? |

**Legend:** **A2** = Apache-2.0; **Gap** = reviewed sources do not establish asset-level SIP permission; **Build** = implement SIP agreements, attribution and rewards separately; **Pending** = not ancestry-cleared; **Inputs** = software route, with every chosen model/dataset still subject to review; **Terms** = conditional permission, not an unrestricted grant. “Yes” under redistribution covers the named artifact, not its training corpus. No row is approved for a production release.

## Ten US lab and provider candidates

| Lab / selected route | 1 Capability | 2 Local control | 3 License | 4 Adaptation | 5 Redistribution | 6 Training visibility | 7 Model ancestry | 8 Source permission | 9 Creator rewards | 10 SIP decision |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Ai2** · original OLMo-7B [L1] | Research base | Yes | A2 | Local training | Yes | Code + Dolma | Pending | Gap | Build | Prioritize recipe |
| **OpenAI** · gpt-oss-20b [L2] | Local reasoning | Yes | A2 | Local tuning | Yes | Partial | Pending | Gap | Build | Conditional evaluation |
| **Google** · Gemma 4 [L3] | Multimodal family | Yes | A2 | Local tuning | Yes | Partial | Pending | Gap | Build | Conditional; US parent |
| **Microsoft Research** · Phi-4 [L4] | Small assistant | Yes | MIT | Local tuning | Yes | Partial | Pending | Gap | Build | Conditional evaluation |
| **Databricks / MosaicML** · MPT-7B Base [L5] | Legacy base | Yes | A2 | Local training | Yes | Code + mixture | Pending | Gap | Build | Research baseline |
| **NVIDIA** · Nemotron 3 Nano 30B-A3B [L6] | Reasoning / agents | Yes | Custom | Terms | Terms | Recipe + data subsets | **Fails: Qwen** | Gap | Build | **Hold checkpoint** |
| **Meta** · Llama 4 [L7] | Multimodal family | Yes | Custom | Terms | Terms | Partial | Pending | Gap | Build | License-dependent |
| **Amazon** · Nova Forge [L8] | Managed customization | AWS-hosted | Service | Managed training | Not established | Partial / managed | Pending | Gap | Build | Managed alternative |
| **Anthropic** · Claude commercial API [L9] | Hosted assistant | No public weights | Service | Competitor restriction | No weights grant | Closed | Pending | Gap | Build | Service only |
| **xAI** · Grok-1 open release [L10] | Legacy 314B base | Yes | A2 | Local modification | Yes | Inference code | Pending | Gap | Build | Low-priority baseline |

Hosted GPT, Gemini and Grok have separate agreements from gpt-oss, Gemma and Grok-1. The reviewed hosted terms restrict competing-model development or output training; do not use API outputs as a sovereign training corpus without applicable permission. Claude's reviewed commercial terms also require approval for competing products. Nova Forge provides AWS customization, not evidence of unrestricted weight export or offline ownership. [OpenAI §3.3](https://openai.com/policies/services-agreement/), [Gemini terms](https://ai.google.dev/gemini-api/terms), [Grok §3.2](https://x.ai/legal/terms-of-service-enterprise), [Anthropic §D.4](https://www.anthropic.com/legal/commercial-terms), [Nova Forge](https://aws.amazon.com/nova/forge/).

## Ten US-led open-source paths

All ten selected paths expose software under Apache-2.0 or MIT. The six baseline families also publish weights under Apache-2.0. This is a component-level shortlist, not an OSI certification of their complete AI systems or permission clearance of their corpora.

| Project / US anchor | 1 Capability | 2 Local control | 3 License | 4 Adaptation | 5 Redistribution | 6 Training visibility | 7 Model ancestry | 8 Source permission | 9 Creator rewards | 10 SIP decision |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **OLMo-7B, original** · Ai2 [O1] | Research base | Yes | A2 | Local training | Weights + code | Code + Dolma | Pending | Gap | Build | Preferred audit baseline |
| **Marin / Levanter** · Stanford origin [O2] | From-scratch trainer | Yes | A2 | Own training run | Code | Public experiments | Inputs | Own corpus | Build | Preferred training path |
| **Pythia** · EleutherAI [O3] | Model-dynamics suite | Yes | A2 | Local training | Weights + code | Code + Pile ordering | Pending | Gap | Build | Attribution experiments |
| **MPT-7B Base** · MosaicML [O4] | Legacy base | Yes | A2 | Local training | Weights + code | Code + mixture | Pending | Gap | Build | Engineering baseline |
| **RedPajama-INCITE-7B-Base** · Together AI [O5] | Legacy base | Yes | A2 | Local training | Weights + code | GPT-NeoX + corpus | Pending | Gap | Build | Data-pipeline reference |
| **Cerebras-GPT** · Cerebras [O6] | Scaling-law suite | Yes | A2 | Local modification | Weights + code | Recipe + Pile | Pending | Gap | Build | Scaling research |
| **OpenLLaMA 7B v1 / EasyLM** · Berkeley researchers [O7] | Legacy base / trainer | Yes | A2 | Local training | Weights + code | Code + RedPajama | Pending | Gap | Build | JAX training reference |
| **vLLM** · Berkeley origin [O8] | Inference server | Yes | A2 | Modify serving code | Code | No pretrained model | Inputs | Own inputs | Build | Serving shortlist |
| **SkyRL** · Berkeley Sky Lab [O9] | RL training library | Yes | A2 | Own RL run | Code | Public RL code | Inputs | Own inputs | Build | Later post-training |
| **StreamingLLM** · MIT Han Lab [O10] | Streaming inference | Yes | MIT | Modify serving code | Code | No pretrained model | Inputs | Own inputs | Build | Optional efficiency study |

**University boundaries:** Stanford contributes transparent training infrastructure; the selected Marin route starts from new weights and an admitted corpus. Its published 8B Instruct data includes Bespoke-Stratos, which uses DeepSeek-R1 outputs, so that checkpoint is excluded under this screen. Berkeley's SkyRL code is distinct from downloaded example models; its dependencies and recipes require review. MIT's StreamingLLM is an inference technique, not an MIT foundation LLM, and it discards middle context rather than creating unlimited memory. [Marin dataset list](https://huggingface.co/marin-community/marin-8b-base), [Bespoke-Stratos origin](https://huggingface.co/datasets/bespokelabs/Bespoke-Stratos-17k), [SkyRL](https://github.com/NovaSky-AI/SkyRL), [StreamingLLM FAQ](https://github.com/mit-han-lab/streaming-llm).

## Project decision

1. **Build the SIP control system first.** Keep Rust/Axum and PostgreSQL authoritative for permission, accepted attribution, syndicate splits and exact accounting. Use Python/Pydantic/Pydantic AI for bounded model work and Prefect for manifests, training supervision and settlement workflows.
2. **Prove training at a small scale.** Evaluate an Ai2 or Marin training stack with newly initialized weights and exclusively admitted data. Include tokenizer training, filtering models, teachers and transformations in the ancestry manifest. A fresh initialization does not clear unreviewed data. Original OLMo/Pythia can support separately labeled research after admission review; their old public corpora are not automatically SIP-qualified.
3. **Keep capable open-weight options conditional.** gpt-oss, Gemma 4 and Phi-4 offer local deployment under permissive licenses. Request or establish ancestry and permission evidence before treating them as a fully sovereign source foundation. Local deployment alone is an operational property, not a full provenance claim.
4. **Preserve the Nemotron study as a held alternative.** Do not launch the planned Nano adaptation under the current strict screen. Another NVIDIA checkpoint would need its own complete review; the family name grants no exemption.
5. **Release only on evidence.** Pin revisions, licenses, dependencies and data manifests; establish source authority and accepted reward agreements; benchmark capability and citation accuracy; test privacy, revocation and exact settlement. The next deliverable is an admitted small-model experiment, not a promised frontier-scale training run.

No reviewed standard release supplies SIP's entire reward system. Provider notices and source citations are not contributor royalties. SIP must preserve upstream notices, distinguish verified use from estimated influence, and calculate payments from accepted agreements. This index changes model selection priorities; it does not adopt SS-SIP, relicense third-party material, purchase compute or authorize a training run.

## Evidence register

All sources below were checked on October 10, 2026. Model families can contain incompatible licenses and ancestries: findings apply only to named artifacts. Mutable repository references must be pinned before adoption. “Gap” and “Pending” express limits of this desk review, not allegations of infringement or concealed ancestry.

- **L1 / O1 — Ai2:** original [OLMo-7B model card](https://huggingface.co/allenai/OLMo-7B) identifies Apache-2.0 code/weights, Dolma and training artifacts. [Current Olmo program](https://allenai.org/olmo) includes later families; the original-model assessment does not clear Olmo 2, Olmo 3 or their post-training mixtures.
- **L2 — OpenAI:** [gpt-oss-20b documentation](https://developers.openai.com/api/docs/models/gpt-oss-20b) establishes local use, Apache-2.0 and tuning. It does not supply a complete asset-level permission or teacher-origin register. [Services agreement](https://openai.com/policies/services-agreement/) is effective January 1, 2026 and governs the separate hosted route.
- **L3 — Google:** [Gemma 4 model card](https://ai.google.dev/gemma/docs/core/model_card_4), updated July 30, 2026, and [Apache-2.0 license](https://ai.google.dev/gemma/apache_2). Its data description is categorical rather than an asset-level SIP register. Do not apply the [older Gemma terms](https://ai.google.dev/gemma/terms), modified April 1, 2026, to Gemma 4; that page expressly distinguishes them.
- **L4 — Microsoft:** [Phi-4 card](https://huggingface.co/microsoft/phi-4) specifies MIT licensing and synthetic/public/acquired data categories. [Technical report](https://www.microsoft.com/en-us/research/publication/phi-4-technical-report/) discusses GPT-4 teaching; this is not a complete certification of every ancestor or dataset.
- **L5 / O4 — Databricks:** [MPT-7B release](https://www.databricks.com/blog/mpt-7b), May 5, 2023, identifies a from-scratch Apache-2.0 base model. The assessment does not extend to MPT-Chat, StoryWriter, DBRX or every dataset named by those variants.
- **L6 — NVIDIA:** [Nano card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B-BF16), released December 15, 2025, discloses Qwen use. [Nemotron license](https://www.nvidia.com/en-us/agreements/enterprise-software/nvidia-nemotron-open-model-license/) is custom; it is not identified here as an OSI-approved license. The [Nano technical report](https://research.nvidia.com/labs/nemotron/files/NVIDIA-Nemotron-3-Nano-Technical-Report.pdf) details synthetic-data methods.
- **L7 — Meta:** [Llama 4 license](https://github.com/meta-llama/llama-models/blob/main/models/llama4/LICENSE), release date April 5, 2025, imposes notice/branding, policy and other conditions, including a large-platform threshold and an EU-domicile limitation for the multimodal grant. It is not an unrestricted Apache/MIT path.
- **L8 — Amazon:** [Nova Forge](https://aws.amazon.com/nova/forge/) describes early checkpoints, blending customer and Amazon-curated data, and hosting on AWS. The public product description is insufficient evidence of a portable, fully source-auditable model license.
- **L9 — Anthropic:** [Commercial terms](https://www.anthropic.com/legal/commercial-terms), effective June 17, 2025, govern the selected Claude service route. No public Claude checkpoint grant is established by this instrument.
- **L10 — xAI:** [Grok-1 repository](https://github.com/xai-org/grok-1) expressly licenses its code and associated weights under Apache-2.0. This 314B base snapshot is distinct from the current hosted Grok service and its [enterprise terms](https://x.ai/legal/terms-of-service-enterprise), updated August 14, 2026.
- **O2 — Stanford origin:** [Marin launch](https://marin.community/blog/2025/05/19/announcement/), May 19, 2025, documents Stanford CRFM origins and open experiments; [Marin license](https://raw.githubusercontent.com/marin-community/marin/main/LICENSE) and [Levanter license](https://raw.githubusercontent.com/marin-community/levanter/main/LICENSE) are Apache-2.0. The recommendation concerns software plus a new corpus, not automatic reuse of released mixtures or tokenizers.
- **O3 — EleutherAI:** [Pythia repository](https://github.com/EleutherAI/pythia) supplies Apache-2.0 code/weights, checkpoints and training-order information. Its [NTIA submission](https://downloads.regulations.gov/NTIA-2023-0009-0291/attachment_1.pdf), March 2024, identifies the institute as a US research organization. Pile component permissions and current availability require separate examination.
- **O5 — Together AI:** [RedPajama base card](https://huggingface.co/togethercomputer/RedPajama-INCITE-7B-Base) identifies Together leadership, Apache-2.0 and international collaborators. US-led does not mean exclusively US-authored. The base assessment does not clear its instruction/chat variants.
- **O6 — Cerebras:** [Cerebras-GPT announcement](https://www.cerebras.ai/blog/cerebras-gpt-a-family-of-open-compute-efficient-large-language-models), March 28, 2023, identifies Apache-2.0 releases and Pile-based scaling experiments. [Training paper](https://arxiv.org/abs/2304.03208) documents the wafer-scale setup; reproducing the original hardware run differs from adapting downloadable weights.
- **O7 — Berkeley researchers:** [OpenLLaMA](https://github.com/openlm-research/open_llama) documents Apache-2.0 weights and EasyLM, with separate v1/v2 data mixtures. [EasyLM](https://github.com/young-geng/EasyLM) is the training framework. The selected 7B v1 is an independently trained reproduction, not a grant to relicense Meta Llama checkpoints.
- **O8 — Berkeley origin:** [vLLM repository](https://github.com/vllm-project/vllm) documents its Sky Computing Lab origins and local serving; [license](https://raw.githubusercontent.com/vllm-project/vllm/main/LICENSE) is Apache-2.0. Supporting an architecture does not require selecting that architecture's weights.
- **O9 — Berkeley:** [SkyRL repository](https://github.com/NovaSky-AI/SkyRL) identifies the Sky Computing Lab/Anyscale collaboration and inherited components; [license](https://raw.githubusercontent.com/NovaSky-AI/SkyRL/main/LICENSE) is Apache-2.0. Configure only admitted models, teachers and environments; example recipes are not ancestry approval.
- **O10 — MIT:** [Han Lab project](https://hanlab.mit.edu/projects/streamingllm), [source and limitations](https://github.com/mit-han-lab/streaming-llm), and [MIT license](https://raw.githubusercontent.com/mit-han-lab/streaming-llm/main/LICENSE). This is an optional inference research component, not a replacement for source retrieval or durable attribution records.

Chinese-developed models are excluded from selection; Nemotron's known Qwen dependency and Marin Instruct's known DeepSeek-derived data are retained only as exclusion evidence. Non-US-led providers such as Mistral, Cohere and UAE-led Falcon are outside this US-focused shortlist. The earlier multinational terms audit remains available for historical comparison.

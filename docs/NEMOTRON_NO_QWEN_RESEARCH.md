# Nemotron candidates without disclosed Qwen ancestry

**Project:** Super Sovereign Source LLM IP  
**Reviewed:** October 10, 2026  
**Scope:** historical alternatives under the no-Qwen screen; the current project target is Nemotron 3 Ultra.

**Selection update:** the user subsequently selected **Nemotron 3 Ultra**, superseding the recommendation below. Its disclosures include Qwen and DeepSeek training dependencies, so it does not pass this document's screen. Preserve the findings as alternative research; do not interpret the selection as proof of Qwen-free ancestry. See the [current architecture](SOLUTION_ARCHITECTURE.md#nemotron-checkpoint-selection) and [Ultra card](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16).

**Yes, the Nemotron family contains relevant alternatives.** The best small research candidates found are **Minitron-4B-Base and Minitron-8B-Base**, descended from NVIDIA's Nemotron-4 15B. **Nemotron-4-340B-Base** is a much larger alternative. Their reviewed disclosures do not identify Qwen as a base or teacher. This finding corrects any family-wide inference from the previously rejected Nano checkpoint; it does not certify every upstream data transformation. [Minitron paper, sections 3–4](https://arxiv.org/html/2407.14679v1), [340B base card](https://huggingface.co/nvidia/Nemotron-4-340B-Base).

## What “no Qwen” means in this review

There are three separate questions: whether weights descend from Qwen, whether Qwen generated or filtered training material, and whether the complete upstream process is documented. A non-Qwen weight parent answers only the first. **No disclosed Qwen dependency** is a conditional research finding; **verified absence throughout training** requires more evidence than the reviewed public cards provide.

The existing US-led, no-Chinese-model screen still applies to other teachers and learned dependencies. A paper comparing scores against Qwen is not evidence of Qwen training ancestry. Names, language coverage and researcher ethnicity do not establish model origin. These are historical model releases, not a claim of current frontier performance; no capability benchmarks were run for this review.

## Candidate comparison

| Exact NVIDIA artifact | Disclosed weight lineage | Qwen finding | Project fit and remaining limitation |
| --- | --- | --- | --- |
| [Minitron-4B-Base](https://huggingface.co/nvidia/Minitron-4B-Base) | Nemotron-4 15B → pruning and distillation | None identified in reviewed lineage and training disclosures | **First small training research candidate.** Base model needs SIP instruction tuning. Card specifies R&D use; full corpus and transformation history remain incomplete. |
| [Minitron-8B-Base](https://huggingface.co/nvidia/Minitron-8B-Base) | Nemotron-4 15B → pruning and distillation | None identified in reviewed lineage and training disclosures | **Second research baseline.** Larger capacity comparison; same R&D wording and upstream evidence limitations. |
| [Nemotron-4-340B-Base](https://huggingface.co/nvidia/Nemotron-4-340B-Base) | NVIDIA Nemotron-4 pretraining | None identified in reviewed training disclosures | Large base for a funded research program. Card lists 8 H200 or 16 H100 GPUs for BF16 inference; this is not a training-resource estimate. |
| [Nemotron-Mini-4B-Instruct](https://huggingface.co/nvidia/Nemotron-Mini-4B-Instruct) | Minitron-4B-Base → instruction tuning | No Qwen named; full alignment-teacher register not supplied | Small RAG/tool-use prototype candidate, but **production-license restrictions** make it a weaker sovereignty fit than its card headline suggests. |
| [Llama-3.1-Nemotron-70B-Instruct-HF](https://huggingface.co/nvidia/Llama-3.1-Nemotron-70B-Instruct-HF) | Meta Llama-3.1-70B-Instruct → NVIDIA RLHF | No Qwen identified in reviewed 2024 recipe | Separate Llama-based assistant option. NVIDIA and Llama terms apply; HelpSteer2 creates additional teacher ancestry to review. |
| [Nemotron-4-340B-Instruct](https://huggingface.co/nvidia/Nemotron-4-340B-Instruct) | Nemotron-4-340B-Base → alignment | No Qwen identified; **Mixtral teacher disclosed** | Not a wholly US-model ancestry route if “USA only” extends to all teachers. Keep distinct from the Base checkpoint. |
| [nemotron-3-8b-base-4k](https://huggingface.co/nvidia/nemotron-3-8b-base-4k) | Original NVIDIA Nemotron-3 generation | No Qwen identified in reviewed card | Historical alternative with restrictive production terms. This is the older 8B release, not the later Nemotron 3 Nano family. |

The first two cards describe 94 billion tokens of continued distillation using the Nemotron-4 15B continued-pretraining corpus. The compression paper describes using the uncompressed model as teacher. The 15B report documents its own tokenizer and pretraining process, including benchmark-style examples in continued training, but does not provide a complete source/teacher manifest. That gap prevents a full ancestry certification. [Compression method](https://arxiv.org/html/2407.14679v1), [Nemotron-4 15B report, section 2](https://arxiv.org/html/2402.16819v1).

## Alignment adds dependencies

Nemotron-4 340B's report names **Mixtral-8x7B-Instruct-v0.1** as the initial generator in its iterative alignment pipeline. The report's Qwen references are benchmark comparisons, rather than a disclosed Qwen teacher. The Minitron paper also describes an instruction-tuning experiment using Nemotron-4 340B instruction data; that is a reason to trace instruction variants separately, not evidence that every released Mini checkpoint has an identical recipe. [340B report, section 3.2.4](https://arxiv.org/html/2406.11704v1), [Minitron instruction-tuning experiment](https://arxiv.org/html/2407.14679v1).

The 2024 Llama-3.1-Nemotron-70B card identifies HelpSteer2-Preference and an NVIDIA reward model for RLHF. HelpSteer2's paper lists Mixtral among response generators, while the current dataset card summarizes responses as coming from in-house models. Preserve that discrepancy and review the exact dataset revision; neither document establishes fully US-only teacher ancestry. Human preference annotation does not mean the underlying responses are human-written. [70B card](https://huggingface.co/nvidia/Llama-3.1-Nemotron-70B-Instruct-HF/raw/main/README.md), [HelpSteer2 paper, section 2](https://arxiv.org/html/2406.08673v1), [dataset source description](https://huggingface.co/datasets/nvidia/HelpSteer2/raw/main/README.md).

## License findings that change the shortlist

**Minitron Base and Nemotron-4-340B-Base:** the linked June 2024 NVIDIA Open Model License grants commercial use and derivative distribution subject to its terms, including notices and termination provisions. The Minitron cards separately state R&D-only intended use. Record both rather than presenting Minitron as an unqualified production choice. These are custom model terms, not Apache-2.0 or an asserted OSI approval. [June 2024 agreement](https://developer.download.nvidia.com/licenses/nvidia-open-model-license-agreement-june-2024.pdf), [4B card](https://huggingface.co/nvidia/Minitron-4B-Base), [8B card](https://huggingface.co/nvidia/Minitron-8B-Base).

**Nemotron Mini:** its metadata says NVIDIA Open Model License, but the body links the **August 23, 2024 NVIDIA Community Model License**. That agreement conditions production on NIM through an AI Enterprise subscription, subject to specified exceptions. It also restricts training other AI models outside its derivative-model allowance and disallows making the NVIDIA model subject to an open-source software license. Resolve the applicable grant before production; do not substitute the more permissive June agreement based on a metadata tag. [Mini's linked agreement, sections 1.2 and 2.1](https://huggingface.co/nvidia/Nemotron-Mini-4B-Instruct/resolve/main/nvidia-community-model-license-aug2024.pdf).

**Original Nemotron-3 8B:** its linked AI Foundation Models agreement requires a paid NeMo/AI Enterprise subscription for production and restricts other-model training and open-source relicensing. It is a poor fit for the proposed freely redistributable foundation. [Agreement, sections 1–2](https://developer.nvidia.com/downloads/nv-ai-foundation-models-license).

SIP agreements can govern authorized project contributions. They cannot replace inherited model terms or establish permissions for undisclosed pretraining works. These findings concern the published instruments reviewed, not bespoke NVIDIA agreements.

## Newer checkpoints that still fail the screen

| Named checkpoint | Evidence of training use | Decision |
| --- | --- | --- |
| [NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) | Training tables identify Qwen and DeepSeek as generators and filters | Current user-selected target; fails this no-Qwen screen. |
| [NVIDIA-Nemotron-3-Nano-30B-A3B-BF16](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B-BF16) | Official card expressly discloses Qwen-assisted improvement | Keep excluded from the no-Qwen shortlist. |
| [Llama-3_1-Nemotron-Ultra-253B-v1](https://huggingface.co/nvidia/Llama-3_1-Nemotron-Ultra-253B-v1) | Llama weight parent, but card expressly discloses Qwen use; report details Qwen and DeepSeek in post-training | A Llama parent alone does not clear the screen. |
| [NVIDIA-Nemotron-3.5-Lightning-30B-A3B-BF16](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-BF16) | Training-data tables identify Qwen-generated material and additional Chinese-model teachers | Keep excluded; newer does not imply independent ancestry. |

The 2025 Llama-Nemotron report identifies Qwen for mathematical data processing and generation, and DeepSeek-R1 for reasoning outputs. Those are training dependencies, unlike models mentioned only in comparison tables. This finding must not be projected backward onto the distinct 2024 70B release. [Llama-Nemotron report, section 3](https://arxiv.org/html/2505.00949v1).

## Historical no-Qwen research path

The following recommendation applies to the earlier ancestry-constrained study. The current Ultra program is documented in the architecture.

1. **Prioritize Minitron-4B-Base for a small research adaptation**, with Minitron-8B-Base as the next comparison. Obtain exact revision, tokenizer, license and upstream training evidence before admission. Treat both as conditional candidates rather than certified Qwen-free releases.
2. **Create SIP instruction data independently.** Use admitted contributor examples, accepted attribution and licensed retrieval sources. Do not import newer Nemotron post-training mixtures merely because they share NVIDIA branding. Record any generator, filter, embedding or reward model used.
3. **Create a checkpoint-specific training profile.** Retain the Python/Pydantic/Pydantic AI, Prefect, Rust/Axum and PostgreSQL architecture. Minitron's dense Nemotron-4 architecture needs its own verified loading, tuning and export path; the held Nano hybrid/MoE recipe and GPU estimates do not transfer automatically.
4. **Evaluate attribution and capability separately.** Test source citation, permission boundaries, tool use and refusal to invent contribution links. Keep accepted syndicate splits and creator rewards in deterministic application logic. Audit SIP-added data without claiming to have retroactively cleared the upstream corpus.

This research preserves alternatives to the selected Ultra program. It does not approve a production release, adopt a license, download weights or start training. The [USA index](USA_SOVEREIGN_AI_INDEX.md) and [architecture](SOLUTION_ARCHITECTURE.md) retain the unresolved ancestry and rights requirements.

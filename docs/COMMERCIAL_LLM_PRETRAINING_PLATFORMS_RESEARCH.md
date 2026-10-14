# Commercial offerings for training an LLM from scratch

**Sovereign Source procurement research — 13 October 2026**

**For Sovereign Source's first small independent model, evaluate Modal and AWS SageMaker AI training jobs. For an enterprise training program, make AWS the default bidder; for supplier-assisted model development, request a Cerebras pay-per-model proposal.** Together GPU Clusters provides a useful portable GPU price comparison. Baseten Training Jobs and Databricks AI Runtime add managed custom-code alternatives, with different availability and operational conditions.

Training from scratch means starting the model's learned weights from a new initialization and training them on an admitted corpus. Continued pretraining, supervised fine-tuning and reinforcement learning applied to an existing checkpoint preserve that checkpoint's ancestry. A product that offers only those operations does not meet this request.

The twelve US-provider offerings below span managed training platforms, managed clusters and contracted training services. They are procurement candidates, not a measured performance ranking. A US supplier does not automatically provide US-only processing, an approved model lineage or unrestricted commercial terms. Calling every offer turnkey SaaS would obscure the engineering work the customer retains.

## Choose the operating model first

| Need | First candidate | Why it belongs on the shortlist | Condition before purchase |
| --- | --- | --- | --- |
| Small research experiment with Python code | **Modal** | Explicit from-scratch language-model example and usage-based execution | Validate region pricing, checkpoint recovery and the 24-hour Function limit |
| Managed enterprise pretraining | **AWS SageMaker AI** | Documented pretraining jobs and a path to resilient HyperPod clusters | Price the full job configuration and verify capacity |
| Supplier engineers help deliver the model | **Cerebras Training Cloud** | Advertised pay-per-model design and training service | Contract specifically for new initialization and usable artifact delivery |
| Portable GPU cluster operated by the team | **Together GPU Clusters** | Customer training code plus public cluster prices | Select clusters, rather than the separate post-training API |
| Managed scripts with checkpoint-to-serving workflow | **Baseten Training Jobs** | Generally available container-based jobs and downloadable checkpoints | Prove the chosen pretraining implementation and US deployment arrangement |
| Training integrated with a Databricks estate | **Databricks AI Runtime** | Managed custom code and MLflow workflow | Accept or resolve current Public Preview limitations |

These are fit recommendations based on the documented capabilities cited in the profiles below. They do not establish which provider will have the lowest cost per successfully trained model.

## Comparison of twelve offerings

**Training platform** means managed execution of customer training code. **Managed cluster** means the supplier operates substantial infrastructure while the customer owns the training program. **Training service** can include supplier engineers delivering a contracted model. These distinctions matter more than a product's use of the word “training.”

| No. | Commercial offering | Route to training from scratch | Best fit for Sovereign Source | Main qualification |
| --- | --- | --- | --- | --- |
| 1 | **AWS SageMaker AI training jobs and HyperPod** | Training platform plus resilient clusters; custom containers and pretraining workflows | Enterprise training with a path from bounded jobs to sustained distributed runs | Quotas, regional capacity, storage and networking must be priced separately |
| 2 | **Google Cloud custom/serverless training** | Managed custom training; the Vertex AI documentation path now redirects to Gemini Enterprise Agent Platform | Teams wanting managed jobs and Google's GPU/TPU ecosystem | Select the custom-training service and supported accelerator path; Gemini model tuning is a different product |
| 3 | **Microsoft Azure Machine Learning** | Managed distributed jobs running customer PyTorch/DeepSpeed code | Organizations already operating in Azure | Customer supplies the pretraining implementation; Azure OpenAI access does not supply a new base model |
| 4 | **Databricks AI Runtime and Mosaic AI Custom Training** | Serverless custom jobs; Mosaic documentation also describes an explicit pretraining route | Training integrated with an existing Databricks workflow | AI Runtime is Public Preview; confirm current Mosaic commercial access and avoid assuming a legacy preview is generally available |
| 5 | **NVIDIA DGX Cloud Lepton with NeMo Megatron Bridge** | Cloud platform plus customer-controlled pretraining library | NVIDIA-oriented model engineering and checkpoint conversion | Provider/region selection and current recipe integration remain necessary; the old NeMo 2.0 example is deprecated |
| 6 | **Together GPU Clusters** | Managed Kubernetes/Slurm clusters running customer code | A flexible GPU alternative with public hourly prices | Its current “Custom Training” product is post-training; use the cluster route for a new initialization |
| 7 | **CoreWeave Cloud with SUNK** | Managed training clusters with Slurm on Kubernetes | Larger, sustained GPU programs with their own ML engineers | Quote capacity and operations scope; infrastructure management does not design the model or corpus |
| 8 | **Lambda 1-Click Clusters** | Reserved interconnected GPUs with managed orchestration | A bounded GPU reservation and portable training code | Current advertised cluster tiers start at 16 GPUs and a two-week term; smaller experiments need another offer |
| 9 | **Cerebras Training Cloud** | Specialized training cloud, with hourly or contracted model-delivery options | Teams willing to evaluate an alternative accelerator and supplier-assisted training | Confirm architecture support, US processing location, checkpoint export and the exact training agreement |
| 10 | **Crusoe Managed Slurm** | Managed cluster orchestration for customer training jobs | Teams that want a familiar Slurm workflow and managed infrastructure | Training code, corpus design and durable recovery remain customer responsibilities |
| 11 | **Modal** | Serverless customer Python/PyTorch code, with an explicit small language-model pretraining example | Small experiments and a possible path to distributed jobs | Durable checkpoints, Function time limits, regional pricing and GPU concurrency need explicit configuration |
| 12 | **Baseten Training Jobs** | Managed containers running customer training scripts across GPU nodes | Teams wanting less infrastructure work and integrated deployment | Fresh-model support is inferred from custom-code execution; validate it in a pilot; Loops is a separate post-training offer |

The linked evidence in the profiles identifies what each platform actually supplies. For generic custom-code platforms, the ability to run a newly initialized language model is a technical inference from their execution model, not proof that a particular LLM recipe has been tested there. Require a working pilot before a substantial commitment.

## Provider profiles and evidence

### Modal

Modal publishes an example that trains a small language model from a new initialization, demonstrating more than a fine-tuning-only workflow. It runs customer Python/PyTorch code and also documents multi-node training through clustered Functions. The small example establishes the execution route; its toy corpus and runtime are not a budget or quality forecast for Sovereign Source. [From-scratch example](https://modal.com/docs/examples/hp_sweep_gpt), [Multi-node training](https://modal.com/docs/guide/multi-node-training)

Function execution is limited to 24 hours per attempt. Multi-node failures and preemptions affect the whole cluster, so a long program needs durable training-state checkpoints and tested restart logic. Automatic retries alone do not restore optimizer or data-loader state. [Timeouts](https://modal.com/docs/guide/timeouts), [Cluster fault behavior](https://modal.com/docs/guide/multi-node-clusters)

For US operation, pin the relevant execution and routing regions and inspect storage and external integrations. Modal documents US durable storage and logs, but region selection carries a price multiplier; US execution must be included in the costed configuration. [Data residency](https://modal.com/docs/guide/data-residency)

The public base rates convert to about **$3.95/H100-hour** and **$6.25/B200-hour**, before CPU, memory and other applicable charges. The Starter plan advertises 10 concurrent GPUs; Team lists 50 and a $250 monthly plan fee plus usage. Capacity and multi-node requirements still need validation. Modal is a practical first pilot candidate, not an assurance of uninterrupted frontier-scale capacity. [Pricing and plan limits](https://modal.com/pricing)

### Baseten Training Jobs

Baseten distinguishes **Training Jobs, generally available**, from **Loops, in early access**. Jobs runs customer scripts in containers; Loops concentrates on reinforcement learning and supervised post-training. Select Jobs for an independently initialized model. The feasibility of a specific pretraining recipe is an inference from the custom-code interface and must be demonstrated. [Training products](https://www.baseten.co/products/training/)

The Jobs documentation describes multi-node execution, packaged training frameworks, checkpoint synchronization, download and resume. These are useful foundations for Sovereign Source's portability requirements. Preserve all required optimizer, scheduler, RNG and data-position state in the checkpoint; synchronizing files does not prove that a script saved sufficient state. [Training Jobs overview](https://docs.baseten.co/training/overview)

Baseten publishes a separate Training price table, including H100 at $0.10833 per minute, approximately **$6.50 per GPU-hour**. Obtain the actual region, GPU topology, storage and support configuration before comparing it with another service. Product-page statements about artifact ownership should be reflected in the applicable agreement. [Training rate card](https://www.baseten.co/pricing/)

### AWS SageMaker AI

AWS documents GPU pretraining jobs with customer containers, data inputs and output artifacts. HyperPod adds resilient clusters with Slurm or EKS orchestration, hardware replacement and supported job recovery. This combination makes it the leading default when the team wants managed training without giving up its own code. [Pretraining tutorial](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-hyperpod-gpu-sagemaker-training-jobs-pretrain-tutorial.html), [HyperPod architecture](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-hyperpod.html)

Use ordinary managed training jobs for the first bounded experiment; justify persistent HyperPod capacity with measured workload needs. Start with an admitted GPU implementation if portability is the priority. A Trainium route requires its own software and numerical validation. HyperPod pricing excludes connected services such as EKS, FSx and S3, so request a complete configuration estimate. [AWS pricing](https://aws.amazon.com/sagemaker/ai/pricing/)

### Google Cloud custom training

Google documents managed execution of a customer training application, distributed training, logging and enterprise controls including IAM, network boundaries and customer-managed keys. The former Vertex AI training URL currently redirects to **Gemini Enterprise Agent Platform** documentation. The reviewed service is custom/serverless training; it does not require initializing from Gemini weights. [Custom training overview](https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning/training/overview)

For a TPU-specific program, Google separately documents training workloads using MaxText and XPK on TPU7x. Do not assume every TPU topology available through GKE or Cloud TPU is also available through the managed-job configuration being purchased. [TPU7x training guide](https://docs.cloud.google.com/tpu/docs/tpu7x-training?hl=en)

This is a strong option for a team prepared to maintain its chosen GPU or TPU stack. Obtain a region-specific quote and benchmark the actual architecture; avoid comparing accelerator hourly prices without accounting for throughput and implementation work.

### Microsoft Azure Machine Learning

Azure Machine Learning supports distributed customer workloads using PyTorch, DeepSpeed and TensorFlow, including appropriate InfiniBand-enabled machines. That makes it a viable execution environment for a customer-written pretraining program. Its managed job launcher does not supply the dataset, objective or evaluation design. [Distributed GPU training guide](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-train-distributed-gpu?view=azureml-api-2)

Azure states that Machine Learning has no additional service charge on the reviewed pricing page, while compute and other consumed services are billed separately. Include storage, registry, logging and networking in the estimate. [Azure Machine Learning pricing](https://azure.microsoft.com/en-us/pricing/details/machine-learning/)

Prioritize this option when existing Azure identity, data and procurement arrangements reduce integration work. Keep custom training and any use of hosted OpenAI outputs as separate contractual and data-admission decisions.

### Databricks AI Runtime and Mosaic AI

Databricks AI Runtime offers serverless GPUs for custom models. Its CLI runs single-node and multi-node jobs with customer code, managed environments and MLflow tracking. **Both the service and CLI are currently marked Public Preview.** The notebook convenience interface should not be mistaken for the multi-node CLI route. [AI Runtime](https://docs.databricks.com/aws/en/machine-learning/ai-runtime/), [CLI execution model](https://docs.databricks.com/aws/en/machine-learning/ai-runtime/cli/)

Mosaic's separate documentation explicitly distinguishes Custom Training with a customer image/code, a DBRX Pretraining API marked preview, and fine-tuning. It provides more direct evidence of pretraining intent, but the published documentation alone does not confirm a new customer's access to every historical offer. [Mosaic AI Training](https://docs.mosaicml.com/projects/mcli/en/latest/)

This is one of the closest fits to managed training SaaS. Confirm the supported production path, region, preview conditions and checkpoint export before selecting it. Use an admitted custom architecture; the DBRX example does not require Sovereign Source to adopt DBRX weights or its tokenizer.

### NVIDIA DGX Cloud Lepton and NeMo

DGX Cloud Lepton supplies a common platform across compute providers and environments. Megatron Bridge supplies a separate PyTorch-native training library, including random-initialization pretraining and checkpoint conversion. NVIDIA documents a route that reads an architecture configuration without loading pretrained weights. [DGX Cloud Lepton](https://www.nvidia.com/en-us/data-center/dgx-cloud-lepton/), [Megatron Bridge](https://docs.nvidia.com/nemo/megatron-bridge/latest/index.html)

The old Lepton NeMo Framework pretraining quickstart is explicitly deprecated because it uses NeMo 2.0. Use a currently supported training stack and validate its Lepton job configuration instead of treating that legacy example as a maintained deployment recipe. [Deprecated example notice](https://docs.nvidia.com/dgx-cloud/lepton/examples/batch-job/nemo-fw-quickstart/index.html)

This route aligns with the project's NVIDIA engineering work, but buying the platform does not require using Nemotron pretrained weights. Quote the platform, underlying capacity and support together. A global marketplace requires an explicitly selected US processing arrangement for the proposed US launch.

### Together GPU Clusters

Together's clusters provide Kubernetes or Slurm access, shared storage, NVIDIA GPU options and high-speed networking for training configurations. They can execute a customer's own pretraining code. Reserved and on-demand capacity have different billing and termination behavior. [Cluster overview](https://docs.together.ai/docs/gpu-clusters-overview), [Cluster billing](https://docs.together.ai/docs/gpu-clusters-billing)

The current **Together Custom Training** page describes RL and supervised fine-tuning of existing models. It should not be used as evidence that its post-training SDK initializes a new base model. Select GPU Clusters or obtain a separately scoped pretraining statement of work. [Current Custom Training product](https://www.together.ai/custom-training)

Together is a useful comparison bidder for the first portable GPU experiment. The public cluster table lists H100 at $3.99/GPU-hour and B200 at $8.19/GPU-hour on demand. These rates concern compute, not a complete trained model. [Together pricing](https://www.together.ai/pricing)

### CoreWeave Cloud and SUNK

SUNK combines Slurm workflows with Kubernetes operations for large, long-running training jobs. CoreWeave describes topology-aware scheduling, infrastructure health monitoring and job-level observability. This is a training-cluster operating layer, rather than an automated corpus-to-model application. [SUNK product documentation](https://www.coreweave.com/products/sunk)

Prioritize it for sustained multi-node work once Sovereign Source has a stable training implementation and engineers responsible for model quality. Request a written capacity, storage, support and recovery quote. Require the pilot to demonstrate checkpoint export and resume outside the original cluster; portable code alone does not prove portable optimizer state or equivalent numerical behavior.

### Lambda 1-Click Clusters

Lambda advertises interconnected GPU clusters with managed Kubernetes or Slurm. Its current table lists a 16-GPU H100 tier at $6.16/GPU-hour and a 16-GPU B200 tier at $9.86/GPU-hour, with advertised terms beginning at two weeks. These are cluster-reservation rates, not the price of a completed training run. [Current cluster offering](https://lambda.ai/1-click-clusters)

The service is a good candidate when the team can operate its own training program and wants a defined reservation. Lambda's billing guide distinguishes cluster reservations from on-demand instances and separately billable filesystems. A small experiment should not inherit a two-week cluster commitment merely because the product name says “1-Click.” [Billing guide](https://docs.lambda.ai/public-cloud/billing/)

### Cerebras Training Cloud

Cerebras offers a specialized training cloud and describes both pay-per-hour and pay-per-model arrangements, including supplier assistance with model design and training. Its product page also markets customer control of models and data. Those statements should become explicit obligations in the training contract, including the treatment of checkpoints, logs, backups and staff access. [Cerebras Training Cloud](https://www.cerebras.ai/cloud)

Consider it when reducing distributed-GPU engineering is worth evaluating another execution stack. Require a demonstration of the exact architecture, optimizer, precision and data-loader behavior needed by the project. An existing PyTorch/OLMo pipeline is not automatically a drop-in Cerebras job. Obtain a training quote rather than using an inference token price, and verify a practical export path for independent serving.

### Crusoe Managed Slurm

Crusoe documents managed Slurm orchestration with a control plane, login nodes, shared storage and GPU worker node sets. Its service handles infrastructure components and hardware remediation; applications must still handle interruptions and restore useful training state. [Managed Slurm overview](https://docs.cloud.crusoe.ai/orchestration/slurm/overview/index.html), [Cluster quickstart](https://docs.cloud.crusoe.ai/quickstart/spin-up-gpu-cluster/index.html)

Use this as another portable Slurm option when the team's preferred training framework fits the offered hardware. Quote the actual node set, networking, shared storage and service scope. Crusoe's serverless fine-tuning quickstart is a separate LoRA product and does not establish a serverless pretraining service. [Product quickstarts](https://docs.cloud.crusoe.ai/quickstart/overview/index.html)

## Training products that do not establish a from-scratch route

The precise product matters even when its supplier also sells general training infrastructure.

| Product | Documented operation | Implication for this purchase |
| --- | --- | --- |
| **Thinking Machines Tinker hosted API** | LoRA fine-tuning, SFT, RL, preference optimization and distillation on supported models | Its documented API does not establish customer-controlled fresh foundation initialization. Keep it in the post-training category. [Documentation](https://tinker-docs.thinkingmachines.ai/) |
| **Together Custom Training** | RL and supervised fine-tuning of existing models | Use Together GPU Clusters or a separately agreed pretraining service. [Product](https://www.together.ai/custom-training) |
| **Baseten Loops** | SDK for RL and SFT, currently early access | Evaluate Baseten Training Jobs for custom pretraining code. [Product distinction](https://www.baseten.co/products/training/) |

A full-weight update can still be fine-tuning: the decisive question is where the starting weights came from. A model catalog entry called “base” normally identifies a released base checkpoint, not proof of fresh initialization. Ask the supplier to demonstrate the launch configuration rather than infer capability from “custom model” marketing.

## Ten parameters for the purchasing decision

Apply the same requirements to every bidder. A supplier's general “AI training” claim is insufficient for acceptance.

| Parameter | Evidence Sovereign Source should require |
| --- | --- |
| 1. New initialization | Inspect configuration and launch logs showing no inherited model weights; identify every model, tokenizer and learned preprocessing dependency |
| 2. Custom training control | Run the chosen code/container, architecture, optimizer, precision, tokenizer and data loader without an undocumented substitution |
| 3. Distributed performance | Measure useful tokens/second, scaling efficiency and data-loader throughput on the exact GPU or other accelerator topology |
| 4. Recovery | Resume model, optimizer, scheduler, RNG and data position after an injected worker failure; measure lost work and cost |
| 5. US deployment and privacy | Contracted processing region, subprocessors, support access, encryption, network controls and permitted retention |
| 6. Artifact portability | Export weights, optimizer state, tokenizer, configuration, logs and manifests; perform a restore and inference smoke test elsewhere |
| 7. Commercial control | Explicit rights to train and commercialize the intended model, including a competing model, and clear supplier rights to customer material |
| 8. Price and commitment | Itemized compute, idle reservation, storage, network, control-plane, support, failed-run and cancellation costs |
| 9. Operational responsibility | Named owner for data integrity, numerical failures, cluster health, incident response and agreed service limits |
| 10. Attribution and rewards integration | Application hooks for source manifests and consumption events; export to SIP's agreement and beneficiary ledger |

Parameters 1, 5, 6 and 7 are admission gates. A low hourly price cannot compensate for a disallowed data transfer, incompatible contract or inaccessible model artifact. For the remaining parameters, compare measured outcomes rather than inventing a numerical vendor score from marketing pages.

## Pricing and budget interpretation

The public rates below were reviewed on **13 October 2026**. They illustrate resource charges; they do not price a completed LLM or establish a performance ranking.

### A short experiment

For **8 GPUs allocated for 24 hours**, equivalent to 192 GPU-hours:

| Offer | Published billing unit | Converted USD per GPU-hour | Resource-charge illustration |
| --- | ---: | ---: | ---: |
| Modal H100 SXM5 | $0.001097/second | $3.9492 | $758.25 |
| Modal B200 | $0.001736/second | $6.2496 | $1,199.92 |
| Baseten Training H100 | $0.10833/minute | $6.4998 | $1,247.96 |

Sources: [Modal pricing](https://modal.com/pricing), [Baseten Training pricing](https://www.baseten.co/pricing/). Totals use the published units before rounding. Modal separately charges CPU and memory; storage, network, region multipliers, paid plans, support and taxes may add cost. Credits and negotiated discounts are excluded. Confirm the available node configuration and concurrency limit; this arithmetic is not a capacity quote. On Modal, longer programs must span checkpointed executions within its Function timeout.

### A sustained cluster allocation

The following assumes **16 GPUs continuously allocated for 14 days, or 336 hours**:

| Offer and billing basis | Listed USD per GPU-hour | Compute-only illustration |
| --- | ---: | ---: |
| Together H100 on demand | $3.99 | $21,450.24 |
| Together B200 on demand | $8.19 | $44,029.44 |
| Lambda H100 16-GPU cluster tier | $6.16 | $33,116.16 |
| Lambda B200 16-GPU cluster tier | $9.86 | $53,007.36 |

Sources: [Together's cluster prices](https://www.together.ai/pricing) and [Lambda's cluster prices](https://lambda.ai/1-click-clusters). The products have different commitments and service arrangements. These figures exclude other charges and are not matched performance benchmarks, capacity reservations or supplier quotes. A higher-priced accelerator may complete a job sooner; verify that result on the intended workload.

For the other routes, obtain a workload-specific total: AWS publishes resource pricing with additional connected-service costs; Google describes consumption-based managed compute; Azure bills underlying resources; Databricks requires the selected runtime's commercial rate; NVIDIA depends on the chosen platform/provider arrangement; CoreWeave and Crusoe need the actual cluster specification; Cerebras offers hourly or model-delivery pricing that requires workload scoping. An inference price per million tokens cannot price a pretraining run.

### Estimate the whole program

Estimate the run with measured throughput:

```text
productive_hours = target_training_tokens / measured_cluster_tokens_per_second / 3600
billed_hours = productive_hours + startup + checkpointing + idle_allocation + replay
compute_cost = accelerator_count * billed_hours * contracted_hourly_rate
program_cost = compute_cost + storage + networking + platform/support fees
             + data acquisition/curation + engineering + evaluations + failed experiments
```

Use a wall-clock throughput measurement that includes the overhead being modeled, or add that overhead separately, but not both. Reserved capacity can bill for time after useful training finishes. Distinguish unique source material from repeated epochs and unsuccessful attempts when recording data consumption and rewards.

The first purchase should validate the pipeline, not promise frontier capability. Follow the [open-source research stack's proposed 100–350 million parameter pilot](OPEN_SOURCE_RESEARCH_LLM_STACK.md), with expansion toward 1 billion parameters only after learning curves, recovery and economics justify it. The engineer must choose the token budget and hardware after a memory and throughput test. The example allocations above do not imply a particular model size, completion time or commercially useful capability.

## Buying model delivery rather than compute

If Sovereign Source needs external engineers to build the model, use Cerebras' pay-per-model offer as a first request for proposal, not as a fixed-price promise. Its advertised service includes design and training assistance; the statement of work must establish whether the bid covers fresh pretraining, adaptation of an existing model, or both. [Service scope](https://www.cerebras.ai/cloud)

Specify the following deliverables for any contracted development service:

1. **Starting state and inputs:** reviewed architecture, newly initialized weights, tokenizer provenance, approved corpus and separately authorized synthetic data. Require approval before substituting pretrained components.
2. **Work and responsibilities:** data preparation, training implementation, numerical debugging, infrastructure, evaluation and source-consumption instrumentation, each assigned to a named party.
3. **Acceptance milestones:** a recoverable small pilot, measured quality on held-out tasks, a spending ceiling and an explicit decision before scale-up. Define how failed runs, delays and scope changes affect payment.
4. **Independent delivery:** weights, tokenizer, configuration, runnable training code, intermediate checkpoints, optimizer state, logs, source manifests and evaluation artifacts, with a tested restore and serving path.
5. **Commercial terms:** intended commercialization and competition rights, confidentiality, permitted supplier reuse, sublicensing where needed, data deletion and access after termination. Identify separately licensed dependencies and source obligations.

Neither a compute invoice nor a promise that the customer owns the weights supplies the rights, reproducibility or content-rewards system by itself.

## Fit with Sovereign Source rights and content rewards

These platforms provide execution services. None of the reviewed offerings establishes SIP's complete combination of member mandates, contribution and influence review, accepted earning agreements, source-use accounting and beneficiary settlement. Sovereign Source should keep those functions in its own application rather than infer them from a provider's model registry or training dashboard.

Reuse the architecture in the [SaaS business plan](SAAS_MARKETS_AND_SYNDICATES_BUSINESS_PLAN.md), [production system plan](PRODUCTION_SYSTEM_PLAN.md) and [open-source research stack](OPEN_SOURCE_RESEARCH_LLM_STACK.md):

1. **Authorize and prepare sources.** Rust/Axum and PostgreSQL hold accepted grants and syndicate mandates. Python/Pydantic validates a manifest. Prefect runs approved preparation jobs, including selected Dolma toolkit steps.
2. **Release an immutable training input.** Retain asset versions, rights references, notices, tokenizer provenance, filtering decisions and the mapping from packed training records to original sources. Only the admitted data crosses into the supplier environment.
3. **Execute a controlled training job.** Pin code and dependencies, record a fresh initialization and checkpoint ancestry, and submit a bounded job to the selected platform. The cluster scheduler handles individual workers; Prefect supervises the external job lifecycle.
4. **Record learning and consumption evidence.** Capture source sampling and consumption with run/attempt/checkpoint identifiers, including replay and filtering. Separate eligibility in a dataset from actual participation in an accepted training run.
5. **Export and release the model.** Preserve weights, tokenizer, configuration, evaluation results, notices and the applicable source/earning cohort. Demonstrate independent inference and recovery before deleting the original deployment.
6. **Calculate contracted rewards.** The SIP ledger applies accepted formulas and beneficiary splits. Platform GPU invoices are costs, not creator-reward formulas; the existing 20% pool applies only where adopted and is not silently reduced by compute expense.

Training-consumption records can support an agreed corpus allocation. They do not establish the exact causal contribution of every source to every generated answer. Record conceptual influences as reviewed claims with supporting evidence and accepted agreements. The [marketplace terms](../licenses/SYNDICATE-MARKETPLACE-TERMS-0.1.md) govern that proposed mechanism separately from the training service.

### Model lineage and commercial restrictions

The shortlist retains the project's US-provider focus. Provider nationality does not establish model ancestry, US-only processing or cleared data rights. A cloud that also offers Qwen or DeepSeek can host a separately controlled training job without loading those weights; the job's complete dependency and data chain is what must pass the project's admission policy.

The existing Nemotron 3 Ultra checkpoint has a recorded conflict with the no-Qwen requirement. Moving it to another supplier, further training it or renaming the result does not remove that conflict. The separate [model-selection recommendation](MODEL_SELECTION_RESEARCH_SUMMARY.md) favors evaluating a new foundation through OLMo-core with newly initialized weights and admitted sources. Validate this implementation on the chosen service; a custom-code interface alone is not an integration test.

A fresh weight initialization also does not resolve provenance for a reused tokenizer, learned filter, teacher-generated data or evaluation contamination. Establish their status explicitly. Training on a customer's own permitted data does not require buying a frontier lab's generated training examples.

Keep infrastructure permission and hosted-model output permission distinct. A provider's support for customer training does not establish unrestricted use of every model API it resells. Before signing, obtain the applicable training/compute agreement and written treatment of commercialization, competition, export, deletion, provider reuse, subcontractors and any supplied datasets. Product-page ownership language should become enforceable contract terms, not an assumed legal clearance.

## Recommended pilot and shortlist reduction

For the first small experiment, compare **Modal and an AWS SageMaker AI training job** using the same admitted OLMo-core program. Include **Baseten Training Jobs** when its managed job and deployment workflow reduces engineering effort. These are alternative execution environments; avoid building three integrations before selecting one pilot.

For sustained GPU training, request comparable proposals from **AWS and Together GPU Clusters**. Add **NVIDIA DGX Cloud Lepton with an identified US compute provider** when NVIDIA support is central. Evaluate **Databricks AI Runtime** where an existing Databricks workflow offsets its current preview constraints. If the team needs model-development engineers as part of the purchase, seek a separately scoped **Cerebras pay-per-model** proposal.

Use the same admitted corpus, newly initialized architecture, tokenizer and precision for comparisons where technically possible. A Cerebras or TPU proposal may need a separate framework port; document numerical and implementation differences instead of treating its speed as an identical benchmark.

| Pilot step | Deliverable | Acceptance condition |
| --- | --- | --- |
| Scope the order | Exact model, token budget, US region, data transfer, compute ceiling and responsible engineers | Contract permits the intended training and independent commercial release |
| Validate initialization | Small synthetic-data run and artifact inventory | No unauthorized pretrained checkpoint or undisclosed learned dependency |
| Exercise admitted data | Short run with source-to-token manifest and held-out validation | All samples resolve to admitted sources; loss and diagnostics are technically credible |
| Test recovery | Deliberate worker interruption and checkpoint resume | Restore training state and account for replay without unexplained data loss or duplicate ledger events |
| Test portability | Downloaded checkpoint and independent inference/restore | Model artifacts are usable outside the supplier's original job environment |
| Compare total cost | Actual invoice, productive throughput, engineering hours and projected full-run cost | Price the same useful training outcome and include operational effort |
| Scale or stop | Reviewed next-stage proposal | Increase spend only after quality, rights, recovery and economics pass |

**Recommended first commitment:** one bounded, recoverable experiment on Modal or AWS with fresh weights, an admitted tokenizer and corpus, source-consumption records and independently usable checkpoints. Select a larger platform or development contract only after the pilot establishes the actual quality, operational effort and cost of the Sovereign Source training program.

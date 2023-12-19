# Flyte community meeting

[![HacmKD documents](https://hackmd.io/badge.svg)](https://hackmd.io/@davidmirror/r1PDrxkEh?edit)

## Logistics
* **Goal:** Share success/failure stories with other Flyte community members, get updates on what's new in the project and learn how other organizations/projects are using/integrating Flyte
* **When:** Every other Tuesday at 9:00AM Pacific Time ([convert to your timezone](https://dateful.com/time-zone-converter?t=9am&tz2=Seattle-Washington))
    * [Add to your calendar](https://www.addevent.com/event/EA7823958)
* **Where:** [Zoom bridge](https://us06web.zoom.us/j/93875115830?pwd=RWo2MklCTElmRzJZWk0xelBENDVuUT09)
* **How:**
    * Agenda template
        * Host: 
        * Attendees [name, affiliation]
        * Welcome new members
        * News from the ecosystem
        * Community/project updates
        * Roadmap updates (once per month)
        * Guest presentation (show & tell)
        * Open mic/questions [add your name]

### Schedule of guest presentations

This meeting is open for the entire ML/Data community to share their knowledge. If you want to present, add your name and topic to the list and we'll reach out to coordinate logistics:

| Date | Presenter  | Topic  |   
|---|---|---|
| 06/27/2023  | Dr. Fabio Graetz  |Flyte at Recogni   |
| 06/27/2023 | Niels Bantilan | Fine tuning LLMS with declarative ML infra|
|07/11/2023   | Jay Chia  |[Intro to dAFT](https://github.com/Eventual-Inc/Daft)   |
|07/25/2023   | Keming Yang  | Develop and run your ML applications inside the container using [envd](https://github.com/tensorchord/envd)  |
|08/08/2023|Elena Samuylova- Emeli Dral| Intro to the [Evidently project](https://github.com/evidentlyai/evidently)|
|08/22/2023| David Aronchick     | Integration with Flyte & Bacalhau (the distribute compute platform) --TO BE RESCHEDULED |    |
|09/05/2023| Eli Bixby     | Flyte journey at Cradle  |    |
|09/19/2023| Community monthly roundtable    |   |    |
|10/03/2023| Jing Xie and HuiC (Memverge)   | Intro to MMCloud and Flyte integration demo |    |
|10/17/2023| David Aronchick and the team from Bacalhau Computing    |  Intro to Flyte and Bacalhau integration|    |
|10/31/2023| Jose Navarro    |Flyte journey at Cleo  |    |
|11/14/2023| Han Ru    | Flyte ChatGPT Agent |    |
|11/28/2023| Community roundtable    |  |    |
|12/05/2023|Neeraj Malhotra / Niels Bantilan    | Pandera-PySpark integration |    |

:::info
:information_source: **Reminders** 
:::
* All meetings are recorded and posted to Flyte's [YouTube channel](https://www.youtube.com/@flyteorg)
* You agree to abide by The Linux Foundation's [Code of Conduct](https://lfprojects.org/policies/code-of-conduct/) 
* Agenda is open for everyone wanting to ask questions or propose discussion topics
:::info
:information_source: **How to stay involved**
:::
* [Join Slack](https://flyte-org.slack.com)
* [Github Discussions](https://github.com/flyteorg/flyte/discussions)
     
-----

## November 28, 2023
* Agenda
  * Host: Samhita Alla
  * Attendees [name, affiliation]
      * Kyle Briggs (iTMethods Inc.)
      * Dan Butler (Salk Institute)
      * Chris Grass (MCG Health)
  * Welcome new members
  * News from the ecosystem
    * Duet AI: https://cloud.google.com/blog/products/ai-machine-learning/how-duet-ai-speeds-up-development-and-operations
    * Llama on AWS Inferentia2: https://huggingface.co/blog/inferentia-llama2
    * AI Proxy: https://www.braintrustdata.com/blog/ai-proxy
  * Community/project updates
    * Flyte school episode coming: https://flyte.org/events/flyte-school-learn-your-codebase-fine-tuning-codellama-with-flyte-to-learn-flyte
    * Dosu bot is being rolled out in the Flyte repository
        * [Example 1](https://github.com/flyteorg/flyte/issues/4488)
        * [Example 2](https://github.com/flyteorg/flyte/issues/4491#issuecomment-1829805632)
    * New reference implementation for GCP ([PR](https://github.com/unionai-oss/deploy-flyte/pull/7#pullrequestreview-1743810920))
    * Vote to rename `Contributor` role: https://github.com/flyteorg/community/issues/20
  * **Community roundtable**
      * Action items:
          * Update FTHW guide to include permissions on workers (David)
          * 
 * Open mic/questions [add your name]
     
## November 14, 2023
* Agenda

  * Host: David Espejo
  * Attendees [name, affiliation]
      * Nikki Everett (Union.ai)
      * Troy Chiu (UCSD)
      * Niels Bantilan (Union.ai)
  * Welcome new members
      * Devin Stein (OSS Manintainer/ Dosu founder https://dosu.dev/)
      * Paul (IT Methods)
  * News from the ecosystem
    * Efficient LLM inference on CPUs: https://arxiv.org/abs/2311.00502v1
    * MemGPT: build chatbots with self-editing memory, extending the LLM context -> perpetual conversations: https://github.com/cpacker/MemGPT 
    * cuDF: https://github.com/rapidsai/cudf
    * OpenAI Dev Day: https://openai.com/blog/new-models-and-developer-products-announced-at-devday
        * GPT-4 Turbo with 128k context (+April 2023 knowledge cutoff)
        * Assistants API
        * GPT-4 Turbo with Vision
        * DALL E 3 API
        * Also, [GPTs](https://openai.com/blog/introducing-gpts)
    * AWS announces EC2 Capacity Blocks (a.k.a. reserve your GPU): https://aws.amazon.com/blogs/aws/announcing-amazon-ec2-capacity-blocks-for-ml-to-reserve-gpu-capacity-for-your-machine-learning-workloads/
    * Levels of AGI: a framework https://arxiv.org/abs/2311.02462
    * HPC Foundation: https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-high-performance-software-foundation-hpsf
  * Community/project updates
    * [Hacktoberfest wrap-up](https://flyte.org/blog/hacktoberfest-2023-wrap-up)
    * Flyte school episode coming: https://union.ai/events/flyte-school-learn-your-codebase-fine-tuning-codellama-with-flyte-to-learn-flyte
  * Guest presentation (show & tell)
    * **Building the FlyteChatGPT Summary Bot: lessons learned** by Eric Chen
    
 * Open mic/questions [add your name]
     * [Dosu](https://dosu.dev/): demo  (Devin Stein)

## October 31, 2023
* Host: Samhita Alla
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Joe Eschen (Union.ai)
    * Eric Chen (Flyte Contributor) (Future-Outlier)
* Welcome new members
    * 
* News from the ecosystem
    * Pandera 0.17 is out: https://www.union.ai/blog-post/pandera-0-17-adds-support-for-pydantic-v2
    * Text embeddings inference: https://github.com/huggingface/text-embeddings-inference
    * Voyager: https://voyager.minedojo.org/
* Community/project updates
    * New Slack guidelines: https://docs.flyte.org/en/latest/community/index.html#slack-guidelines
    * **Flyte 1.10 is out**: https://flyte.org/blog/flyte-1-10-monorepo-new-agents-pyflyte-ergonomic-improvements-and-more
    * Hacktoberfest: Final call to have your PRs merged!
* Guest presentation (show & tell)
    * **Flyte journey at Cleo** by Jose Navarro
* Open mic/questions [add your name]

## October 17, 2023

* Host: David Espejo
* Attendees [name, affiliation]
    * Ketan Umare [Union AI]
    * Joe Eschen [Union AI]
    * Katrina Rogan [Union AI]
    * Kyle Briggs [iTMethods Inc.]
* Welcome new members 
    * Troy Chiu (MsC student, UC San Diego)
* News from the ecosystem
    * State of AI report: https://www.stateof.ai/
    * A visual exploration illustrating the why and how of LLMs: https://ig.ft.com/generative-ai/
    * Take on stateless Terraform: https://www.bejarano.io/terraform-stateless-critique/
    *  Protect AI Open Sources Three Tools to Help Organizations Secure AI/ML Environments from Threats: https://www.businesswire.com/news/home/20231005973991/en/Protect-AI-Open-Sources-Three-Tools-to-Help-Organizations-Secure-AIML-Environments-from-Threats
* Community/project updates
    * "Spotify's Next-Gen Workflow Platform with Flyte" talk at Crunch Conf: https://www.linkedin.com/posts/sonja-ericsson_just-had-an-incredible-time-speaking-at-activity-7116157198937784320-GdFO
    * An introductory guide to LLMs: https://flyte.org/blog/getting-started-with-large-language-models-key-things-to-know
    * Flyte school session on Flyte plugins: https://union.ai/events/flyte-school-enrich-your-ai-pipelines-a-deep-dive-into-flyte-plugins
    * **Hacktoberfest** 
        * Performance so far:
            * ![](https://hackmd.io/_uploads/rk3Mdlhbp.png)
            *  61% increase in code contributions
            *  36% increase in productivity
            *  42 open Issues / 14 unassigned / 33 with [no linked PRs](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+label%3Ahacktoberfest+-linked%3Apr+sort%3Acomments-desc+)
            *  2 blog posts in review
            *  ![](https://hackmd.io/_uploads/HyQucmh-6.png)
            *  Updates to guidelines:
                *  First-come, first-served
                *  Link your PR to the Issue using [GH keywords](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword)


* Guest presentation (show & tell)
    * **Power Your Flyte Machine Learning Workflows with Bacalhau Computing** by David Aronchick
        * Links shown:
            * 
* Open mic/questions [add your name]
     
-----

## October 3, 2023

* Host: 
    * David Espejo
* Attendees [name, affiliation]
    * 
* Welcome new members
    * 
* News from the ecosystem
    * Python 3.12 is out: https://www.python.org/downloads/release/python-3120/
    * Llama2 on SageMaker: perf benchmark https://huggingface.co/blog/llama-sagemaker-benchmark
    * Preventing hallucination in LMMs: https://arxiv.org/abs/2309.14525
    * Open source coding assistant: https://tabby.tabbyml.com/
    * Mistral AI https://mistral.ai/news/announcing-mistral-7b/
* Community/project updates
* 
    * Hacktoberfest: https://flyte.org/blog/flyte-at-hacktoberfest-2023
    * 1.10 beta release: https://github.com/flyteorg/flytekit/releases/tag/v1.10.0b0
        * Upcoming release will be the 1st using the monorepo = simplified contribution experience
* Guest presentation (show & tell)
    * **Running pipelines on spot computing with Flyte and MMCloud** by Jing and Hui from Memverge
* Open mic/questions [add your name]

## September 19, 2023
* Host: Samhita Alla
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Han-Ru Chen
    * Peeter Piegaze (Union.ai)
* News from the ecosystem
    * Falcon 180B: https://huggingface.co/blog/falcon-180b
    * Stable Audio: https://www.stableaudio.com/
    * Mojo: https://www.modular.com/blog/mojo-its-finally-here
* Community/project updates
    * **Flyte School ep # 5**: https://flyte.org/events/flyte-school-flyte-deployment-a-live-walkthrough
    * **Docs restructuring**: https://docs.flyte.org/projects/cookbook/en/latest/userguide.html
    * Hacktoberfest is coming!
    * Upcoming biotech panel: https://www.union.ai/events/unlocking-value-from-sequencing-data-with-workflow-management
    * MLOps World 2023 (Austin, Oct 24-26)
        * Workshop: https://flyte.org/events/flyte-at-mlops-world-2023
        * You want to attend? Reach out, we have some complimentary tickets
* Guest presentation (show & tell)
    * **Flyte community roundtable**
* Open mic/questions [add your name]

## September 5, 2023
  * Host: David Espejo
  * Attendees [name, affiliation]
      * David Espejo (Union.ai)
      * 
  * Welcome new members
      * 
  * News from the ecosystem
      * CodeLlama: https://ai.meta.com/blog/code-llama-large-language-model-coding/
      * OSS Docker registry for AI models: https://depot.dev/blog/depot-ai
      * Consciousness in AI: https://arxiv.org/abs/2308.08708
      * Graph of Thoughts: https://arxiv.org/abs/2308.09687
      * Cuber: simplify app deployment to K8s https://github.com/cuber-cloud/cuber-gem#cuber
  * Community/project updates
      * Deployment resources:
          * [Local K8s](https://github.com/davidmirror-ops/flyte-the-hard-way/blob/main/docs/on-premises/001-configure-local-k8s.md)
          * [Updates to plugin setup guides](https://docs.flyte.org/en/latest/deployment/plugins/index.html)
          * [**Terraform modules**](https://github.com/unionai-oss/deploy-flyte)
      * Flyte School keeps going: https://flyte.org/events/flyte-school-flyte-architecture-deep-dive
      * "Flyte: 1 year in" by Edgar Trujillo from Bazaarvoice: https://blog.developer.bazaarvoice.com/author/edgar-trujillo/
  * Guest presentation (show & tell)
      * **Flyte journey at Cradle (Eli Bixby)**
          * Notes: Eli discussed the mission of their company, which is to make programming biology easy by using machine learning to improve proteins and enzymes. They also mentioned their unique usage of Flyte in their production loop, where they trained and updated models based on new data from customers.
Eli and John discussed the positive aspects of the Flyte workflow system, including its provision of reproducibility, provenance, and caching. They also mentioned using weights and biases for storing artifacts and expressed a desire for more tagging and filtering options for provenance.

The team discussed the challenges of composing workflows and encouraging good code practices. They implemented a multi-package Python monorepo approach to handle dependencies and ensure separate Python environments for development.

The discussion revolved around addressing issues related to dependencies, versioning, and workflow composition in a development environment. They explored solutions such as separate Python environments, tagging versions, and making workflow execution serializable to improve the overall workflow management process.

Eli and Ketan discussed various improvements and challenges in using Flyte. Eli mentioned the need for more granular permissions, better execution fetching, data deletion, improved mapping and streaming capabilities, and support for higher-order functions to avoid a combinatorial explosion of registered workflows.
Ketan and Eli discussed the possibility of solving a problem using task templates, but they also acknowledged that the requirement of interfaces could complicate the solution. They ran out of time to share more details but expressed interest in exploring the topic further in the future.
  * Open mic/questions [add your name]
      *  

## August 22, 2023
* Host: Samhita Alla
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Fabio Grätz (Recogni.com)
* Welcome new members
* News from the ecosystem
    * AI Town: https://www.convex.dev/ai-town
    * Candle: https://github.com/huggingface/candle
    * humanscript: https://github.com/lukechilds/humanscript
    * K8sGPT: https://k8sgpt.ai/
* Community/project updates
    * **Flyte School**: https://flyte.org/events/flyte-school-kubernetes-for-ml-and-data-an-introduction
    * **Flyte 1.9 release**: https://flyte.org/blog/flyte-1-9-arraynode-execution-tags-new-navigation-and-more
* Guest presentation (show & tell)
    * **An Open Conversation with Istiyak H. Siddiquee and Gopal K. Vashishtha About Flyte**
* Open mic/questions [add your name]

## August 8, 2023
* Host: David Espejo
* Attendees [name, affiliation]
    * Tim Sheiner, Union
    * Eduardo Apolinario, Union
    * Dan Rammer, Union
* Welcome new members
* News from the ecosystem
    * Tensorchord announced pgvecto. rs: https://modelz.ai/blog/pgvecto-rs
    * An overview of current supply/demand of GPUs: https://gpus.llm-utils.org/nvidia-h100-gpus-supply-and-demand/#tracing-the-journey-of-gpu-supply-and-demand
    * Patterns for LLMs-based products and services: https://eugeneyan.com/writing/llm-patterns/
    * Gorilla: LLM connected to 1,600+ APIs" https://github.com/ShishirPatil/gorilla
    * Audocraft: a library for audio processing and generation with DL: https://github.com/facebookresearch/audiocraft
    * LK-99: more like an anti-superconductor https://arxiv.org/abs/2308.03110
* Community/project updates
    * Upcoming Flyte school session (EU/APAC timezone): https://www.eventbrite.com/e/flyte-school-a-practical-introduction-to-machine-learning-orchestration-tickets-691091502287
    * 
* Roadmap updates (once per month)
    * Release updates (Eduardo)
* Guest presentation (show & tell)
    * **Continuous testing and monitoring for production ML pipelines** by Emeli Dral and Elena Samuylova from Evidently.ai
        * Link to the example: https://github.com/evidentlyai/community-examples/blob/main/events/202308_demo_bikes_for_flyte.ipynb
        * Blog post: https://www.evidentlyai.com/blog/ml-monitoring-data-drift-how-to-handle
* Open mic/questions [add your name]



## July 25, 2023

* Host: Samhita Alla
* Attendees [name, affiliation]:
* Welcome new members
* News from the ecosystem
  * Llama 2: https://ai.meta.com/llama/
  * PyTorch Transformers RL Library: https://github.com/lvwerra/trl
  * Flash Attention 2: https://princeton-nlp.github.io/flash-atttention-2/
* Community/project updates
   - [Governance model](https://github.com/flyteorg/community/blob/main/GOVERNANCE.md#community-roles-and-path-to-maintainership) updated:
     * New role: Flyte Collaborator
     * Updated privileges and expected responsibilites for each role
    * Yicheng Lu accepted as new contributor
    * Request for Comments: [Run flytekit code from a Jupyter notebook](https://github.com/flyteorg/flyte/discussions/3878)
    * Flyte 1.8 released
    * Flyte School
* Guest presentation (show & tell)
    * **Develop and run your ML applications inside the container using envd - Keming Yang**
    * **Flyte Agents - Kevin Su**
* Open mic/questions [add your name]

## July 11, 2023

* Host: David Espejo
* Attendees [name, affiliation]
    * Samhita Alla [Union.ai]
* Welcome new members
* News from the ecosystem
    * https://www.run.house/blog/a-pytorch-approach-to-ml-infrastructure?s=09 [David]
    * https://inflection.ai/nvidia-coreweave-mlperf [David]
    * FastAPI 0.100 [released](https://github.com/tiangolo/fastapi/releases/tag/0.100.0): includes support for Pydantic V2
    * GPT-4 API GA: https://openai.com/blog/gpt-4-api-general-availability [David]
* Community/project updates
    * Flyte callback for LangChain merged! https://python.langchain.com/docs/ecosystem/integrations/flyte
    * Flyte at SciPy 2023:
        * Hands-on workshop: https://cfp.scipy.org/2023/talk/YHEYVY/
        * Open source sprints (Sat and Sun): https://cfp.scipy.org/2023/talk/NMNJYF/
* Roadmap/release updates
    * Eduardo Apolinario, OSS Engineering Manager, Union.ai
        *  Eduardo provided updates on Flyte 1.8, highlighting stabilization, bug fixes, improved support for optionals and GCP secrets, and upcoming features like eager mode, breaking flytekit into smaller packages, better dev experience for agents, and improvements in handling data plugins.
* Guest presentation (show & tell)
    * Authz on Flyte (lighting talk) - **David Espejo**
        * PR to update auth docs: https://github.com/flyteorg/flyte/pull/3837
    * Daft: the distributed Python dataframe for complex data - **Jay Chia, Eventual.inc co-founder and daft maintainer**
        * Performance benchmarks: https://blog.getdaft.io/p/introducing-daft-a-high-performance
        * Notes: Jay presented about the Python distributed data frame library called daft, which aimed to handle complex data types like images and tensors. He discussed the challenges of working with multimodal data and the need to combine ML algorithms, Python code, and SQL relational operations for effective data engineering. Jay discussed the challenges of maintaining separate systems for handling different types of data and the benefits of using a solution like DAFT, which allows for efficient processing of both relational and complex data types. He also mentioned the advantages of using Flyte in conjunction with DAFT for scalable and reproducible data processing workflows. Jay discussed the capabilities of Daft, a data frame library, including filtering data, working with complex data like images, and running Python functions. He also mentioned the use of Flyte, a workflow engine, to create reproducible pipelines and orchestrate data processing tasks. Jay discussed the integration of Flyte tasks using Ray and mentioned the possibility of passing data frames between steps for more efficient processing. Jeev and David expressed interest in understanding the implementation of lazy serialization and passing of unmaterialized frames between tasks
* Open mic/questions [add your name]

## June 27, 2023
* Host: Samhita Alla
* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * Maarten de Jong [blackshark.ai]
    * Samhita Alla [Union.ai]
    * Martin Stein [Union.ai]
* Welcome new members
    * Joe Saarem
* News from the ecosystem
    * vLLM: https://vllm.ai/
    * Andromeda Cluster: https://andromedacluster.com/
    * Gorilla: https://github.com/ShishirPatil/gorilla
    * GPT Engineer: https://github.com/AntonOsika/gpt-engineer
    * The new LLM stack: https://www.sequoiacap.com/article/llm-stack-perspective/ (David)
    * MosaicML got acquired: https://www.databricks.com/company/newsroom/press-releases/databricks-signs-definitive-agreement-acquire-mosaicml-leading-generative-ai-platform (David)
* Community/project updates
    * Flyte 1.7 release: https://flyte.org/blog/flyte-1-7-flyte-agents-revamped-kubeflow-plugins-and-more
* Guest presentation (show & tell)
    * Niels Bantilan: **Fine-tuning LLMs with declarative ML orchestration**
        * https://github.com/unionai-oss/llm-fine-tuning
    * Dr. Fabio Graetz: **Flyte at Recogni**
* Open mic/questions [add your name]

## June 13, 2023
* Host: David Espejo
* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * Prafulla Mahindrakar [Union.ai]
    * Eduardo Apolinario [Union.ai]
    * Martin Stein [Union.ai]
* Welcome new members 
    * Markus Breener
    * Peeter Piegaze (Union.ai)
    * Broder Peters
    * Jannis Grondberg
* News from the ecosystem [add news including your name]
    * OWASP Top 10 vulnerabilities for LLMs (draft): https://owasp.org/www-project-top-10-for-large-language-model-applications/descriptions/
        * Related: https://owasp.org/www-project-machine-learning-security-top-10/
        * MITRE's mitigation list: https://atlas.mitre.org/mitigations/
    * MLFlow 2.4: https://www.databricks.com/blog/announcing-mlflow-24-llmops-tools-robust-model-evaluation
    * MusicGen: https://ai.honu.io/papers/musicgen/
    * Google's Secure AI Framework: https://blog.google/technology/safety-security/introducing-googles-secure-ai-framework/
    * 
* Community/project updates
    * [TMLS](https://www.torontomachinelearning.com/)
    * SIG-auth: yay or nay
        * Related: https://github.com/flyteorg/flyte/issues/3671
* Roadmap updates (once per month)
    * New release
        * 1.7 going out today
        * Flyteagents to be expanded. Improving plugin authoring experience
        * Execution tags (v1 for 1.8)
        * Eager-mode
        * Expose dataclass usage on flytekit (v1.8)
* Guest presentation (show & tell)
    * Prafulla Mahindrakar: **"Monitoring Flyte workloads"**
        * Slide deck: https://docs.google.com/presentation/d/1DUNHfKm9draSQ8cjx_GYBANmtZI3gThkX5mB9hgihAE/edit?usp=sharing
    * Jan Fiedler: **"Flyte@Kineo.ai - from PoC to MVP in no time!"**
* Open mic/questions [add your name]
    * *Insert your question*
* Next session:
    * June 27th, Dr. Fabio Graetz from Recogni!


## May 30, 2023

* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * 
* Welcome new members
    * Mike Morgan (Fidelity Investments)
* Community/project updates
    * [Community groups](https://github.com/flyteorg/community/blob/main/GOVERNANCE.md#community-groups)
    * [Office Hours now with themed slots](https://docs.flyte.org/en/latest/community/index.html#office-hours)
    * Flyte in the HuggingFace docs! --> https://huggingface.co/docs/transformers/main/en/main_classes/callback
* Presentations/demos (show & tell)
    * Contributors of the month [https://flyte-org.slack.com/archives/CNMKCU6FR/p1685101013243129]
    * Yubo Wang
    * Yicheng Lu
    * Byron Hsu
* Open mic/questions [add your name]

## May 16, 2023
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
* Welcome new members
    * Brian O'Donovan
    * Jan Fiedler
    * Vaibhav Verma
* Community updates
    * Agenda now lives on hackmd, er, here. It's open for you to add questions or discussion topics
    * Show off something you've shared using the #show-and-tell Slack channel or the Show and Tell GH discussions category
    * Upvote issues to help prioritize for release planning
* Roadmap updates (once per month)
    * 1.6 is out! Try it and let us know!
* Guest presentation (show & tell)
    * ImageSpec demo!
        * Uses envd
        * Paralellizes image building
* Open mic/questions [add your name]

## May 2nd, 2023

* Community updates
    * Contributors of the month (Tim Leonard, Franco Bocci and Alex Papanicolau)
    * PyData Seattle last week was a blast! See the [recap blog](https://www.union.ai/blog-post/pydata-seattle-2023-in-review)

* Roadmap updates
    * A sneak peek into what's coming for 1.6 release
    * Let us know what's top of mind for you. Upvote feature requests by adding a "thumbs up" reaction to [Issues](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+is%3Aissue+label%3Aenhancement+sort%3Areactions-%2B1-desc)
    *  Go through the ideas in the [RFC Incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator) and comment!

* Guest presentation by Mick Jermsurawong, ML Infra engineer @ Stripe
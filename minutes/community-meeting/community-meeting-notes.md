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
|07/11/2023   | *Add your name*  |   |
|07/25/2023   | *Add your name*  |   |
|08/08/2023|*Add your name*|
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
## June 27, 2023
* Host: Samhita Alla
* Attendees [name, affiliation]
* Welcome new members
* News from the ecosystem
    * vLLM: https://vllm.ai/
    * Andromeda Cluster: https://andromedacluster.com/
    * Gorilla: https://github.com/ShishirPatil/gorilla
    * GPT Engineer: https://github.com/AntonOsika/gpt-engineer
    * The new LLM stack: https://www.sequoiacap.com/article/llm-stack-perspective/
    * MosaicML got acquired: https://www.databricks.com/company/newsroom/press-releases/databricks-signs-definitive-agreement-acquire-mosaicml-leading-generative-ai-platform
* Community/project updates
    * Flyte 1.7 release: https://flyte.org/blog/flyte-1-7-flyte-agents-revamped-kubeflow-plugins-and-more
* Guest presentation (show & tell)
    * Niels Bantilan: **Fine-tuning LLMs with declarative ML orchestration**
    * Dr. Fabio Graetz: **Flyte at Recogni**
* Open mic/questions [add your name]

## June 13, 2023
* Host: David Espejo
* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * Prafulla Mahindrakar [Union.ai]
    * Eduardo Apolinario [Union.ai]
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
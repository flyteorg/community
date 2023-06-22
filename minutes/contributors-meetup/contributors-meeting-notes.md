# Flyte Contributors meetup

[![HacmKD documents](https://hackmd.io/badge.svg)](https://hackmd.io/gmwGOpD_TWiyw9_dJ_34Dg?edit)

## Logistics
* **Goal:** Discuss RFCs, features, integrations and major changes with Maintainers and Technical Steering Committee members
* **When:** Every other Thursday at 11:00AM Pacific Time ([convert to your timezone](https://dateful.com/time-zone-converter?t=11am&tz2=Seattle-Washington))
    * [Add to your calendar](https://www.addevent.com/event/xn16931566)
* **Where:** [Zoom bridge](https://us06web.zoom.us/j/81897346046?pwd=cGxaRWxSTUdkTlpHSXB1RUJ1Njd3UT09)
* **How:**
    * Agenda template
        * Attendees [name, affiliation]
        * Welcome new members
        * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
        * Working Groups updates
        * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
        * Opportunities to contribute
            * [Good first issues](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)
            * [Help wanted](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22+)
        * Open mic/questions [add your name]

:::info
:information_source: **Reminders** 
:::
* All meetings are recorded and posted to Flyte's [YouTube channel]((https://youtube.com/playlist?list=PLmQd1BBY9MWozXmf4NGS8zQK17E5aV8oE))
* The Linux Foundation's [Code of Conduct](https://lfprojects.org/policies/code-of-conduct/) applies to every communication chanel the community uses
* Agenda is open for everyone wanting to ask questions or propose discussion topics
:::info
:information_source: **How to stay involved**
:::
* [#contribute](https://flyte-org.slack.com/archives/C04NJPLRWUX) Slack channel
* [Github Discussions](https://github.com/flyteorg/flyte/discussions)
     
-----
## June 22, 2023
* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * Recogni.com [Recogni.com]
    * Bernhard Stadlbauer [Pachama.com]
    * Niels Bantilan [Union.ai]
    * Tim Sheiner [Union.ai]
    * Arthur Book [RecoverX]
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
    * Config overrides
        * Working group meeting to sync on progress with Byron
        * We will need to update the protobuf messages in flyteidl to be `oneof`. Otherwise we cannot distinguish between defaults and user-set overrides
        * Fabio needs to review Bernhard's PR into his but hasn't happened yet
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * [Unify retry behaviour](https://github.com/flyteorg/flyte/discussions/3793)
* Open mic/questions [add your name]
    * Yee - Tiny URLs, Artifact service, multi-variate maps
        * Artifact IDL: https://github.com/flyteorg/flyteidl/pull/408
        * Artifact Flytekit: https://github.com/flyteorg/flytekit/pull/1655/files
        * Artifact Admin https://github.com/flyteorg/flyteadmin/pull/572/files
        * Older flyte URL PRs ([first](https://github.com/flyteorg/flyteadmin/pull/546), [second](https://github.com/flyteorg/flyteadmin/pull/565))
        * Now closed/rejected multi-variate [map PR](https://github.com/flyteorg/flytekit/pull/1700)
        * General dataclass PR that should be streamlined with Pydantic effort: https://github.com/flyteorg/flytekit/pull/1679/
    * Feedback on support for generalized container types [PR](https://github.com/flyteorg/flytekit/pull/1700) - Yee
    * SKIP: Status of `help wanted` and `good first issue` work [David]
    * [Type support for Pydantic](https://github.com/flyteorg/flytekit/pull/1660)
        * Arthur and Fabio are working on this
        * Will need review from someone from Union after the next iteration
    * Niels - talk about GPU machine selection (RFC TBD)
        * https://github.com/flyteorg/flyte/discussions/3796

## June 8, 2023
* Attendees [name, affiliation]
    * Fabio Grätz (Recogni.com)
    * Yubo Wang (linkedin.com)
    * Bernhard Stadlbauer [Pachama.com]
    * David Espejo [Union.ai]
    * Dan Rammer [Union.ai]
    * Eduardo Apolinario [Union.ai]
* Welcome new members
    * Edvard Majakari [Rakettitiede.com]
    * Arthur Book [ML Eng at RecoverX]
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * [Console UI Upgrade Slides](https://docs.google.com/presentation/d/1Lm5WO1PwmsaR7MnPwCmkeKQ-1DxvfGGCf5kfrB46Zwo/edit?usp=sharing)
* Working Groups updates
    * Started implementation work for "runtime override" RFC https://github.com/flyteorg/flyte/pull/3553
        * https://github.com/flyteorg/flyteidl/pull/412 (Add overrides to protos, Byron)
        * https://github.com/flyteorg/flytekit/pull/1672 (Send override name from flytekit to flyteadmin, Fabio)
        * https://github.com/flyteorg/flytekit/pull/1676 (Add runtime override to workflow and launchplan specs, Bernhard, Fabio will review)
        * Fabio will work on changes in flyteadmin
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Opportunities to contribute
    * [Good first issues](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)
    * [Help wanted](https://github.com/flyteorg/flyte/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22+)
* Open mic/questions [add your name]
    * Discussion in Slack about which options should be exposed in Kubeflow plugins
        
        * Expose everything that is possible (e.g. resources of master and worker replicas in `task_config=PyTorch` ) or opinionated approach?
            * Allow controlling restarts via `task_config` or refer user to use Flyte's retry mechanism?
    * Adding log links on a per-task level ([see discussion](https://github.com/flyteorg/flyte/issues/3696#issuecomment-1572217346))
        * Option 1:
            ```python
            @task(
                log_links="{"wandb": f"https://...com/?tag={{.executionId}}"
            )
            ```
        * Option 2:
            ```python
            deck.append(...)
            deck.flush
            ```
        * I think most users would love option 2 but I understand the hesistance to create such a communication channel. Option 1 would solve my personal problem (Fabio).
    * How will we handle `task_config` overrides at runtime



## May 25, 2023
* Attendees [name, affiliation]
    * David Espejo [Union.ai]
    * Bernhard Stadlbauer [Pachama.com]
    * Dan Rammer [Union.ai]
    * Hongxin (honnix) [Spotify.com]
    * Fabio Grätz (Recogni.com)
    * Byron (linkedin.com)
    * Eduardo Apolinario [Union.ai]
* Welcome new members
    * Hongxin (Spotify)
    * Jay Ganbat (Freenome)
* Review [outstanding RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * Eager Mode
        * What happens to "child executions" when an `@eager` task is aborted?
    * Execution tags
        * [PR](https://github.com/flyteorg/flyte/pull/3727) amending the original RFC with changes discussed last time. Do you agree?
        * What happens to pod labels when somebody adds a tag in the UI mid execution?
        * Address [Comment](https://github.com/flyteorg/flyte/pull/3320#discussion_r1203591315)
    * Config overrides RFC
        * The results of the latest discussions need to be incorporated into the document. After that merge? (TODO: byron)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]
    * `flytekit` regressions in `1.6.1` [Bernhard]
        * https://github.com/flyteorg/flytekit/pull/1657 [Fabio]
    * Splitting up work for config override [Bernhard]
    * Community groups implementation [David]
    * Implementation of privileges for roles in repos (see https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization) [David]
    * [Discussion](https://github.com/flyteorg/flyte/issues/3696) about adding additional log links from a `@task` [Fabio]
    * [Pydantic Plugin](https://github.com/flyteorg/flytekit/pull/1620): Arbitrary types break `model.schema()`. How can we avoid code duplication with dataclass type transformer?

## May 11, 2023
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Byron (linkedin.com)
    * Dan Rammer (Union.ai)
    * Niels Bantilan (Union.ai)
    * Yee (Union.ai)
    * Kevin (Union.ai)
    * Fabio (Recogni.com)
    * Bernhard (Pachama.com)
* Welcome new members
* Review [outstanding RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * Config overrides RFC:
        * Naming: `with_runtime_overrides` vs `with_overrides_hook`
    * Execution tags RFC:
        * discuss [approach 1](https://github.com/flyteorg/flyte/blob/bc087ed2eb260f02658741d1c54696fbf7bbe14a/rfc/system/0001-flyte-execution-tags.md#approach-1-treat-all-labels-the-same-way-and-allow-searchfilter-and-click-based-grouping) vs [2](https://github.com/flyteorg/flyte/blob/bc087ed2eb260f02658741d1c54696fbf7bbe14a/rfc/system/0001-flyte-execution-tags.md#approach-2-certain-label-keys-are-treated-special) (since there are discussions about the exact UX of option 2)
    * Eager Mode RFC:
        * discuss RFC draft https://github.com/flyteorg/flyte/discussions/3396
        * PR: https://github.com/flyteorg/flytekit/pull/1579
* (Monthly) Release planning
    *  Niels/Eduardo to create an Issue with the features planned for 1.7.0 for the community to comment and pick where to collaborate
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * [Rework Slack notification](https://github.com/flyteorg/flyte/discussions/3647)
    * [Idea about improvements of logging links configuration](https://github.com/flyteorg/flyte/discussions/3666)
* Open mic/questions [add your name]


## April 27, 2023
* Attendees [name, affiliation]
    * David Espejo, Union.ai
    * Fabio Grätz, Recogni.com
    * Bernhard Stadlbauer, Pachama.com
    * Dan Rammer, Union.ai
    * Byron Hsu, linkedin.com
    * Eduardo Apolinario, Union.ai
* Welcome new members
* Review [outstanding RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * Let's discuss [this](https://github.com/flyteorg/flyte/pull/3553#issuecomment-1510807853) comment (config override RFC)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Contributions
    * [Adapt authentication flow for Azure AD & Azure AD setup doc](https://github.com/flyteorg/flyte/issues/3620)
* Open mic/questions [add your name]
    * Updates to [GOVERNANCE](https://github.com/flyteorg/community/pull/5) [David]

## April 13, 2023
* Attendees
    * David Espejo (Union.ai)
    * Dan Rammer (Union.ai)
    * Fabio Grätz (Recogni.com)
    * Eduardo Apolinario (Union.ai)
    * Yee Tong (Union.ai)
    * Tim Sheiner (Union.ai)
* Welcome new members
    * Shivay Lamba
    * Yubo Wang (Linkedin)
* Review [outstanding RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions
    * User identity (byron)
    * Database queries (eduardo)
        * CTA to tun some queries in `flyteadmin` and `datacatalog`
        * @Eduardo to share list of queries
    * Refactor kf-operator plugins (yubo)
        * How Flyte handles backward-incompatible changes
        * [KU] Typically, use ask template version
        * [DR] Currently offering configuration for different ReplicaSets. Flyte plugin versions are not tied to propeller versions so you could use an older plugin version
        * [KU] There could be a `parsing` error message in the UI
    * Global config (yubo)
        * Trying to set config at workflow level, accesible from tasks at execution time.
        * [KU] Not supported right now. Would workflow-level env variables be enough?
        * [DR] PR recently added for execution time env variables
        * [KU] You can use raw output prefix which is available in the context and handles I/O automatically
        * [YW] What about retention config?
        * 

    * HW accelerators presentation (Shivay)
    * Discovered a small bug with pod templates, would need a pointer where the best place is to fix it (Fabio) 
        * [#3590](https://github.com/flyteorg/flyte/issues/3590)
    * Torchrun status (Fabio)
        * Getting closer, further testing planned. PR open in flytepropeller


## March 30, 2023
* Attendees
    * David Espejo (Union.ai)
    * Fabio Grätz (Recogni.com)
    * Bernhard Stadlbauer (Pachama.com)
    * Greg Gydush (Freenome)
    * Niels Bantilan (Union.ai)
    * Dan Rammer (Union.ai)
    * Byron Hsu (LinkedIn)
* Welcome new members
    * Tim Sheiner (Union.ai)
    * Greg Gydush (Freenome)
* Review [outstanding RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * (Notes on each PR)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions
    * *Add your question here*
    * 
    * Branches vs forks
    * CODEOWNERS file
    * Issue/bug report template changes

## March 16, 2023
* Attendees
    * David Espejo (Union.ai)
    * Bernhard Stadlbauer (Pachama)
    * Fabio Grätz (Recogni.com)
    * Byron Hsu (LinkedIn)
    * Dan Rammer (Union.ai)
    * Eduardo Apolinario (Union.ai)
    * David Muraco
    * Niels Bantilan (Union.ai)
* Welcome new members
    * 
* Review outstanding RFCs
    * Introduce the CODEOWNERS file to assing ownership on reviews
    * Performance benchmarking RFC: https://github.com/flyteorg/flyte/pull/2995
    * Flyte system tags (https://github.com/flyteorg/flyte/pull/3320)
        * Nice for experimentation
        * Fabio and Bernhard using workarounds at the moment
    * Array Node for Map Task (https://github.com/flyteorg/flyte/pull/3446)
        * [NB] Should'nt it be named Map...
        * [DR] Happy to change naming
        * [DR] Multiple inputs is a frequent ask and it should be included here
        * [SB] Just switched to DynamicTasks
    
* Open mic/questions
    * [RFC process](https://github.com/flyteorg/flyte/pull/3460)
    * [Flyte Config Overrides RFC](https://docs.google.com/document/d/1NS93TghOzwKamihQMDATd_jdYJtrtWQ1sViSTSDduAA/edit#heading=h.rcvd21a5zyol)
        * [DR] Using nodeIds could introduce complexity, you might be overrriding the wrong task
        * [BH] Linkedin uses an internal workaround
        * [DR] More generalized key-value pairs are good. 
        * [BS] referenceTask is a black box, the proposal would introduce some reference between teams
        * [BH] We don't need to override the reference
        * [Yee] How to handle it from the user perspective on runtime (prompt)
        * [FG] Recent experience trying to override the cache, probably a PR coming. It would be great to be able to override things defined in the decorator at runtime, not sure about adding it to the UI
        * [SB] Using PodTask and using overrides for GPU selection at runtime
        * [Yee] Resources are already overridable
        * [SB] Not enough for our use case as we need to specify GPU type. Workflow parameters and task config in the proposal could be problematic

* [Special Interest Groups](https://en.wikipedia.org/wiki/Special_interest_group)/[Working Groups](https://en.wikipedia.org/wiki/Working_group)
* PR spotlight: https://github.com/flyteorg/flyte/pull/3256
    * [EA] Probably a stretch on maintaining the images for this but up for the community

* [BS] Switching to Mono Repo?
    * [EA] It shouldn't affect OSS users

* [FG] We should create GH teams to reflect the governance structure

    * 

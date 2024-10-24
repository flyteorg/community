# Flyte Contributors meetup - meeting notes archive

## October 10, 2024
* Attendees [name, affiliation]
  * Yee Tong, Union
  * Jason Parraga
  * Paul Dittamo, Union
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Discuss [active RFCs]((https://github.com/orgs/flyteorg/projects/12/views/1))
  * Open mic/questions [add your name]
      * Jason Parraga - Execution Concurrency Threshold Support



## Sep 26, 2024

* Attendees [name, affiliation]
    * Fabio Grätz
    * David Espejo
    * Eduardo Apolinario
    * John Votta
    * Niels Bantilan
    * Jason Parraga
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Discuss [active RFCs]((https://github.com/orgs/flyteorg/projects/12/views/1))
  * Tuple/NamedTuple: https://github.com/flyteorg/flytekit/pull/2732
  * Deterministic error propagation for distributed tasks https://github.com/flyteorg/flyte/pull/5598 
* Open mic/questions [add your name]

## Minutes

### Key Takeaways

- Large object handling improvements coming soon, addressing community pain points
- Binary IDL implementation progressing, solving multiple issues (JSON-like objects, data classes, unions)
- New error aggregation strategy proposed for distributed tasks, improving root cause identification

### Topics

#### Large Object Handling
Upcoming feature to offload large objects to Blob store, circumventing gRPC limitations.
Configurable thresholds for when objects get offloaded (min/max sizes).
No new flags or opt-in mechanism; seamless integration with existing SDK.
#### Binary IDL (Implementation in Progress)
Addresses multiple issues: JSON-like object encoding, data classes, Pydantic models, union types
Reuses existing literal types, reducing deployment risks
Improves developer experience across various contexts (e.g., dictionaries with integer values)
Beta release expected in November, including UI visualization updates.

#### Error Aggregation for Distributed Tasks
New RFC proposes timestamp-based error aggregation for distributed training jobs
Aims to solve race conditions in error reporting for multi-pod setups
Key changes:
Unique error file names (UUID-based) to avoid overwrites
Error documents to include timestamps and worker names
New error file reader in Propeller to aggregate multiple error files
Plugin properties to specify error aggregation strategy
Backwards compatibility considerations included

#### Community Plugins
Updated process: plugin authors responsible for maintenance, Flyte maintainers for approvals/merging
Triage permissions for non-binding approvals to be explored

#### Next Steps
- Eduardo to review the error aggregation RFC in detail
- David to tag Paul for a sanity check on the multi-error output reader proposal
- Fabio to potentially work on implementation if RFC is accepted
- Consider organizing a talk/panel on distributed training with Flyte
- Update community plugin RFC with non-binding approval process for plugin maintainers

## August 29, 2024

 * Attendees [name, affiliation]
   * David Espejo (Union.ai)
   * Fabio Grätz
   * Kevin Su
   * Chun-Mao Lai
   * Eduardo Apolinario (Union.ai)
  * Welcome new members
    * Chun-Mao (Michael) Lai (Incoming UC San Diego student/OSS contributor)
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Discuss existing RFCs
      * Community plugins RFC
          * https://github.com/flyteorg/flyte/pull/5610/files#r1736689384
          * https://github.com/flyteorg/flyte/pull/5610/files#r1736694079
      * Execution Concurrency
          * https://github.com/flyteorg/flyte/pull/5659/files#r1722376237
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Open mic/questions [add your name]
    * [Rafael] Keeping versions in sync (flyteidl/1.13.2 etc...)
    * [Fabio] https://github.com/flyteorg/flyte/issues/5684

**Minutes**


Introducing new RFC for tuple support @ 4:49
Michael presented a new RFC to add support for named tuples and tuple types in Flyte. The key goals are to allow users to specify the name of a tuple and the names of its fields, and to add new types to support these new tuple constructs. The group discussed various implementation details and tradeoffs, such as how to handle the case where a tuple is returned as part of a larger output structure.

Exploring options for tuple support @ 9:00
The group explored different approaches for implementing tuple support, including:

Treating tuples as a first-class type with special handling
Treating tuples the same as lists, with no special support
Creating a new "univariate tuple" type distinct from regular tuples The group agreed that a prototype implementation would be helpful to better understand the tradeoffs and implications of the different approaches.
Discussing impact on existing Flight features @ 27:39
The group discussed how adding tuple support could impact existing Flight features, such as the ability to reference fields in named tuples returned by tasks. There were concerns about maintaining backwards compatibility, and the group agreed that the prototype should aim to preserve existing behaviors where possible.

Recap and next steps @ 39:59
The group summarized the key open questions and agreed that Michael should work on a prototype implementation to further explore the different approaches. The group will continue the discussion asynchronously and revisit the topic in a future meeting.

## August 15, 2024

* Attendees [name, affiliation]
  * David Espejo(Union.ai)
  * Fabio Grätz
  * Eduardo Apolinario (Union.ai)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]

**Minutes**

Changing meeting time to regular schedule @ 0:00

David proposed moving the meeting back to the regular time of every other Thursday at 11am Pacific, as the alternating schedule has had limited success and excludes many US-based contributors. The group agreed to this change.

New RFC: Serialized execution of launch plans @ 1:36

Eduardo introduced a new RFC to allow serialized execution of launch plans, which has been a long-requested feature. The goal is to provide a mechanism to control concurrency at the workflow level, such as for scheduled runs. The group discussed some potential edge cases and implications, and agreed to review the RFC in more detail.

New RFC: Offloading large literals to blob storage @ 11:09

Eduardo also presented a new RFC to address the issue of hitting GRPC limits with large fan-out jobs, by offloading large literals to blob storage. This is initially being scoped for map tasks, but the plan is to extend it to other workflow types. The group was generally supportive of this proposal.

Incubator project: Task execution optimization @ 14:03

David noted a recent entry in the incubator project list around task execution optimization, and encouraged the group to review and provide feedback on the discussion thread if they have strong opinions.

Meeting wrap-up @ 15:01

The group concluded the meeting, with a reminder to continue discussing the RFC proposals on the relevant channels.


## August 1, 2024
* Attendees [name, affiliation]
  * David Espejo (Union.ai)
  * Fabio Grätz
  * Rafael Raposo
* Welcome new members
  * Bugra Cedik, StackAV
  * Andy Czerwonka, Principal Engineer at Citrine Informatics
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * [Deterministic error propagation](https://github.com/flyteorg/flyte/pull/5598)
  * [JSON IDL](https://github.com/flyteorg/flyte/pull/5607)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions
  * Andy Czerwonka (Attempting to adopt Flyte on the JVM, with future Python use cases). I realize we'll likely not get to all of this, but we're at a tipping point in our adoption. Should we schedule a JVM-focused discussion?
    * Citrine Use Cases
      * Task/Workflows written by engineers, published using CI/CD
      * Tasks/Workflows triggered from API servers
      * Client requesting workflow status
    * Deployment architecture
      * Current offering is single tenant
      * Flyte cluster will be multi-tenant, offloading jobs to a regional cluster
      * Need S3 storage isolation for each tenant (Flyte project)
    * Understanding the Gap between jflyte and pyflyte
      * I don't really understand where the gaps is, I learn as I go, creates a tonne of adoption risk
      * Features of jflyte vs "the platform"
    * Getting to a Baseline where we can contribute
	  * Ownership (who are the contributors)
	  * Baseline
		- Protos have not been updated in 2 years
		- Flyte publishes 20-ish libraries, yet the docs suggest we're good with one or two
		- Registration is the only exposed Flyte Admin capability, not sure why
		- Roadmap
		- Github Issues
    * Progress (Technical Details)
	  * Data Binding challenges using Struct / Binary
		- JSON support seems obvious? How are people managing without?
		- Can we use custom protos?
	  * Copying all jars on every task execution
	  * How does the map/reduce workflow work in `flytekit-java`
	  * Integration with DataDog
	  * New `Job` attribute, can someone give insight into the use case it's intended to solve?

**Minutes**


- RFC discussion

Error handling for distributed tasks @ 2:03
Fabio presented a proposal to address the issue of race conditions when multiple worker pods try to write error files during a distributed training task. The goal is to make error handling more deterministic by allowing each worker pod to write its own error file, so the first error can be identified as the likely root cause. The team discussed potential implementation approaches and open questions around how the plugin should communicate the need for multiple error file outputs.

Handling of task outputs @ 5:16
The group explored how task outputs are currently handled, noting that some plugins have race conditions for outputs similar to the error file issue. The team discussed whether the plugin should be responsible for handling output communication to avoid issues like having to return a list of outputs instead of a single value.

Backwards compatibility for new error handling @ 13:05
Eduardo raised the question of the backwards compatibility story for the proposed error handling changes. The team discussed a plan to leverage metadata and type transformations to maintain compatibility with existing tasks, while allowing the new error handling functionality.

Community contributed plugins @ 16:47
David brought up the topic of how community contributed plugins are currently handled, noting that they automatically become maintenance tasks for the core team. The group agreed this is not ideal, and discussed the need for a process to better manage community contributions, potentially by marking them as "community" plugins.

- Open mic  

Java SDK usage and gaps @ 19:36
Andy from Citrine Informatics shared his experience and challenges in trying to adopt the Java SDK for Flyte, including issues with data types, deployment, and the overall state of the Java ecosystem compared to the Python SDK. The group discussed potential ways to better support the Java use case, including documentation, roadmapping, and enabling more community contributions.


## June 6th, 2024
 * Attendees [name, affiliation]
     * Eduardo Apolinario (Union.ai)
     * David Espejo (Union.ai)
     * Yee (union.ai)
 * Welcome new members
   * Jason Parraga
 * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
 * Working Groups updates
 * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
 * Community pulse
   * Open and noteworthy 
     * [Support non-any Python types](https://github.com/flyteorg/flyte/pull/5408)
     * [Adding identity to Python agents](https://github.com/flyteorg/flytekit/pull/2315)
     * [Fixes the OAuth callback URL for subpaths](https://github.com/flyteorg/flyte/pull/5192)
     * [Fix console bradcrumbs for subpahts](https://github.com/flyteorg/flyteconsole/pull/861)
   * Recently merged 
 * Open mic/questions [add your name]
   * Release process and [RC](https://github.com/flyteorg/flyte/releases/tag/v1.12.1-rc0)
   * [New candidate for TSC](https://github.com/flyteorg/community/issues/25)
   * [Add ImageBuilderSpec.should_build method](https://github.com/flyteorg/flytekit/pull/2458)
   * [pyflyte run --copy flag](https://github.com/flyteorg/flyte/issues/5343)


## July 18, 2024 (It shoudld have been) cancelled
## July 4, 2024 CANCELLED DUE TO US HOLIDAY
## June 20th, 2024
 * Attendees [name, affiliation]
   * David (Union.ai)
   * Niels (Union.ai)
   * Eduardo (Union.ai)
   * Rob Ulbrich (Mercedes Benz)
   * Rafael Raposo (Spotify)
   * Fabio Graetz (Recogni)
   * Daniel Sola (Union.ai)
   * Haytham (Union.ai)
 * Welcome new members
 * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
   * Project Isolation RFC
     * There can be a compile-time solution for the flyteadmin middleware issue
     * It would be a check in case there's a new endpoint. If not set, flyteadmin won't compile. 
     * Rob Ulbrich to upstream this change, then we can move the RFC back to the Final Comment Period
 * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
 * Community pulse
   * PRs pending for review:
     * [Execution cluster label support](https://github.com/flyteorg/flytekit/pull/2422) (Fabio will review one more time by end of day)
     * [keep envFrom from podTemplate](https://github.com/flyteorg/flyte/pull/5423)
       * Eduardo to review
     * [Improve flyte-core Helm chart](https://github.com/flyteorg/flyte/pull/5362)
       * Yee or David to give final review
     * [Support positional arguments](https://github.com/flyteorg/flytekit/pull/2522)
   * Open, most commented Issues
     * [task_config override is broken](https://github.com/flyteorg/flyte/issues/4543)
       * Still broken and not easy to fix.
       * Eduardo and Fabio to sync
     * [Support for declaring tasks in classes](https://github.com/flyteorg/flyte/issues/3492)
       * Needs a champion and further validation to see if the idea is valid
     * [Method to query large workflows](https://github.com/flyteorg/flyte/issues/4056)
       * Fabio: agree with the need
     * [Union types fail for e.g. two different dataclasses](https://github.com/flyteorg/flyte/issues/5489) (Not commented a lot yet but maybe worth discussing)
       * Supporting inheritance in dataclasses is a common use case
       * We could use the metadata field to pass information, including Python under bases
       * We could encode inheritance in the metadata field but type checking wouldn't be simple anymore
       * More discussion needed
 * Open mic/questions [add your name]
   * Changes in the TSC (David)
     * Bernhard stepping down: https://github.com/flyteorg/community/pull/26
     * Welcome Rafael Raposo!
   * Numpy 2 is painful 😭 (Niels)
     * Significant impact when a foundational library gets a major release
     * CI checks fixed
   * Revisit `--copy` flag, i.e. fast registration UX: https://github.com/flyteorg/flyte/issues/5343 (Niels)
     * The intent is to include source files
     * A recent contribution introduced the .flyteignore file that works similar to Git's
     * A better ModuleNotFound error would be great too
     * Fabio: I think making it easy to inject other packages is a great feature. I feel another flag is not a catastrophe, trying to detect it automatically seems like it might be brittle.
     * Rafael: another flag should be fine


## May 23, 2024
* Attendees [name, affiliation]
  * David Espejo (Union.ai)
  * Robert Ulbrich (Mercedes-Benz)
  * Han-Ru Chen (Future-Outlier)
  * Eduardo Apolinario (Union.ai)
  * Fabio Grätz
  * Rafael Raposo (Spotify)
* Welcome new members
  * None this week
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]
  * `cluster-pool` added, no backend implementation ([reference](https://github.com/flyteorg/flyte/pull/4956#issuecomment-2114843886))
    * Notes:
      * Fabio: maybe just a code comment would go a long way to avoid confusions. Rafael agrees.
      * Eduardo: one additional tactic would use reserverd fields on flyteidl. For other parts of the code, leaning into comments would be a good approach.
      * Rafael: adding reserved fields in the protos would save time
  * Feature request: [Vertical Pod scaling](https://github.com/flyteorg/flyte/issues/2234)
    * Notes:
      * Swarup (Software engineer at Stripe)
      * Next step: create an RFC Incubator post. David to promote it in the community to find other community members who want to commment on it.
  * Task node overrides still partially broken (`task_config`), see [issue](https://github.com/flyteorg/flyte/issues/4543#issuecomment-2127217720). Do we remove the `task_config` override ([beta](https://github.com/flyteorg/flytekit/blob/91cfb973eecca2ef35f0f5959f9754a1f51af451/flytekit/core/node.py#L187)) or is there a way to fix it? To fix it, we'd have to be able to access the task template in `with_overrides` as the backend is not aware of the task_config itself.
    * Notes:
      * Eduardo to explore how to expose the task_config, which would require re routing
      * Fabio: if we could override the template would be better than sending the task_config to the backend.
      * Eduardo: further discussion is needed, to fix it for all fields.

 -----


## May 9, 2024
  * Attendees [name, affiliation]
    * David Espejo (Union)
    * Niels Bantilan (Union)
    * Eduardo Apolinario (Union)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
    * [Project isolation RFC updates](https://github.com/flyteorg/flyte/pull/5204)
      * Notes:
        * Robert reviewed the current implementation of the project isolation feature, which uses an interceptor to check the user's access permissions based on claims in the token. The team discussed potential weaknesses in the current approach, such as the need to manually maintain a list of all endpoints, and explored alternative solutions like using the user ID instead of claims. 
Eduardo suggested extending the project isolation feature to support other dimensions like environment, in order to create a more comprehensive role-based access control (RBAC) system. The team agreed this could be a valuable enhancement, while being mindful of not conflicting with union.ai's commercial offering.
    * [Elastic plugin UX](https://github.com/flyteorg/flyte/issues/5339)
      * Notes:
        * Niels proposed improving the configuration for shared memory used in distributed training setups, to provide a more user-friendly default experience. The team discussed technical details around mounting, timeouts, and integrating this with the flight-run fast registration process.
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * Nothing new this week
  * Open mic/questions [add your name]
      * Multi-cluster deployment
        * Datacatalog, Ingress and auth on multi-cluster (Fabio)
            
            From [docs](https://docs.flyte.org/en/latest/deployment/deployment/multicluster.html#data-plane-deployment):

            ```yaml
            configmap:
              admin:
                admin:
                  endpoint: <your-Ingress-FQDN>:443 #indicate the URL you're using to connect to Flyte
                  insecure: false #enables secure communication over SSL. Requires a signed certificate
              catalog:
                catalog-cache:
                  endpoint: <your-Ingress-FQDN>:443
                  insecure: false
            ```     
            
            How does auth work if one was to expose datacatalog through the ingress?
            
            * **Notes**: datacatalog currently doesn't use auth. The team agreed to add a disclaimer in the docs clarifying that users need to handle the networking and authentication for these cross-cluster connections.
            * [PR is merged](https://github.com/flyteorg/flyte/pull/5345)

        * Can cluster labels be specified for projects via the helm values? See [issue](https://github.com/flyteorg/flyte/issues/4029#issuecomment-2100479357). (Fabio)
        * When using the cluster in which the control plane is deployed also as a dataplane, it would be nice to use in-cluster credentials. Would you agree if I add such an option? (Fabio)
            ```yaml
            configmap:
              clusters:
               clusterConfigs:
               - name: "dataplane_1"
                 endpoint: https://<your-dataplane1-kubeapi-endpoint>:443
                 enabled: true
                 auth:
                    type: "file_path"
                    tokenPath: "/var/run/credentials/dataplane_1_token"
                    certPath: "/var/run/credentials/dataplane_1_cacert"
               - name: "controlplane"
                 inCluster: true  # Proposed flag
            ```
            
            Check [here](https://github.com/flyteorg/flyte/blob/c0f5b10777fbdfcf2b08059a270b04f0c60d7678/flyteadmin/pkg/flytek8s/client.go#L57) if flag is set.
    * Ownership of plugins. Should there be something like `flytekitplugins.contrib.x` to signal that a plugin is purely community maintained? Then some process to promote out of `.contrib`.
      * Notes
        * Fabio proposed introducing a "contrib" tag for community-maintained plugins, to help users better understand the support and maintenance levels for different plugins. The team agreed this was a good idea and will explore the details of how to implement this in a future RFC.
    * Support local pip-installable packages in ImageSpec and pyflyte run --remote: https://github.com/flyteorg/flyte/issues/5343


## April 25, 2024
* Attendees [name, affiliation]
    * Nikki Everett (Union)
    * David Espejo (Union)
    * Eric (Han-Ru) Chen (Future-Outlier)
    * Robert Ulbrich (Mercedes-Benz)
    * Eduardo Apolinario (Union)
    * Kevin Su (Union)
* Welcome new members
  * Lina Sjongren (Spotify)
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]

## April 11, 2024
* Attendees [name, affiliation]
    * Fabio Grätz (Recogni)
    * Nikki Everett (Union)
    * Dan Rammer (Union)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
  * Integrations Inventory:
    * Deliverable so far: https://github.com/flyteorg/community/blob/main/working-groups/plugin-inventory/2024-inventory.md
 * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
 * Community pulse
 * Open mic/questions [add your name]

## March 28, 2024

 * Attendees [name, affiliation]
     * Fabio Grätz
     * Dennis Keck (Recogni)
     * Nikki Everett (Union.ai)
     * Bernhard Stadlbauer (Pachama.com)
     * Eric Chen (Future Outlier) (Flyte)
     * Haytham Abuelfutuh (Union)
     * Eduardo Apolinario (Union)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Working Groups updates
    * Integrations Inventory WG
        * Flyte Integrations assessment form: https://forms.gle/7EvjuYgxpB2cb8wJ9
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * Project description for initialization: https://github.com/flyteorg/flyte/discussions/5090
    * Return K8s events: https://github.com/flyteorg/flyte/discussions/5089
    * Notifications via SMTP relay: https://github.com/flyteorg/flyte/discussions/5088
    * Project isolation: https://github.com/flyteorg/flyte/discussions/5084
  * Open mic/questions [add your name]
      * (Bernhard) Webhook notifications

## March 14, 2024
  * Attendees [name, affiliation]
    * David Espejo (Union.ai)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Working Groups updates
    * Plugin (Integrations?) Inventory WG:
      * Proposed format: https://github.com/flyteorg/community/blob/main/working-groups/plugin-inventory/2024-inventory.md
      * Details: https://github.com/flyteorg/community/blob/07dbb3e9b63fb49c11e3368a22775c4a80d1bd77/groups.yaml#L46-L66
      * We need you!
        * Suggestion: add a DATE column
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Open mic/questions [add your name]
    - (Bernhard): Updates on (Slack) webhook support
      - Related: https://github.com/flyteorg/flyte/pull/4605

## February 29, 2024
  * Attendees [name, affiliation]
      * Bernhard Stadlbauer (Pachama.com)
      * David Espejo (Union.ai)
      * Dan Rammer (Union.ai)
      * Fabio Grätz (Recogni)
      * Nikki Everett (Union.ai)
      * Han-Ru Chen (Flyte)
      * Dennis Keck (Recogni)
      * Eduardo Apolinario (Union.ai)
      * Haytham Abuelfutuh (Union.ai)
  * Welcome new members
    * Rafael Reposo (Spotify)
    * han-Run Chen
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Working Groups updates
      * Should we close out the config override?
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Community pulse
  * Open mic/questions [add your name]
    * (Bernhard) Can we update the link at the top?
    * (Bernhard) Will anyone be at KubeCon?

### Minutes
**Notification System Proposal**: Han-Ru Chen proposes adding a notification system to Flyte Interactive Plugin to notify users when the VSCode server is about to terminate. However, there's a discussion about whether this should be integrated into flyteadmin instead.  
**Cluster Pool Proposal**: Rafael Raposo presents a proposal for implementing a cluster pool feature, allowing the selection of execution time and destination clusters for workflows.
Discussion on Implementation: There's a discussion about whether existing labels for clusters can be reused for specifying execution time or if a new mechanism is needed.  
**Action Items:**  
Han-Run Chen agrees to close the notification system proposal.
Rafael and Fabio agree to explore the implementation details of the cluster pool proposal further.  
**Working Groups Update:**
The Config Overrides Working Group is discussed for possible retirement due to inactivity.  
**Incubator Ideas:**  
Existing ideas in the incubator are mentioned, with no significant updates or discussions.
Conclusion: The meeting concludes with a reminder to revisit the ideas in the incubator and an acknowledgment of potential future discussions.


## February 1, 2024
* Attendees [name, affiliation]
    * Fabio Grätz
    * David Espejo
    * Bernhard Stadlbauer (Pachama.com)
    * Niels Bantilan (Union.ai)
    * Nikki Everett (Union.ai)
    * Eduardo Apolinario (Union.ai)
* Welcome new members
    * Troy Howard (Union.ai)
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * Revisit [#4570](https://github.com/flyteorg/flyte/pull/4570#issuecomment-1899201267)
        * Ping Ethan on this
* Open mic/questions [add your name]
    * flyteconsole OSS fork [Jason]
    * Resource requests behavior (see [#2151](https://github.com/flyteorg/flytekit/pull/2151))
    * Meeting logistics [David]
    * Interested in early feedback on [this](https://github.com/flyteorg/flyte/pull/4726) PR (whether there is agreement that this is a useful feature) [Fabio]

## February 15, 2024
  * Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Fabio Grätz
    * Nikki Everett (Union.ai)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Working Groups updates
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Open mic/questions [add your name]
    * Migrating meetings to LFX
      * New Zoom : https://zoom-lfx.platform.linuxfoundation.org/meeting/92309721545?password=c93d76a7-801a-47c6-9916-08e38e5a5c1f
      * Update pinned Slack message and everywhere else
    * Alternating schedule
      * Try for 4 meetings, measure and decide
    * Plugin inventory WG?
      * +1 to form a WG to audit the status of current plugins, including flytekit integrations
      * Not all plugins are to me refactored as Agents
      * Compile a list of people responsible of specific plugins, if there's no clear owner it's a good indicator of maintenance issues
      * Nikki steps up to help too
      

## January 18, 2024
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Fabio Grätz (Recogni.com)
    * Nikki Everett (Union.ai)
    * Dan Rammer (Union.ai)
    * Eduardo Apolinario (Union.ai)
    * Bernhard Stadlbauer (Pachama.com)
* Welcome new members
    * Austin Stretz
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * [Polish "rough edges" of type engine](https://github.com/flyteorg/flyte/discussions/4544)
    * [Offloading of objects during registration is a difficult to debug trap for inexperienced users we should catch](https://github.com/flyteorg/flyte/discussions/4743)
* Open mic/questions [add your name]
    * UX of dynamic workflows. Is there capacity to tackle [this issue](https://github.com/flyteorg/flyte/issues/4466) in the frontend?
    * Dosubot's value [David]
    * Meeting logistics [David]


* **Minutes**:

Welcome and introductions @ 0:00

David welcomed attendees including new community member Austin, who aims to learn MLOps through Flyte.

Discussion of new RFCs and proposals @ 3:26

Members discussed a proposal for a .flyteignore file to ignore files during registration. They agreed Bernhard should open an issue. Kevin explained challenges with notification plugins, agreeing to discuss further offline.

Proposed .flyteignore file for ignoring files @ 19:15

Bernhard proposed a .flyteignore file to avoid unintentionally including large files during fast registration. Members agreed this could prevent user frustration and improve the experience. Bernhard offered to submit an initial implementation.

Improving object serialization between tasks @ 26:53

Fabio demonstrated an issue where objects serialized during registration are saved locally instead of the blob store. Members agreed the system should default to the blob store to avoid workflow failures. They will further discuss improving usability.

Improving dynamic workflow debugging @ 31:23

Fabio highlighted frustrations debugging dynamic workflows due to unclear errors. Members agreed the UI should surface detailed error messages from preparer to aid users. John will investigate propagating errors appropriately in the UI.

Discussion of meeting logistics and community involvement @ 41:11

David asked about meeting frequency and timezones. Members agreed to biweekly meetings but explore alternating times to include others. They aim to foster a more welcoming community through clear communication.


## January 4, 2024

* Attendees [name, affiliation]
    * Bernhard Stadlbauer (Pachama.com)
    * Dan Rammer (Union.ai)
    * Nikki Everett (Union.ai)
 * Welcome new members
     * N/A
 * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
     * #3749:
         * Not implemented yet
         * Probably needs a new name
         * A.I.: reach out to Katrina to confirm
* 

 * Working Groups updates
 * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
 * Open mic/questions [add your name]
## December 21 (cancelled due to holidays)
## December 7, 2023
* Attendees [name, affiliation]
    * Fabio Grätz (Recogni.com)
    * Dan Rammer (Union.ai)
    * Nikki Everett (Union.ai)
    * David Espejo (Union.ai)
    * 
* Welcome new members
    * Jeames and Paul
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
  * N/A
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * Flow auth inside Tasks [James Sutton]: https://github.com/flyteorg/flyte/discussions/4527
        * Also involve the Stripe team
    * Rough edges in the type engine [Fabio]:
        * Implementation needs more discussion
* Open mic/questions [add your name]
  * Getting started guide updates [Nikki]

## November 23, 2023 (Cancelled due to US Holiday)
## November 9, 2023
  * Attendees [name, affiliation]
      * David Espejo (Union.ai)
      * Fabio Grätz (Recogni.com)
      * Dan Rammer (Union.ai)
      * Troy Chiu (UCSD)
      * Bernhard Stadlbauer (Pachama.com)
      * Eduardo Apolinario (Union.ai)
      * Niels Bantilan (Union.ai)
  * Welcome new members
      * Daniel Farrell (Cyrus Biotech)
      * Nikki Everett (Tech Writer, Union.ai)
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Working Groups updates
      * Config Overrides -> halted for now
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
      * Sorting through old discussions
          * [Discussed] [Build images on the fly while registering](https://github.com/flyteorg/flyte/discussions/3397)
              * No development since March
              * Already implemented for envd
              * Currently there is a [plugin in development for docker](https://github.com/flyteorg/flytekit/pull/1926)
              * Close -> yes
              * Related: [Slack thread](https://flyte-org.slack.com/archives/C04NJPLRWUX/p1699405285278189)
          * [Discussed] [Allow disabling Flyte cache locally via env var](https://github.com/flyteorg/flyte/discussions/4192)
              * Bernhard will create PR -> close RFC
          * [Will be an RFC] [Streaming Literals](https://github.com/flyteorg/flyte/discussions/4101)
          * [First version merged, plugin, no RFC required] [VSCode decorator](https://github.com/flyteorg/flyte/discussions/4314)
              * will be a plugin that doesn't require changes in flytekit -> no RFC required
          * [Discussion will be continued in the contributor slack channel, no RFC] [Asking for feedback on Bacalhau integration](https://github.com/flyteorg/flyte/discussions/4099)
              * RFC incubator is wrong format -> close?
          * [Implementation in progress, backend changes already merged, discussion can be closed][GPU type selection](https://github.com/flyteorg/flyte/discussions/3796)
              * several different proposals for how UX could look like -> should be an RFC
          * [Save resolved execution time parameters in flyteadmin, David will ping Katrina to turn into an issue](https://github.com/flyteorg/flyte/discussions/3934)
              * This could just be an issue -> Yes.
          * [David to reach out to original authors to confirm direction. If closed, Ip should persist] [Distributed Locks](https://github.com/flyteorg/flyte/discussions/3754)
              * No development since August 1
              * Needs a champion or should be closed
          * [Make it an Issue][Run flyte exec from jupyter](https://github.com/flyteorg/flyte/discussions/3878)
              * Probably useful feature for data scientists
              * Pinged Niels what the status is here
              * Decision: make it an Issue
          * [Fabio champions RFC, Dan supports] [Feedback mechanism from task pod to propeller/use pod logs](https://github.com/flyteorg/flyte/discussions/3838)
              * Really important, let's revive this one
          * [More investigation needed to see if using Airflow Operators enables what's described here][Introduce triggers for workflows](https://github.com/flyteorg/flyte/discussions/3464)
              * No development since July 11
              * Cool feature
          * [Will be used as a use case/argument for #3838] [Customizing logging links](https://github.com/flyteorg/flyte/discussions/3666)
              * Dependant on a feedback mechanism from the task pod to flytepropeller
          * [Dependant on the development of webhooks, help wanted][Notification system including Slack](https://github.com/flyteorg/flyte/discussions/3647)
              * Important
              * What about https://github.com/flyteorg/flyte/pull/4147? @Kevin
          * [?] [Generate spark resource configuration from machine config](https://github.com/flyteorg/flyte/discussions/3655)
              * Needs a champion
          * [Already covered by Issue][Ability to add notes to executions](https://github.com/flyteorg/flyte/discussions/3646)
              * Covered by the "system tags and metadata RFC"
              * Close this discussion?
              * Is there a timeline for bringing this to flyte console?
              * Issue: https://github.com/flyteorg/flyte/issues/3960
          * [Close ][Allow users to inject secrets via `pyflyte run`](https://github.com/flyteorg/flyte/discussions/3622)
              * Needs a champion
              * Implementation in progress on Union Cloud
          * [Close][Infinitely long running tasks](https://github.com/flyteorg/flyte/discussions/3463)
              * Unsure, what is relation to the [trigger](https://github.com/flyteorg/flyte/discussions/3464) discussion?
          
          * [Address by recent contributions][Improving Launch plan UX](https://github.com/flyteorg/flyte/discussions/3333)
              * Criticizes e.g. that launchplans cannot be (de-)activated from the UI
              * Needs a champion?
  * Open mic/questions [add your name]
      * Docker plugin discussion (see PR: https://github.com/flyteorg/flytekit/pull/1926) [**Dan Farrell**]




## October 26, 2023
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Niels Bantilan (Union.ai)
    * Byron Hsu (LinkedIn)
    * Fabio Grätz (Recogni.com)
    * Eduardo Apolinario (Union.ai)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
    * Deprioritized (on hold) for now
    * Implementation effort is high
    * Not urgency so far that motivates
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * [vscode plugin](https://github.com/flyteorg/flyte/issues/4284) turning any python (AutoContainer) task to a vscode server to accelerate the debug/develop process
    * [streaming literals](https://github.com/flyteorg/flyte/discussions/4101): a streaming primitive data type.
* Community pulse
    * Issues with old docs versions (see [here](https://github.com/flyteorg/flyte/issues/4181) and [here](https://github.com/flyteorg/flyte/issues/3730) )
    * Notifications
* Open mic/questions [add your name]

## October 12, 2023
  * Attendees [name, affiliation]
      * Eduardo Apolinario (Union.ai)
      * Bernhard Stadlbauer (Pachama.com)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
       
  * Working Groups updates
      * Follow up needed to confirm. Bernhard to sync with Byron Hsu (Byron is on vacation)
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
      )
      * [Disable local caching](https://github.com/flyteorg/flyte/discussions/4192) (Bernhard)
  * Community pulse
  * Open mic/questions [add your name]
      

## September 28, 2023
  * Attendees [name, affiliation]
      * David Espejo (Union.ai)
      * Bernhard Stadlbauer (Pachama.com)
      * Eduardo Apolinario (Union.ai)
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
      * Simplify retry behavior implementation ready for review
          * Do we expose the system-level retry budget?
          * This proposal is aimed to claraify the behavior
      * 
  * Working Groups updates
      * Config Overrrides
          * Linkedin team evaluating the effort to implement the example proposed by Ketan here: https://docs.google.com/document/d/1vS9Gml1Yq-Y5ylAnhk8Iju5874xvz6b0Skd1IvKsXRQ/edit
          * Follow up needed to confirm. Bernhard to sync with Byron Hsu
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Community pulse
  * Open mic/questions [add your name]
      * Status of the monorepo (Bernhard)
          * Beta release built off the monorepo
          * Guide soon to be out to show open PR authors how to *transform* those PRs to the monorepo
          * Monorepo is reay to try it out!
      * Propeller debugging strategies (Bernhard)
          * Reported bug: https://github.com/flyteorg/flyte/issues/4087

## September 14, 2023
* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Niels Bantilan (Union.ai)
    * Eduardo Apolinario (Union.ai)
    * Fabio Grätz (Recogni.com)
    * Dennis Keck (Recogni.com)
    * Dan Rammer (Union.ai)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
    * No recent updates. Pending decision on Linkedin document
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]
    * Monorepo [Eduardo]
        * https://github.com/flyteorg/flyte/pull/4014 will make it official
        * script to move pending PRs
    * Proxy-Authorization PR/integration with GCP Identity Aware Proxy
        * flytekit PR approved by Haytham
        * Have implemented the same logic for flytectl, will add tests and create PR
## August 31, 2023
  * Attendees [name, affiliation]
      * David Espejo (Union.ai)
      * Fabio Grätz (Recogni.com)
      * Bernhard Stadlbauer (Pachama.com)
      * Dan Rammer (Union.ai)
      * Arthur Book
  * Welcome new members
  * Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
  * Outstanding RFCS:
      * Simplify retry behavior: https://github.com/flyteorg/flyte/pull/3902
              - Recent experiment by Fabio and Dennis (authors)   
              -  Looks good
  * Working Groups updates
      * Override task config RFC
          * Discussions about 3rd iteration of proposal, see [here](https://docs.google.com/document/d/1vS9Gml1Yq-Y5ylAnhk8Iju5874xvz6b0Skd1IvKsXRQ/edit#heading=h.lgx3r5ef3n4h).
  * New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
  * Open mic/questions [add your name]
      * Stale Issue [bot](https://github.com/flyteorg/flyte/pull/3984/files) [David]
      * GCP Identity Aware Proxy integration ready for review
          * https://github.com/flyteorg/flyte/issues/3965

          * https://github.com/flyteorg/flytekit/pull/1787

* Minutes:  
The team discussed an experiment they conducted to implement a minimal change in propeller to address user confusion regarding retries. They found that the implementation resolved most cases and made a small PR to adapt the one case where it didn't, awaiting feedback from customers and Eduardo.

The team discussed the behavior of retries and attempts in the system. They debated whether to switch to a non-interruptible behavior for the last system failure and considered introducing a negative number configuration value for the last retry.

David discussed updates on working groups and proposals, but there were no significant comments or new ideas. Fabio introduced a new bot in the flag repo to label and close stale issues, and also discussed the GCP identity hour proxy initiative, which aims to enhance security by allowing only authenticated requests to reach the back end.

Fabio and Haytham discussed the authentication setup for integrating a proxy with the flyteadmin. They explored different options, including using ID tokens and proxy authorization headers, and discussed the possibility of extending the authentication mechanism to other proxies in the future.

Haytham asked about the dependency on Google libraries in a command. Fabio explained that the command uses a standard OAuth2 flow with a dependency on a Google library, but it is only added to the specific plugin and not to the main flyteKit. They agreed to discuss further offline or in the next meeting
           

## August 17, 2023

* Attendees [name, affiliation]
    * David Espejo (Union.ai)
    * Fabio Grätz (Recogni.com)
    * Bernhard Stadlbauer (Pachama.com)
    * Eduardo Apolinario (Union.ai)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
    * Config overrides
        * See: https://docs.google.com/document/d/1vS9Gml1Yq-Y5ylAnhk8Iju5874xvz6b0Skd1IvKsXRQ/edit
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Open mic/questions [add your name]
    * Monorepo [Eduardo]
    * GCP Identity Aware Proxy [Fabio]
        * https://github.com/flyteorg/flyte/issues/3965

* Notes

  
  - In the discussion, Eduardo suggested internally updating the retry behavior RFC or proposing an alternative, while Fabio mentioned resolving questions and trying a prototype PR in the staging cluster. They also discussed renaming the extra plugin service to "Flyte agents" and the progress of other RFCs. 
  - The team discussed various proposals and ideas, including an alternative software use case, the implementation of overrides in workflows, and a proposal to resolve execution time parameters in the database. They also talked about the possibility of merging the Flyte-related repositories into a mono repo to improve the development experience.
  - In the discussion, Eduardo informed everyone that they were moving to a monorepo, which would streamline the development experience and make it easier for contributors to make single PRs. Bernhard expressed his support for the move, mentioning that it would lower the entry barrier for contributors and make it easier to test changes. 
  - Fabio discussed the implementation of encryption between the load balancer and the backend using Flight Admin, and mentioned the possibility of rotating the server certificates using a Terraform resource. He also mentioned the integration of identity-web anonymously and the decision to implement it on the client side for easier deployment.
  - Fabio discussed his idea of extending the authentication process by running a second command to generate a token for a proxy in front of the application. He opened a pull request for a plugin called Flight IAP and mentioned the need for someone from the team to review and test it.
  



## August 3, 2023
* Attendees [name, affiliation]
  * David Espejo (Union.ai)
  * Dan Rammer (Union.ai)
  * Dennis Keck (recogni.com)
  * Byron (LinkedIn)
  * Bernhard Stadlbauer (Pachama.com)
  
* Welcome new members
  * Linkedin team
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
  * Config Overrides
    * Potential bug on the `hook` idea. See [thread](https://flyte-org.slack.com/archives/C05A4PNMKL1/p1691037878571179)
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
* Community pulse
  * [Improve error messages](https://github.com/flyteorg/flyte/issues?q=is%3Aissue+is%3Aopen+error+message+label%3Aimprove-error-message)
* Open mic/questions [add your name]
  * Downward trend on Closed/Open issue rate [David]:
  
  | Metric | Q422  | Q123  | Q223|
  |---|---|---|---|
  | Time to first review (days)  | 8  |5.8  |5.83|
  |Closed/created issue rate |1.47 |0.75(-49%) | 0.77 (+2.6%)|
  |New issues|173|238(+37%)|172(-27%)|
  |Time to merge (days)|49|43|25|
  
  **Source**: https://insights.lfx.linuxfoundation.org/projects/lfai%2Fflyte/dashboard;quicktime=time_filter_3Y

## July 20, 2023
* Attendees [name, affiliation]
  * Fabio Grätz (recogni.com)
  * Eduardo Apolinario (Union.ai)
  * Niels Bantilan (Union.ai)
* Welcome new members
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
    * Config overrides RFC -> Linkedin will take lead because of internal deadline
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * Jupyter run: https://github.com/flyteorg/flyte/discussions/3878
    * [Feedback from flytekit to propeller via logs](https://github.com/flyteorg/flyte/discussions/3838)
    * [Unify retry behaviour of interruptible tasks](https://github.com/flyteorg/flyte/discussions/3793)
* Community pulse
* Open mic/questions [add your name]
    * [Type support for pydantic base models](https://github.com/flyteorg/flytekit/pull/1660)
        * Alpha release off of this branch to help in testing
        * pandera support for pydantic v2: https://github.com/unionai-oss/pandera/pull/1253/

## July 6, 2023
* Attendees [name, affiliation]
    * Fabio Grätz (recogni.com)
    * David Espejo (Union.ai)
    * Dan Rammer (Union.ai)
    * Bernhard Stadlbauer (Pachama.com)
    * Arthur Book
* Welcome new members
    * Maria Slanova (schibsted.com)
    * Dennis Keck (recogni.com)
* Introduce [new RFCs](https://github.com/orgs/flyteorg/projects/12/views/1)
* Working Groups updates
* New ideas in [the incubator](https://github.com/flyteorg/flyte/discussions/categories/rfc-incubator)
    * [Feedback from flytekit to propeller via logs](https://github.com/flyteorg/flyte/discussions/3838)
    * [Unify retry behaviour of interruptible tasks](https://github.com/flyteorg/flyte/discussions/3793)
* Community pulse
    * Sensor mechanism
        * [Slack thread](https://flyte-org.slack.com/archives/CP2HDHKE1/p1688039960761709)
       * Related incubator entry: https://github.com/flyteorg/flyte/discussions/3754
* Open mic/questions [add your name]
    * Nomination for new contributor: https://github.com/flyteorg/community/issues/11
    * Governance updates: https://github.com/flyteorg/community/pull/15
    * [Type support for pydantic base models](https://github.com/flyteorg/flytekit/pull/1660#issuecomment-1623990301)


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

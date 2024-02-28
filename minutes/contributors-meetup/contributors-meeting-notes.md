# Flyte Contributors meetup - meeting notes archive

-----
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

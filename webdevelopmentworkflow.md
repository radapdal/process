# Web Development Workflow

Work smarter, not harder.



## Goals

The goal of this workflow is to increase productivity by letting the Agile nature of software requirements take its course and handle it efficiently and effectively.

This workflow aims to:

- Remove guesswork, constant recycling of tasks, and instill Test-First philosophy by adding a Definition phase so that management, developer, and QA are on the same page before an issue is even started.
- Provide a more accurate estimate on issues via Points system.
- Reduce QA failures and back-and-forth delay in communication by means of QA Demos.
- Promote discussion and eliminate miscommunication of requirements by having Daily Standup meetings and Backlog grooming.
- Improve on previous and future work by means of Sprint Meetings and Sprint Retrospectives.
- Push a steady stream of shippable project iterations via Releases so that the client and the team can see the progress and current state of the project.



## The Workflow

![workflow](https://github.com/radapdal/process/blob/master/images/SoftwareDevelopmentWorkflow.v.2.2.jpg)

https://yempo-solutions.atlassian.net/secure/admin/EditWorkflowScheme.jspa?schemeId=10837


For **Sprint Workflow**, start at [**Sprint Meeting**](#sprint-meeting).

For **Services Workflow**, jump to [**Services**](#services).



## Sprint Meeting

Before the workflow starts the whole team gets to participate in the Sprint Meeting. In this meeting, the initial requirements for this iteration is introduced, clarified, defined, and estimated. At this point, everyone will be looking at the Open issues and its order based on priority.

- Ask questions regarding the issues.
- Work with the team on how to define.
- Provide an honest estimate in hours.


### Backlog Grooming

> **Open**

Backlog grooming is the re-prioritization of Open issues and description update, this is done by Management and communicated in the Sprint or Daily meeting.


### Internal Definitions

Here the requirement's criteria of completion are defined by the team to the best of their ability to make it easier for development and testing.


Before proceeding, it is best to fully understand the Issue types used in this workflow. [**Know Your Issue Types**](#know-your-issue-types).


#### Approval


> **Defined and Approved**
>
> `OPEN TICKET` -> `DEFINITION APPROVED`

Once the definitions are completed, it is confirmed by the Project Coordinator. Always try to get complete approval on all definitions before starting the sprint to avoid recycle.


### Point Estimates

Points are added to all issues for the sprint. Point estimates are used to represent task difficulty, not estimated time. This is meant to provide a consensus on team members on how difficult they think the task is and is used to measure total difficulty of the iteration. 

Point system is defined by Fibonacci Sequence for increasing difficulty: **1** **2** **3** **5** **8** **E**

- **1** is very easy
- **2** is easy
- **3** is moderate
- **5** is hard
- **8** is very hard
- **E** needs breakdown

Team discussion:

- Present your point estimate.
- Discuss shortly why that is your estimate.
- Use the most voted number.

The individual estimate by hour is added by the developer that intends to work on the issue at the Daily Meeting.



## Development

After the Sprint Meeting, and the iteration issues are approved and ready for work, the sprint can now start building.


### Daily Meeting

This short standup meeting is best done if everyone is looking at the same board so it is easy to point out issues.

- Start by declaring issues you worked on yesterday.
- Point out blocked issues and those you were not able to move. Tag people that might clear said Blockers for a quick discussion later.
- Then "grab" issues you intend to work on today by assigning issues to yourself and pushing it to Dev Ready.

> **For Development**
>
> `DEFINITION APPROVED` -> `DEV READY`


Everyone will do the same until the Ready list is filled with tasks to be moved by the day. In this way it is easy for the team to see who is having a hard time or if the team can do more by grabbing more issues from the backlog.

After the meeting, immediately follow up with the help regarding issue Blockers so it can be unblocked, the longer an issue rests as Blocked the more the risk of the sprint not meeting its end date.

Quick Tip: Keep the Daily Meeting concise and only discuss the current position of each team member, more strategic discussions should be done outside this meeting.



### DevQA Workflow

#### Dev Flow

The Ready list and Devs are now ready. Begin by reviewing the definitions, then move the issue to Dev In Progress.

> **Start Development**
>
> `DEV READY` -> `DEV IN PROGRESS`

There will be a lot of times wherein upon development, some criteria will not be met due to difference in systems and expectations. Definitions are not set in stone and was created to be a guide before starting work. Communicate the problem to the Project Lead and check if it is within expected outcome and merits a definition update.

After fulfilling the issue requirements in the development push the changes to staging and transition the issue to its next state.

Issues with criteria should be pushed to QA. Assign, comment, and tag the QA accordingly.

> **For QA**
>
> `DEV IN PROGRESS` -> `QA READY`

Technical Tasks can be pushed for release immediately after completing.

> **Issue Completed**
>
> `DEV IN PROGRESS` -> `RELEASE READY`

If there is unfulfilled criteria due to missing requirement or a major change in definition should be requested, push the issue to Blocked, and make sure to Flag it. Assign, comment, and tag the Project Lead accordingly.

> **Issue is Blocked**
>
> `DEV IN PROGRESS` -> `BLOCKED`

#### QA Flow

When a QA is ready for testing, move the issue to QA In Progress.

> **Start QA**
>
> `QA READY` -> `QA IN PROGRESS`

Test the criteria and do exploratory testing within the borders of the issue. Note scenarios tested and corresponding results. Add screenshots for clarity. After testing move the issue to its next state.

Issues that passed all criteria will be pushed to Release Ready for Internal UAT. Assign, comment, and tag the Project Lead.

> **QA Approved**
>
> `QA IN PROGRESS` -> `RELEASE READY`

Those that failed the criteria will be sent to QA Failed. Reassign, comment, and tag the issue developer. Schedule a QA Demo if necessary.

> **QA Failed**
>
> `QA IN PROGRESS` -> `QA FAILED`

If issue could not be tested due to circumstances, move it to Blocked and Flag it. Assign, comment, and tag the Project Lead accordingly.

> **Issue is Blocked**
>
> `QA IN PROGRESS` -> `BLOCKED`

**QA Demo**

A QA Demo can be requested when there are problematic results from scenarios tested thats needs to be demonstrated to the issue developer for replication and clarity. Communicate with the issue developer and agree upon a scheduled short meeting. Demonstrate the problems found and how it was achieved, discuss if this can be immediately addressed in parallel while meeting, or too big of an issue and be handled separately. Resolve all problems that can be resolved in this meeting and process the remaining issues accordingly.

**Handling missed criteria**

Upon testing, there will also be times when a scenario or result is pointed out that may not be intended with regards to the issue being developed. In this case communicate the result to the issue developer, see if it is intended or not. 

- If it is **intended but not in the definitions**, or if it is **not intended but within scope** of the issue, relay to the Project Lead and check merit for definition update.
- If it is **not intended and is out of scope** of the issue, tag the Project Lead and request for processing.

Comment the resolution and proceed with the testing workflow.


### Additional Requests mid-Sprint and How to Deal with them

Most of the time scope creep will slowly seep into the sprint, either by clients constantly updating requirements or team members unknowingly adding more.

To monitor and handle these, follow the guideline below.

A change to the requirements will be accepted within the same sprint ONLY IF:

- The change has been confirmed and negotiated with the client.
- The change aligns well with the value proposition of a story in the sprint.
- The change is small and can be completed before sprint production release.
- The change has been identified at least 2-3 days before sprint production release.



## Release 

When all sprint issues are finally moved to Release Ready, it is now ready for the release process.


### Release Notes

The Project Lead will collect the Release Notes from the Release manager in JIRA. This document briefly outlines the things to review for this sprint.


### UAT

When all sprint issues are in "Release Ready", the system being worked on is turned over along with the Release Notes for review. The assessment can take some time and it is within the management's decision to proceed with the next sprint or not.


### 2 Step UAT

#### Internal UAT

In order to combat the issue of relying too much on the response of the client for verification, an internal layer of confirmation is added to assure that the development process flows smoothly. This can also entail that the release can be accepted when the client takes too long to verify.

> **For Internal UAT**
>
> `RELEASE READY` -> `RELEASED INTERNAL`

- Make sure that all sprint issues are in Release Ready
- Project Lead will collect and prepare the Release Notes.
- Modify notes to add Timeline of sprint.
- Upload Release Notes to sharepoint and copy share URL.
- Transition all sprint issues to "Released Internal".
- Reassign sprint issues to Product Owner, and bulk comment on the issues.
- Set a schedule for an Internal UAT Demo with the project management regarding the release.

Based on the Internal UAT results, confirm acceptance for all issues. For review problems, see [**Issues from UAT**](#issues-from-uat) below.

#### Client UAT

When all sprint issues are internally reviewed and accepted, Project Coordinator will confirm to the client that the staging site is ready for their review. Project Lead will transition issues to "Released to Client".

> **For Client UAT**
>
> `RELEASE INTERNAL` -> `RELEASED TO CLIENT`

Clients will sometimes take too long to review, so at an acceptable time (up to 2 weeks) after staging release, it is up to the management to decide if the team waits longer, or treat the release as client accepted so other sprints can start rolling.


### Issues from UAT

If the UAT returns with additional requests, which it almost always will, take time to review the new requirements. Note that the initial committed requirements at this point has already been fulfilled, and other issues from the next sprint might take priority.

To process these, treat them as Additional Requests and see [**Additional Requests mid-Sprint and How to Deal with them**](additional-requests-mid-sprint-and-how-to-deal-with-them).

Failed issues by client review will undergo change rollback and is recycled back to the workflow.

> **Deployment Rollback**
>
> `RELEASED TO CLIENT` -> `REOPENED`


### Getting ready for Production

When the client is ready to push the staged changes to production, it's time to get ready for Production Deployment. 

- Create Deployment Checklist.
- Relay checklist to the Project Coordinator and agree on a deployment schedule with the client. 
- Project Lead will grab sprint issues.
- Update sprint due date to the scheduled deployment date.


### Deployment

See [Deployment Procedures](https://github.com/radapdal/process/blob/master/deploymentprocedures.md).

A QA must be delegated for review and be on stand-by during the deployment. After successfully deploying the system to production, the assigned QA will then verify the deployment.

After a successful deployment and verification, transition issues to "Released to Production".

> **Deployed to Production**
>
> `RELEASED TO STAGING` -> `RELEASED TO PRODUCTION`

Comment, and tag the Project Coordinator for client verification. If the client verifies the release, or after a designated time after verification (3 days) the sprint issues can now be safely closed.

> **Deployed Approved**
>
> `RELEASED TO PRODUCTION` -> `CLOSED`

#### Issues after Deployment

If a problem is unfortunately found due to the deployment, target the source from the sprint issues then assess problem as an [**Additional Request**](#additional-requests-mid-sprint-and-how-to-deal-with-them).

Issues that are deemed to be crucial will be inserted back to the sprint, Flagged, set to highest Priority, and cycled to the development workflow with urgency.

> **Deployment Rollback**
>
> `RELEASED TO PRODUCTION` -> `REOPENED`

When the issue is cycled successfully and the QA confirms the deployment, Project Lead will release the issue as part of the completed sprint.


### Sprint Retrospective

This meeting is scheduled right after a successful sprint release.

It tackles:

- status of expectations for current sprint
- highs and lows of each team member
- workflow improvement
- expectations for the next sprint




----




# Services 

After a successful website build and release, or a new client requires site maintenance and support, the workflow will seamlessly transition to a Continuous Delivery release.

**Continuous vs Sprinting**

In Sprints, we release large chunks of the software as one Major version. This means grouping issues beforehand, developing and testing them, then sending them for a 2-Step UAT before pushing to Production.

However, in a Continuous Delivery process, issues are individually assessed to a target version in Staging or Production, and can bypass UAT. This release process allows for two things: 
	
	1. Allows the Staging to build up Minor versions and be pushed when required.
    2. Allows emergency Patches to push ahead of the versions in staging directly into Production.


## Workflow

To properly understand the distinction of where issues would go, see ["Versioning"](#versioning).

Basically, Major versions will be developed on the Sprint board, while Minor versions and Patches will be handled by the Service Kanban.

The Service Kanban will follow the same DevQA process with minor changes to the Release pipeline. 

> **QA Approved**
>
> `QA IN PROGRESS` -> `RELEASE READY`

When an issue is approved by QA, it is moved to "Release Ready" for assessment of the Project Lead.

- Minor version issues will sit at "Release Ready" to wait for the other issues in the version before so it can undergo UAT.

> **For Internal UAT**
>
> `RELEASE READY` -> `RELEASED INTERNAL`

> **For Client UAT**
>
> `RELEASED INTERNAL` -> `RELEASED TO CLIENT`

- Patches will bypass UAT and be immediately pushed to Production.

> **Patch Deployed to Production**
>
> `RELEASE READY` -> `RELEASED TO PRODUCTION`

Some issues are also expected to be completed on a target environment and does not need to be pushed further into the release pipeline. These issues can be transitioned to "Closed" after QA Verification.

> **Release Approved**
>
> `RELEASED INTERNAL` -> `CLOSED`

> **Release Approved**
>
> `RELEASED TO STAGING` -> `CLOSED`

> **Release Approved**
>
> `RELEASED TO PRODUCTION` -> `CLOSED`




----




# KNOWGLEDGE BASE


### Know your Issue Types 

#### Task vs Story vs Bug

Issues are primarily divided into Tasks, Stories, and Bugs

***Tasks*** 

Issues that can affect user experience but does not directly pertain to user behaviour.

Tasks are further differentiated as Technical Task, Content Task, and Maintenance Task.

- *Technical Tasks* - issues that need no internal testing, as it is a requirement for other issues.

   Ex. Setup site skeleton, create new admin user

- *Content Tasks* - issues that affect user experience.

   These are defined and tested via **UX Criteria**. 

   Ex. Reduce font size, change menu color, delete section

- *Maintenance Tasks* - issues for the website maintenance service.

   These are defined and tested by the **Update Impact** and detailed in the  site's Maintenance Log.
  
   Ex. Update Impact:
   
   - MAJOR: Woocommerce update, check cart design and total calculations

***Stories***

Issues that pertain to specific user behavior and its results.

These are defined and tested via **Acceptance Criteria**.

Ex. As a user I want to add an item to cart So I can include it in my checkout.

- able to view option to add to cart
- redirected to cart page on click
- able to see item in cart page and list

***Bugs***

Bugs are issues that are found in Production. They are either tasks or stories.

These are tested using either UX Criteria or Acceptance Criteria or both, whichever is applicable.

Ex. Fix product add to cart button not showing in mobile


### Versioning

#### MAJOR.MINOR.PATCH

From [**Semantic Versioning 2.0.0**](https://semver.org)

Given a version number MAJOR.MINOR.PATCH, increment the:

1. MAJOR version when you make incompatible API changes,
2. MINOR version when you add functionality in a backwards-compatible manner, and
3. PATCH version when you make backwards-compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.




----

Congratulations you have released a sprint! Cheers!

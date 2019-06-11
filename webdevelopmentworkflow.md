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



## The Workflow

![workflow](https://github.com/radapdal/process/blob/master/SoftwareDevelopmentWorkflow.v.3.0.jpg)

https://yempo-solutions.atlassian.net/plugins/servlet/project-config/SC/workflows




## 1. Sprint Meeting

Before the workflow starts the whole team gets to participate in the Sprint Meeting. In this meeting, the initial requirements for this iteration is introduced, clarified, defined, and estimated. At this point, everyone will be looking at the Open issues and its order based on priority.

- Ask questions regarding the issues.
- Work with the team on how to define.
- Provide an honest estimate.

### 1.1 Backlog Grooming

> **Open**

Backlog grooming is the re-prioritization of Open issues and description update, this is done by the Project Manager and communicated in the Sprint or Daily meeting.

### 1.2 Internal Definitions

> **Start defining**
>
> `OPEN` -> `DEFINITION IN PROGRESS`

Here the requirement's criteria of completion are defined by the team to the best of their ability to make it easier for development and testing.

### Know your Issue: Task vs Story vs Bug

Issues are primarily divided into Tasks, Stories, and Bugs

***Tasks*** 

Issues that can affect user experience but does not pertain to his/her behavior.

Tasks are further differentiated as Technical Task, Content Task, and Maintenance Task.

- *Technical Tasks* - issues that need no internal testing, as it is a requirement for other issues.

   Ex. Setup site skeleton, create new admin user

- *Content Tasks* - issues that affect user experience but does not pertain to his/her behaviour. 

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


### Approval


> **Definition is approved**
>
> `DEFINITION IN PROGRESS` -> `DEFINITION APPROVED`

Once the definitions are completed, it is confirmed by the Project Manager. Always try to get complete approval on all definitions before starting the sprint to avoid recycle.

### 1.3 Point Estimates

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

After the Sprint Meeting, and the iteration issues are approved and ready for work, the sprint can now start on its intended start date.

### Daily Meeting

This short standup meeting is best done if everyone is looking at the same board so it is easy to point out issues.

- Start by declaring issues you worked on yesterday.
- Point out blocked issues and those you were not able to move.
- Then grab issues you intend to work on today by assigning issues to yourself and pushing it to Dev Ready.

> **For development**
>
> `DEFINITION APPROVED` -> `DEV READY`


Everyone will do the same until the Ready list is filled with tasks to be started by the day. In this way it is easy for the team to see who is having a hard time or if the team can do more by grabbing more issues from the backlog.

Quick Tip: Keep it concise and only discuss the current position of each team member, more strategic discussions should be done outside this meeting.




### DevQA Workflow


#### Dev Flow

The Ready list and Devs are now ready. Begin by reviewing the definitions, add the estimate in hours, then move issue to Dev In Progress.

> **Start development**
>
> `DEV READY` -> `DEV IN PROGRESS`

There will be a lot of times wherein upon development, some criteria will not be met due to difference in systems and expectations. Definitions are not set in stone and was created to be a guide before starting work. Communicate the problem to the Dev Lead and check if it is within expected outcome and merits a definition update.

After fulfilling the issue requirements in the target environment, push the issue to its next state.

Issues with criteria should be pushed to QA. Assign, comment, and tag the QA accordingly.

> **For QA**
>
> `DEV IN PROGRESS` -> `QA READY`

Technical Tasks can be Closed immediately after completing.

> **Task is complete**
>
> `DEV IN PROGRESS` -> `CLOSED`

If there is unfulfilled criteria due to missing requirement or a major change in definition should be requested, push the issue to Blocked, and make sure to Flag it. Assign, comment, and tag the Project Manager accordingly.

> **Issue is blocked**
>
> `DEV IN PROGRESS` -> `BLOCKED`


#### QA Flow

When a QA or Dev is ready for testing, move the issue to QA In Progress.

> **Start QA**
>
> `QA READY` -> `QA IN PROGRESS`

Test the criteria and do exploratory testing within the borders of the issue. Note scenarios tested and corresponding results. Add screenshots for clarity. After testing move the issue to its next state.

Issues that passed all criteria will be pushed to Acceptance Ready for client UAT. Assign, comment, and tag the Project Manager.

> **For acceptance**
>
> `QA IN PROGRESS` -> `ACCEPTANCE READY`

Those that failed the criteria will be sent to QA Failed. Reassign, comment, and tag the issue developer. Schedule a QA Demo if necessary.

> **Found issue in QA**
>
> `QA IN PROGRESS` -> `QA FAILED`

If issue could not be tested due to circumstances, move it to Blocked and Flag it. Assign, comment, and tag the Project Manager accordingly.

> **Issue is blocked**
>
> `QA IN PROGRESS` -> `BLOCKED`


**QA Demo**

If a QA Demo is deemed necessary, mostly when there are problematic results from multiple scenarios and definitions tested, communicate with the issue developer and agree upon a scheduled short meeting. Demonstrate the problems found and how it was achieved, discuss if this can be immediately addressed in parallel while meeting, or too big of an issue and be handled separately. Resolve all problems that can be resolved in this meeting and process the outstanding issues accordingly.


**Handling missed criteria**

Upon testing, there will also be times when a scenario or result is pointed out that may not be intended with regards the issue being developed. In this case communicate the result to the issue developer, see if it is intended or not. 

- If it is intended but not in the definitions, relay to the Dev Lead and check merit for definition update.
- If it is not intended but within the scope of the issue, relay to the Dev Lead and check merit for definition update.
- If it is not intended and is out of scope of the issue, tag the Project Manager and request for processing.

Comment the resolution and proceed with the testing workflow.



### Additional Requests mid-Sprint and how to deal with them

Most of the time scope creep will slowly seep into the sprint, either by clients constantly updating requirements or team members unknowingly adding more.

To monitor and handle these, follow the guideline below.

A change to the requirements will be accepted within the same sprint ONLY IF:

- The change has been confirmed and negotiated with the client.
- The change aligns well with the value proposition of a story in the sprint.
- The change is small and can be completed before sprint production release.
- The change has been identified at least 2-3 days before sprint production release.




## Release 

When all sprint issues are finally moved to Acceptance Ready, it is now ready for the release process.



### Release Notes

The Dev Lead will collect the Release Notes from the Release manager in JIRA. This document briefly outlines the expected modules of the project for easier review.



### UAT

The system being worked on is turned over to the client along with the Release Notes for review. This can take some time and it is within the management's decision to proceed with the next sprint or not.



### Issues from UAT

If the UAT returns with additional requests, which it almost always will, take time to review the new requirements. Note that the initial agreed-upon requirements at this point has already been fulfilled, and the system is already shippable.

To process these, treat them as Additional Requests and see "Additional Requests mid-Sprint and how to deal with them".

Failed definitions by client review will be recycled back to the workflow.

> **Found issue in definition**
>
> `ACCEPTANCE READY` -> `REOPENED`



### Getting ready for Production

When all is well and the sprint definitions are fully accepted by the client, it's time to get ready for deployment. 


- Relay deployment procedures and agree on a deployment schedule with the client. 
- Dev Lead will transition sprint issues to Awaiting Release.

> **Definitions accepted**
>
> `ACCEPTANCE READY` -> `AWAITING RELEASE`

- Update sprint due date to schedule deployment date.



### Deployment

See [Deployment Procedures](https://github.com/radapdal/process/blob/master/deploymentprocedures.md).

A QA must be delegated for review and be on stand by during the deployment.


### Verification and JIRA Release

After successfully deploying the system to production, push sprint issues to Released to Prod.

> **Deployed to Prod**
>
> `AWAITING RELEASE` -> `RELEASED TO PROD`

The assigned QA will then verify the production deployment.


#### Issue after Deployment

If a problem is unfortunately found due to the deployment, target the source from the sprint issues then assess problem as an Additional Request (see "Additional Requests mid-Sprint and how to deal with them").

Issues that are deemed to be crucial will be inserted to the sprint, Flagged, set to highest Priority, and cycled to the development workflow with urgency.

When the QA confirms the successful deployment, Dev Lead will release the sprint:

- In JIRA Releases, on the Sprint row, choose Edit.
- Change sprint name to the respective Version number based on [Release Versioning Guideline](https://semver.org/). Save.
- Select the release, on the top right press Release.
- Verify release date and click Release. This will only tag all version issues to the updated version name.
- Manually transition version issues to Closed to close them.

> **Deployed verified**
>
> `RELEASED TO PROD` -> `CLOSED`



### Sprint Retrospective

This meeting is scheduled right after a successful sprint release.

It tackles:

- expectations for this sprint
- highs and lows of each team member
- workflow improvement
- expectations for the next sprint

---

Congratulations you have released a sprint! Cheers!

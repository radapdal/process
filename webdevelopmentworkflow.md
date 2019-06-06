# Web Development Workflow

Work smarter, not harder.



## Goals

The goal of this workflow is to increase productivity by letting the Agile nature of software requirements take its course and handle it efficiently and effectively.

This workflow aims to:

- remove guesswork and constant recycling of tasks by adding a Definition phase so that management, developer, and QA are on the same page
- reduce QA issues and back-and-forth delay in communication by means of QA Demos
- promote discussion and eliminate miscommunication of requirements by having Daily Standup meetings and Backlog grooming
- improve on previous and future work by means of Retrospectives and Sprint Meetings
- provide a more accurate estimate on tasks via Points system



## The Workflow

![workflow](https://github.com/radapdal/process/blob/master/SoftwareDevelopmentWorkflow.v.3.0.jpg)

https://yempo-solutions.atlassian.net/plugins/servlet/project-config/SC/workflows




## 1. Sprint Meeting

Before the workflow starts the whole team gets to participate in the Sprint Meeting. In this meeting, the initial requirements for this iteration is introduced, clarified, defined, and estimated. At this point, everyone will be looking at the Open issues and its order based on priority.

- ask questions regarding the tasks
- work with the team on how to define an issue
- provide an honest estimate

### 1.1 Backlog Grooming

> **Open**

Backlog grooming is the re-prioritization of Open issues and description update, this is done by the Project Manager and communicated in the Sprint or Daily meeting.

### 1.2 Internal Definitions

> **Start defining**
>
> `OPEN` -> `DEFINITION IN PROGRESS`

Here the requirement's criteria of completion are defined by the team to the best of their ability to make it easier for testing.

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

   These are defined and tested by the update impact and detailed in the  site's Maintenance Log.
  
   Ex. Update Impact:
   
   - Woocommerce major update: check cart design and total calculations

***Stories***

Issues  that pertain to specific user behavior and its results.

These are tested via **Acceptance Criteria**.

Ex. As a user I want to add an item to cart So I can include it in my checkout.

- able to view option to add to cart
- redirected to cart page on click
- able to see item in cart page and list

***Bugs***

Bugs are issues that are found in Production. They are either tasks or stories.

These are tested using either UX Criteria or Acceptance Criteria or both, whichever is necessary.

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

- present your point estimate
- discuss shortly why that is your estimate
- use the most voted number

The individual estimate by hour is added by the developer that intends to work on the issue at the daily meeting.




## Development

After the Sprint Meeting, and the iteration issues are approved and ready for work, the sprint can now start on its intended start date.

### Daily Meeting

This short standup meeting is best done if everyone is looking at the same board so it is easy to point out issues.

- start by declaring issues you worked on yesterday
- point out blocked issues and those you were not able to move
- then grab issues you intend to work on today by assigning issues to yourself and pushing it to Dev Ready

> **For development**
>
> `DEFINITION APPROVED` -> `DEV READY`


Everyone will do the same until the Ready list is filled with tasks to be started by the day. In this way it is easy for the team to see who is having a hard time or if the team can do more by grabbing more issues from the backlog.

Quick Tip: Keep it concise and only discuss the current position of each team member, more strategic discussions should be done outside this meeting




### DevQA Workflow


**Dev Flow**

The Ready list and Dev are now ready. Begin by simply moving an issue to Dev In Progress.

> **Start development**
>
> `DEV READY` -> `DEV IN PROGRESS`

There will be a lot of times wherein upon development, some criteria will not be met due to difference in systems and expectations. Definitions are not set in stone and was created to be a guide before starting work. Communicate the change to your team, if it is within relative expected outcome feel free to modify the definitions.

After fulfilling the issue requirements in the target environment, push the issue to its next state.

Issues with criteria should be pushed to QA. Assign, comment, and tag the QA accordingly.

> **For QA**
>
> `DEV IN PROGRESS` -> `QA READY`

Technical Tasks can be Closed immediately after completing.

> **Task is complete**
>
> `DEV IN PROGRESS` -> `CLOSED`

If there is unfulfilled criteria due to missing requirement or a major change in criteria should be requested, push the issue to Blocked, and make sure to Flag it. Assign, comment, and tag the Project Manager accordingly.

> **Issue is blocked**
>
> `DEV IN PROGRESS` -> `BLOCKED`


**QA Flow**

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

Upon testing, there will also be times when a result is found not relative to the criteria being tested. In this case communicate the result to the issue developer, see if it is intended or not. 

- If it is intended but not in the definitions, update the definition.
- If it is not intended but within the scope of the issue, update the definition.
- If it is not intended and is out of scope of the issue, tag the Project Manager and request for processing.

Comment the resolution and proceed with the testing workflow.




## Release 


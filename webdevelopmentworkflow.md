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

Tasks are further differentiated as Technical Task and Content Task.

- *Technical Tasks* - issues that need no internal testing, as it is a requirement for other issues.

   Ex. Setup site skeleton, create new admin user

- *Content Tasks* - issues that affect user experience but does not pertain to his/her behaviour. 

   These are tested via **UX Criteria**. 

   Ex. Reduce font size, change menu color, delete section

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

After fulfilling the issue criteria in the target environment, push the issue to its next state.

Content Task and Stories should be pushed to QA. Assign, comment, and tag the QA accordingly.

> **For QA**
>
> `DEV IN PROGRESS` -> `QA READY`

Technical Task should be pushed to Closed.

> **Task is complete**
>
> `DEV IN PROGRESS` -> `CLOSED`

If there is unfulfilled criteria due to missing requirement or a change in criteria should be requested, push the issue to Blocked, and make sure to Flag it. Assign, comment, and tag the Project Manager accordingly.

> **Issue is blocked**
>
> `DEV IN PROGRESS` -> `BLOCKED`


**QA Flow**

When a QA or Dev is ready for testing, move the issue to QA In Progress.

> **Start QA**
>
> `QA READY` -> `QA IN PROGRESS`

Test the criteria and do exploratory testing within the borders of the issue. Note scenarios tested and corresponding results. Add screenshots for clarity. After testing move the issue to its next state.

> **For acceptance**
>
> `QA IN PROGRESS` -> `ACCEPTANCE READY`

> **Found issue in QA**
>
> `QA IN PROGRESS` -> `QA FAILED`

> **Issue is blocked**
>
> `QA IN PROGRESS` -> `BLOCKED`

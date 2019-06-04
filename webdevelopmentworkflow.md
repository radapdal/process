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

Here the requirement's criteria of completion are defined by the team.

**UX Criteria** - are requirements that affect a user experience but does not pertain to his/her behaviour.

Ex. Reduce font size, change menu color, delete section

**Acceptance Criteria** - are requirements that pertain to specific user behaviour and its results

Ex. Able to add item to cart from the product page, redirected to cart page

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

> **For development**
>
> `DEFINITION APPROVED` -> `DEV READY`

### DevQA Workflow

> **Start development**
>
> `DEV READY` -> `DEV IN PROGRESS`

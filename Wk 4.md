# Software Engineering – Week 4 Exam Notes

## Software Project Management

Week 4 introduces **Software Project Management**, which deals with planning, organizing, monitoring, and controlling software development so that projects are completed **on time, within budget, and according to customer requirements.** 

---

# 1. What is Software Project Management?

## Definition

Software Project Management is the process of

* Planning
* Organizing
* Leading
* Monitoring
* Controlling

software development activities to successfully complete a project.

---

## Why is Project Management needed?

Software development involves

* Many developers
* Multiple user stories
* Several modules
* Tight schedules
* Limited budget

Without proper management,

* deadlines slip,
* costs increase,
* quality decreases.

---

# 2. Project Manager

## Definition

A Project Manager is responsible for managing all aspects of the software project.

The project manager acts as the bridge between

* Customers
* Stakeholders
* Development team

and ensures that customer needs are satisfied while the project progresses on schedule. 

---

## Responsibilities of a Project Manager

Remember these.

* Form the development team
* Assign work
* Plan the project
* Estimate cost and effort
* Create schedules
* Manage risks
* Communicate with customers
* Resolve conflicts
* Monitor progress
* Ensure timely completion

---

# 3. Main Activities in Software Project Management

The course discusses five major activities.

1. Team Formation
2. Project Estimation
3. Project Scheduling
4. Risk Management
5. Agile Project Management

---

# 4. Project Estimation

## Definition

Project Estimation predicts

* Cost
* Time
* Effort
* Resources

required to complete a project.

---

## Why is Estimation Important?

It helps to

* Estimate project cost
* Estimate completion date
* Decide team size
* Bid for software contracts
* Monitor project progress

More information about the project leads to more accurate estimates. 

---

# 5. Estimation Parameters

## A. Size of Code

Measured using

* LOC (Lines of Code)
* KLOC (1000 Lines of Code)

Example

1 KLOC = 1000 lines

---

## B. Effort

Measured in

**Person-Month (PM)**

Definition

Amount of work one person performs in one month.

Example

Project = 12 Person-Months

Possible staffing

* 12 people → 1 month
* 4 people → 3 months
* 2 people → 6 months

(assuming ideal parallel work)



---

# 6. Estimation Techniques

The course mainly discusses

---

## Expert Judgment

Experienced developers estimate effort based on previous projects.

Advantages

* Fast
* Practical

Disadvantages

* Subjective
* Depends on experience

---

## Analogy-Based Estimation

Estimate by comparing with similar completed projects.

Example

If Project A required

20 person-months,

a similar project may need approximately the same effort.

---

## Decomposition (Bottom-Up)

Break project into smaller tasks.

Estimate each task.

Total estimate

= Sum of individual estimates.

---

# 7. Project Scheduling

## Definition

Scheduling determines

* What tasks are done
* Who performs them
* When they start
* When they finish

---

## Why Scheduling?

Scheduling helps

* Monitor progress
* Detect delays
* Take corrective action
* Coordinate team members



---

# 8. Steps in Project Scheduling

Remember this sequence.

1. Identify activities
2. Break activities into tasks
3. Determine dependencies
4. Estimate task duration
5. Represent schedule
6. Determine start/end dates
7. Find critical path
8. Allocate resources



---

# 9. Task Dependency

Some tasks cannot begin until another task finishes.

Example

Requirement Analysis

↓

Design

↓

Coding

↓

Testing

Testing cannot begin before coding.

---

# 10. Critical Path

## Definition

The **Critical Path** is the longest sequence of dependent tasks that determines the total project duration.

Important point

Delay in any critical-path task

↓

delays the entire project.

---

# 11. Risk Management

## Definition

A Risk is

> An anticipated unfavorable event that may occur during a project.

Risks are identified before they happen so they can be mitigated. 

---

# 12. Why Software Projects Have Risks

Software is

* Invisible
* Complex
* Constantly changing

Examples

* Syntax errors
* Third-party library failures
* Technology changes
* Team conflicts



---

# 13. Types of Risks

## A. Technical Risk

Occurs due to technical problems.

Examples

* Wrong implementation
* Poor architecture
* Incomplete requirements
* Integration failures



---

## B. Schedule Risk

Project finishes late.

Reasons

* Poor estimation
* Resource shortage
* Unexpected issues

---

## C. Cost Risk

Project exceeds budget.

---

## D. People Risk

Examples

* Developer leaves
* Team conflict
* Lack of skills

---

## E. Requirement Risk

Customer changes requirements frequently.

---

# 14. Risk Management Process

Remember

Identify

↓

Analyze

↓

Prioritize

↓

Mitigate

↓

Monitor

---

# 15. Agile Project Management

Traditional approach

* Heavy planning
* Predict cost early
* Large documentation

Agile approach

* Short iterations
* Frequent customer feedback
* Flexible planning
* Working software first

Agile does not attempt to predict the entire cost and schedule at the start of the project. Instead, planning evolves through frequent iterations with customer collaboration. 

---

# 16. Agile Lifecycle

Typical iteration

1–2 weeks

Each iteration

* Implements selected user stories
* Produces working software
* Gets customer feedback
* Updates priorities



---

# 17. Scrum

Scrum is the Agile framework emphasized in the course.

---

## Sprint

A Sprint is

A short, time-boxed development cycle.

Usually

1–2 weeks.

Goal

Deliver working software.

---

## Scrum Team Size

Typically

4–9 people.



---

# 18. Scrum Roles

## A. Development Team

Builds the product.

Includes

* Developers
* Testers
* Designers

---

## B. Product Owner

Represents customer.

Responsibilities

* Prioritize requirements
* Maintain product backlog
* Maximize customer value

---

## C. Scrum Master

Ensures Scrum practices are followed.

Responsibilities

* Remove obstacles
* Facilitate meetings
* Support the team



---

# 19. Sprint Planning

Before each sprint,

the team conducts a Sprint Planning Meeting.

Two questions are answered:

1. What work will be completed?
2. How will it be completed?



---

# 20. Product Backlog

## Definition

A prioritized list of all work required for the product.

Derived from

* Requirements
* User stories

Highest-priority items appear at the top.



---

# 21. Pivotal Tracker

Pivotal Tracker is a project management tool that supports Agile development.

It helps teams

* Track user stories
* Monitor velocity
* Manage iterations
* Maintain backlog



---

# 22. Important Pivotal Tracker Terms

## Current Iteration

Stories currently under development.

---

## Backlog

Prioritized work waiting to be completed.

---

## Icebox

Ideas and user stories not yet prioritized.

---

## Story

One user requirement.

---

## Epic

Collection of related user stories.

---

## Story Points

Estimate of effort.

Higher points

↓

Greater complexity.

 

---

# 23. Story Attributes

Each story may include

* Title
* Description
* Priority
* Story Points
* Labels
* Tasks
* Comments
* Owner



---

# Comparison Tables

## Traditional vs Agile

| Traditional               | Agile               |
| ------------------------- | ------------------- |
| Predict everything early  | Adapt continuously  |
| Heavy documentation       | Working software    |
| Large releases            | Small iterations    |
| Fixed plan                | Flexible plan       |
| Customer at beginning/end | Customer throughout |

---

## Product Owner vs Scrum Master

| Product Owner         | Scrum Master           |
| --------------------- | ---------------------- |
| Represents customer   | Supports Scrum process |
| Prioritizes backlog   | Facilitates team       |
| Decides product value | Removes obstacles      |
| What to build         | How to work            |

---

## Backlog vs Sprint

| Product Backlog      | Sprint              |
| -------------------- | ------------------- |
| Entire project work  | Small iteration     |
| Prioritized list     | Selected tasks      |
| Continuously updated | Fixed during sprint |

---

# Important Definitions

### Project Management

Planning and controlling software development.

---

### Project Manager

Person responsible for overall project success.

---

### Estimation

Prediction of effort, cost and schedule.

---

### Person-Month

Work done by one person in one month.

---

### Scheduling

Planning tasks over time.

---

### Critical Path

Longest chain of dependent tasks.

---

### Risk

Expected unfavorable event.

---

### Scrum

Agile framework for iterative development.

---

### Sprint

Short development iteration.

---

### Product Backlog

Prioritized list of all project work.

---

### Epic

Group of related user stories.

---

### Story Points

Relative estimate of effort.

---

# Likely Exam Questions

## Short Answer

1. Define Software Project Management.
2. List responsibilities of a Project Manager.
3. What is Project Estimation?
4. What is Person-Month?
5. Define KLOC.
6. What is Project Scheduling?
7. Define Critical Path.
8. What is Risk?
9. What is Scrum?
10. Define Sprint.
11. What is a Product Backlog?
12. What is an Epic?
13. What are Story Points?

---

## Long Answer

1. Explain the responsibilities of a Project Manager.
2. Explain project estimation techniques.
3. Explain project scheduling steps.
4. Explain software risk management.
5. Explain Agile project management.
6. Explain Scrum roles and activities.
7. Explain Pivotal Tracker and its features.

---

# One-Page Revision Sheet

* Project Manager = Plans, organizes, estimates, schedules, manages risks, communicates.
* Estimation predicts cost, effort, schedule, and resources.
* Size = LOC or KLOC.
* Effort = Person-Month.
* Scheduling steps: Identify → Break Down → Dependencies → Estimate → Schedule → Critical Path → Allocate Resources.
* Critical Path = Longest dependent path; delays here delay the project.
* Risk = Anticipated unfavorable event.
* Agile = Iterative development with customer feedback.
* Scrum = Agile framework.
* Sprint = 1–2 week iteration.
* Scrum Roles = Product Owner, Scrum Master, Development Team.
* Product Backlog = Prioritized work list.
* Pivotal Tracker manages stories, backlogs, iterations, epics, and story points.

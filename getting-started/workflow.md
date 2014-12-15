
# DevTeam Workflow

At Mindspace, we use [Github Flow](https://guides.github.com/introduction/flow/index.html) exclusively. Please read that document before continuing on with this outline of our workflow.

## Tasks

**tl;dr:**

* `individual tasks` are created for developers
* `master tasks` are created for project management
* read the thing about [task labels](#task-labels) and Huboard

At Mindspace, we create two types of tasks in Github. Development leads and a producer create `individual tasks` for all the features in a project. These individual tasks are then assigned to developers each Friday during the [weekly review](#weekly-review). Once the development leads create and prioritize all of the individual tasks, we create a `master task` for each major feature in the project.

You can think of these as matching user stories in an agile development approach. The master tasks contain checkbox lists which reference each individual task related to the feature. This makes it easy for us to track progress on features while also having smaller, easy-to-tackle individual tasks for everyone on the team. 

Here are our guidelines to good task creation:

* The task can be done in one day
* The task is clear and well documented
* The task references the *master task* so that the developer can reference the bigger picture


#### Task Labels

For better project management, we use [Huboard](http://huboard.com/) so that we can have a dashboard (BINGO!) view of tasks. Huboard adds labels to Github to set task status. These labels are:

1. `Backlog` - this label should apply to tasks that are not ready to be completed yet
1. `Ready` - this label should apply to tasks that are ready for development
1. `Working` - when a developer is ready to work on a new task, she should change it from "Ready" to "Working"
1. `Done` - when a developer is done with a task, she should change the task from "Working" to "Done" and submit a pull request for that task


## Milestones

Milestones should be created for each project. We schedule milestones by the week, from the start-date of development to the week of final deployment. Milestones will be created by Jay, Dirk, or Rebecca. 

#### Weekly Review

Each Friday, Jay, Dirk, and Rebecca check each project's progress by reviewing the week's milestone. If there are unfinished tasks, they will move to the following week's milestone, or re-prioritized. This means, milestones evolve each week depending on what gets finished. The goal here is that Monday - Thursday can be focused development while Friday becomes a day of review and adjustment for the following week.

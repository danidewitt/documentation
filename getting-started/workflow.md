
# DevTeam Workflow

At Mindspace, we use [Github Flow](https://guides.github.com/introduction/flow/index.html) exclusively. Please read that document before continuing on with this outline of our workflow.

* [Explaining Tasks and Milestones](#explaining-tasks-and-milestones)
    * [Tasks](#tasks)
        * [Task Labels](#task-labels)
    * [Milestones](#milestones)
    * [Weekly Review](#weekly-review)
* [An Example Workflow](#an-example-workflow)

## Explaining Tasks and Milestones

**tl;dr:**

* `individual tasks` are created for developers
* `master tasks` are created for project management
* read the thing about [task labels](#task-labels) and Huboard
* we use Github flow, understand it, and never commit code directly to master

### Tasks

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

### Milestones

Milestones should be created for each project. We schedule milestones by the week, from the start-date of development to the week of final deployment. Milestones will be created by Jay, Dirk, or Rebecca. 

### Weekly Review

Each Friday, Jay, Dirk, and Rebecca check each project's progress by reviewing the week's milestone. If there are unfinished tasks, they will move to the following week's milestone, or re-prioritized. This means, milestones evolve each week depending on what gets finished. The goal here is that Monday - Thursday can be focused development while Friday becomes a day of review and adjustment for the following week.

---

## An Example Workflow...

Let's walk through working on a task that is assigned to a developer. We'll use Jay as an example.

![An image of task #143](http://mindspacepdx.s3.amazonaws.com/github-images/example-ticket.png)

Jay can look at tasks assigned to him that are "Ready" by using Github's filtering in the issues list.

He then starts work on issue #143 by changing the ticket label from "Ready" to "Working" so that the project managers can see what he's working on. After that, he creates a new branch from an up-to-date master for the new issue like so: 

```bash
# switch to master
git checkout master

# fetch the latest from Github
git fetch

# update master on your local machine
git pull origin master

# create a new branch from the updated master
git checkout -b jc-learningplan-view
```

After completing work on the issue, Jay then commits and pushes that branch to Github:

```bash
# Commit the changes to git
git commit -am "Added learning plan view"

# Push the changes to Github
git push origin jc-learningplan-view
```

Once the branch is pushed to Github, Jay does two things. He creates a Pull Request to merge his new branch into master, and then updates the task label from "Working" to "Done".

When creating a new pull request, we ask that the following be added to the PR comment,

* A bulleted list of what you've done
* How to test it
* If it closes an issue, finish the comment with "resolves #<ticket_number>"

So using the above example, Jay would write something like this in his PR:

```markdown
* adds learning plan react component
* adds a new route for the learning plan zone
* test by selecting Barista Basics zone and seeing learning plan
* Resolves #143
```

Once Jay has made this PR, he will post it for someone to check, usually in Slack.

> Hey @channel? Can someone look at this? https://....

Someone will volunteer and take a look at the PR and give it a :thumbsup: or :thumbsdown: with a reason. If you get the :thumbsup: then you can hit the "merge" button for your PR to get into master. 

![Pull request example](http://mindspacepdx.s3.amazonaws.com/github-images/pull-request-example.png)

Hitting "merge" will automatically close the issue #143 when the PR is merged into master. Then Github will let you delete the branch. You **do** want to do this =)

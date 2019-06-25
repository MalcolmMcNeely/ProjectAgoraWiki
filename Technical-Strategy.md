#Branching and branch naming convention
Let's borrow something from [Trunk Based Development](https://trunkbaseddevelopment.com/) and have the following branch hierarchy:

- Master (for deployment, may look to automatically deploy from this branch)
- Develop
    - Task3/create-react-app
    - Task4/basic-get-fetch-function
    - Bug5/react-app-doesnt-support-something
    - Task6/integrate-react-and-function


The idea is to avoid merge hell from large epics, even though the benefit is diminished somewhat in a smaller team, it's a practice that I'm eager to explore. We can still organise our work in terms of epics, stories, and tasks in DevOps since it is useful to do so but our branches should be tasks only.

#Unit Testing
Should be included in their respective tasks.

#Repos
We'll be using GitHub for transparency. Don't use the Azure Repo.. I created it by accident and it doesn't seem like you can delete it.

#Picking up work
The backlog will (or should) be populated and we'll pick up work items as and when we want. If a epic/story lacks stories/tasks then we can add/edit/remove as we see fit.

# Pull Request Workflow
As a Project Manager, you'll complete Pull Request Reviews every single day. Making this process a little bit easier/faster/more streamlined will save you a lot of time in the long run, so learning the git commands can help everyone out a ton!

## Grabbing the Pull Request and viewing it locally

For this to work, you have to be using a clone of the base assignment repo from Lambda School, NOT a personal fork of it. This gives you access to the pull requests on the assignment and it prevents you from having to clone a million repositories and spam your GitHub profile.

1. Find the ID of the pull request. It's visible in the URL and on the actual GitHub website. In this short tutorial, we'll use one of my student's projects as an example.

	  You can find the ID using either of the two methods below:

	  In the URL to the PR:
  https://github.com/LambdaSchool/Bootstrap-Project-I/pull/109


	  Or by looking at the title of the PR on the actual GitHub website:

  ![image](https://i.imgur.com/Di5Tgfu.png)

In this case, the ID is **109**. We'll need that for the next step.

2. CD into the directory that you'd like to clone the student's PR into and type: `git fetch origin pull/109/head:julian`

* 109 is the ID of the Pull Request. That'll change in your case.

* `head:julian` tells git to make a new branch called `julian` to store his Pull Request. You can use any name instead of `julian`.


3. `git checkout julian` to move to the new branch and check out the students code. Everything should automagically switch inside of your editor and you'll immediately be able to see the students code and be able to run any sort of tests that you need to complete. For example, if I already had the index.html open before I checked out Julian's branch, I could just refresh the page in my browser and it will automatically update to Julian's project.

## Lost? Check your local branches

`git branch -a`: If you lose track of what branches you already have on your machine for each repo, this will fetch all of the available branches. (both local AND remote)

## Running out of space?

`git branch -D julian`: After you're done running each test, you're free to delete the branch.

Again, julian is just the example name from above. Enter the name of your branch in its place. Also, note that -D is an alias for `--delete --force` flags, so it will completely delete that branch from your machine irrespective of its merged status (and it WONT prompt you to check if you're sure, so make sure you're done with the branch before you do this!)

## Troubleshooting

`fatal: Couldn't find remote ref pull/{ID}/head`

Make sure you're working from the cloned base repo of the assignment and **NOT** from a personal fork of the repo

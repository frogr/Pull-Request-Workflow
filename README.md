# Pull Request Workflow
As a Project Manager, you'll complete Pull Requests every single day. Making the process a little bit easier/faster/more streamlined will save you a lot of time in the long run, so learning the git commands can help everyone out a ton!

## Grabbing the Pull Request and viewing it locally

First, you need to find the ID of the pull request. It's visible in the URL and on the actual GitHub website. In this short tutorial, we'll use one of my student's projects as an example.

You can find the ID using either of the two methods below:

In the URL to the PR:
https://github.com/LambdaSchool/Bootstrap-Project-I/pull/109


On the actual GitHub website:

![image](https://i.imgur.com/Di5Tgfu.png)

In this case, the ID is 109. We'll need that for the next step.

Next, CD into the directory that you'd like to clone the student's PR into and type: `git fetch origin pull/109/head:julian`

Things worth noting about the above command:

* 109 is the ID of the Pull Request. That'll change in your case.

* head:julian tells git to make a new branch called `julian` to store his Pull Request. You can use any name instead of `julian`, that's just what I use because it's simple for me.


Finally, run `git checkout julian` and check out the students code. Everything should automagically switch inside of your editor and you'll immediately be able to see the students code and be able to run any sort of tests that you need to complete. For example, if I already had the index.html open before I checked out Julian's branch, I could just refresh the page in my browser and it will automatically update to Julian's project.

## Lost? Check your local branches

If you lose track of what branches you already have on your machine for each repo, you can type: `git branch -a`

This will fetch all the branches available (both local AND remote)

## Running out of space? Delete the branches when you're done

After you're done running each test, you're free to delete the branch and get it off your local machine. Do so by typing: `git branch -D julian`

Again, julian is just the example name from above. Enter the name of your branch in its place. Also, note that -D is an alias for `--delete --force` flags, so it will completely delete that branch from your machine irrespective of its merged status.

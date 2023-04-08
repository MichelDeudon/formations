---
title: Github crash course for data scientists
date: 2022-01-24
---

From zero to hero, all you need to know

<!--more-->

I always had an imposter syndrome working with Github, until recently. I remember the first time I opened a terminal, it felt like I was about to hack the world 🐱‍💻 With time and practice, I eventually grasped the key concepts behind Github. Now I feel more comfortable working with engineers and developers or mentoring peers, and that’s fun. I wrote this crash course at the time I applied to Vinted for a Data Science position and decided to share it because it might be what you’re looking for 😊. Great, so what’s Github?

{{< figure src="blog-git-1.jpg" caption="git/Photo by Tatiana Syrikova from Pexels" numbered="true" >}}

Git is an open source, distributed version-control system and Github is a platform for hosting and collaborating on Git repositories. <b>Github helps people collaborate across the world</b> - learn, share, contribute and build together by synchronising work on different machines to solve various kind of problems related to artificial intelligence, machine learning or apps. In other words, Github is like a distributed sandbox and it’s free to play!

Whether you work or you’re applying for a job as an analyst, a data or decision scientist, a developer, an engineer, a consultant or a manager and you need a refresher on Github or you heard about it and need to use it to collaborate, this <b>practical guide to master Github in 7 steps</b> is probably for you. I will only assume you have Git installed and a Github account, otherwise check [how to install Git for your Operating System](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (Mac, Windows, Linux/Ubuntu) and [sign up for a Github account](https://github.com/) 🚀

Before diving into practical use cases and Git commands, here’s a bit of <b>terminology</b> to get familiar with the concepts:

> `Repository`: A folder with files we want to keep track of <br>
> `Remote`: A common repository that all team members use to exchange their changes <br>
> `Origin`: Your local repository <br>
> `Index`: An area where Git holds files that have been changed, added or removed <br>
> `Commit`: An entry into Git’s history, representing a change made to a set of files at a given point in time, a compressed snapshot of your entire repository <br>
> `Branch`: A version of a repository, a lightweight movable pointer to a commit, which represents the status of the repository <br>
> `HEAD`: The most recent commit on a branch. It represents your current working directory and can be moved to different branches, tags or commits when using git checkout

## Use cases and practical Git commands

### 1. Get started

The first step when you start working with Git is to configure your user information (name and email). You can do so for all local repositories by typing the commands below in a terminal

```sh
git config — global user.name "your_name"
git config — global user.email "your_email"
```

Easy, right? You can further display help information about Git using

```sh
git help
```

### 2. Start a working area

Now that your local repositories are configured, you can create a repository on Github and clone (download) it locally with

```sh
git clone "url"
```

The <b>.gitignore</b> file is helpful to exclude files from being tracked with Git such as credentials, tokens or data. You can find templates at [github.com/github/gitignore](https://github.com/github/gitignore).

### 3. Examine the history and state

From your cloned repository, you can list the version history for the current branch with

```sh
git log
```

To further inspect and compare the evolution of project files, use

```sh
git diff
```

This will show changes from the previous commit (what was added, removed or modified). You can further specify branches or commits to change the default result.

{{< figure src="blog-git-2.jpg" caption="git/Photo by James Wheeler from Pexels" numbered="true" >}}

### 4. Make changes and commit

At this point, you can inspect the version history. Now it’s time to contribute to the project! Add, remove or edit a file in your repository, for example, a Python script <i>hello-world.py</i>.

The changes you’ve made to your local repository and which files are tracked/untracked on your branch can be accessed with

```sh
git status
```

To add content to the index and snapshot the files you worked on for versioning, simply use

```sh
git add [file1][file2][file3]
```

Or to add all files and changes directly (beware though), use

```sh
git add .
```

The last step to record the changes in your version history is done with

```sh
git commit -m "descriptive message"
```

Your message should carry specific information, [what the changes do, not what you did for the change](https://vinted.engineering/2015/01/02/proper-git/) (e.g., <i>“fixed bug”</i> 🙈). Ask yourself, will other people or yourself in 6 months understand what it is about without looking at the code? Consider splitting a large commit into multiple commits if it makes it easier to understand and don’t forget Github is a tool for collaboration and should be used as such.

### 5. Swing with branches

Let’s assume you have a first prototype and want to develop features in parallel. That’s where branches kick in. Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently <i>“checked out”</i> to and you can see the different branches using

```sh
git branch -l
```

You can create a new branch locally, for example called <i>“feature/x”</i>, using

```sh
git branch feature/x
```

And you can delete this same branch by adding the flag `-d` after `git branch`

Now you can switch to a specific branch or commit (this will update your local working directory) with the first or second command line below

```sh
git checkout feature/x
git checkout commit_id
```

{{< figure src="blog-git-3.jpg" caption="git/Photo by Leah Kelley from Pexels" numbered="true" >}}

Each branch tends to diverge naturally with different features. You can join their development history back together by “merging” branches, i.e., incorporating changes from one branch to another. By default,

```sh
git merge
```

combines the remote tracking branches into the current local branch and

```sh
git merge origin [branch]
```

combines the specified branch’s history into the current branch. This is usually done in pull requests (more on this in the next section).

Finally, a few words on `git rebase`. Rebase applies the commits of a branch on top of another branch’s HEAD (it’s also known as fast forwarding). It should be used carefully because it modifies the commits themselves and therefore can become a mess if done on a branch with many collaborators. I personally find it helpful to clean the version history of a branch or integrate changes done on the master branch (`-i` stands for interactive mode)

```sh
git rebase -i master
```

### 6. Synchronize changes

At this point, you did some changes in your local repository and modified the version history of your local branch <i>“feature/x”</i>. In the meantime, your friend and colleague also modified the version history of the same remote branch. What to do now?

The first step is to download all history from the remote tracking branches. You can do so with

```sh
git fetch
```

Then, you actually need to merge these remote tracking branches in your local branches. You can simply use

```sh
git pull origin feature/x
```

as a combination of `git fetch` and `git merge` to get changes from the remote repository. If you’re lucky, everything worked well. Otherwise, if `git merge` returns <i>“Automatic merge failed; fix conflicts and then commit the result”</i>, it means your friend and you both modified the same code and conflicts need to be resolved manually. In such case, `git status` will help you find which files are modified on both branches and git diff will show where the conflicts are. These are marked and delimited in the code with `>>>>`, `====`, `<<<<` which makes it easy to detect and modify with a text editor, until all conflicts are resolved. When you’re done, your local working branch is up to date with all new commits from the corresponding remote branch on GitHub.

Finally, you can send your commit to the remote repository and grab a snack. Congrats!

```sh
git push origin feature/x
```

Note: In some situations, e.g., all changes were done on master but were meant to be done on branch <i>“feature/x”</i>, it’s convenient to <i>“stash”</i> the changes in a dirty working directory before adding them to the version history. You can do so and apply the modification on the right branch using

```sh
git stash
git checkout feature/x
git stash apply
```

### 7. Tag your commits

Git is a version-control system and helps keep track of different versions. You might want to tag some of these with a human readable name such as “alpha”, “beta”, “v0.0.1” or “v0.0.2”. The syntax is given below. Although this step is entirely optional, it's a nice way to celebrate milestones and victories 🎉

```sh
git tag [label] [commit]
```

## Final words

You’re done with this crash course, well done! You’re ready to collaborate with people across the globe. Don’t forget it takes time and practice to master a tool like Github and if you want to go further, check the reference below or just ask around you for some help.

{{< figure src="blog-git-4.png" caption="git/Visual Git Cheatsheet by Andrew Perterson" numbered="true" >}}

[1] [Git Documentation](https://git-scm.com/doc) <br>
[2] [GitHub Git Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/) <br>
[3] [Visual Git Cheatsheet](https://ndpsoftware.com/git-cheatsheet.html) <br>
[4] [Vinted Proper Git](https://vinted.engineering/2015/01/02/proper-git/)

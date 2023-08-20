# Git And Github

- [Git And Github](#git-and-github)
  - [Getting Started](#getting-started)
    - [What Is Version Control?](#what-is-version-control)
    - [Why Is Git So Important?](#why-is-git-so-important)
    - [Basic Terminal-Based Text Editors](#basic-terminal-based-text-editors)
  - [Configure Git Locally](#configure-git-locally)
    - [Git Config](#git-config)
    - [Creating A New Project With Git](#creating-a-new-project-with-git)
    - [Git Commit](#git-commit)
    - [Git Logs](#git-logs)
    - [Undo a Commit](#undo-a-commit)
  - [Branches](#branches)
    - [What Is a Branch?](#what-is-a-branch)
    - [Creating a Branch](#creating-a-branch)
    - [Switching Between Branches](#switching-between-branches)
    - [Renaming Branches](#renaming-branches)
    - [Deleting A Branch](#deleting-a-branch)
    - [Git Stash](#git-stash)
  - [Merging Branches](#merging-branches)
    - 
## Getting Started

### What Is Version Control?
<hr>

This lesson dives into version control and explains why it is useful for large projects.

- Why do we need version control? :

Let’s say you create a project and have worked on it for over a month. While adding a new feature, you realize that something you did a week back won’t allow your new feature to work properly. You decide to revert those changes but aren’t sure if you have made similar changes in other files as well.

What if there was a way for you to identify what exact changes you made and where in your code you made them? That’s where version control can help you out.

- Keep track of changes to the codebase :

In the simplest of terms, you can consider version control to be a record of all the changes that your software code goes through. Version control systems allow you to keep track of how your project changes over time, with additional information about why and when each change was incorporated.

- Ease in collaborative work :

Version control systems can solve many problems that you, as a developer, will face. They keep track of how your source code changes, who is changing it, and when. It also allows you to revert those changes as you deem fit.

Because of all these advantages, version control makes collaborative work easier.

If you opt not to use version control for your project, sooner or later you will find yourself copying your project directory into multiple different versions. You might name them according to whichever priority you want to assign, such as ‘final_version,’ ‘latest_version,’ or something along those lines. However, it is not a sustainable approach, especially when working collaboratively with a team. Version control systems essentially formalize this process, so you don’t have to manually do it yourself.

- Version control tools :

Version control tools have been continuously updated over time, following the ever-changing workflows that developers choose to use. In more recent times, Git has become the tool of choice for version control.

In the next lesson, we will look into what Git is and what makes it such a widely used software for version control.


### Why Is Git So Important?
<hr>

In this lesson, you will learn about Git and why it's so widely used.

- What is Git?

Git is a distributed version control software. As a result, a complete copy of the entire codebase will be available on every contributor’s computer; we can also call this codebase a local repository.

Git tracks the local repository, maintains a record of all the changes that occur within it. It removes the hassle of keeping multiple versions of the project in separate directories and also makes sharing changes to the source code between collaborators seamless and quick.

The distributed nature of Git makes it unique and efficient. Since every contributor or collaborator has their own ‘clone’ of the source code in their local repository, it allows Git to track, add, or revert changes very quickly. Git uses the local database to keep a record of the changes to the project files.

- Git snapshots :

A Git snapshot is, essentially, the state of the project files at a certain point in time. In other words, instead of maintaining a record of file-based changes that occur over time, Git will store that data as a snapshot, which is the entire state of the project at that particular moment. While saving the snapshot, it will keep those files that did get updated and only keep references of files that didn’t change from the previous snapshot to avoid duplicates.

- Git states :

Git has three primary states that it allows the project’s files to acquire. The three states are:

`Modified` - files that have been changed, but the changes have not yet been marked by Git. These changes won’t become part of the next snapshot.

`Staged` - the changes have been tracked by Git and will be marked as such in the next snapshot.

`Committed` - the changed files that have successfully become part of the latest snapshot.

Before we move on to learn more about Git, let’s briefly go over how you can use the terminal to edit text files using text editors and terminal commands.


### Basic Terminal-Based Text Editors
<hr>

A basic summary of how you can edit files or make changes using terminal commands or terminal-based text editors.

The goal of this course is to cover the necessary Git commands and concepts. To do that, we will have to alter the content of some files as we go along. We have a variety of options to opt for in this regard. Since you will be able to test out all the commands within the lessons, it’s going to be beneficial if you have an idea about how you can modify plain text files using the terminal itself.

Normally, we use fancy text editors and notepad applications, but, for this course, we will opt to use plain terminal-based commands and terminal-based text editors to make changes and updates.

- Using the `echo` command :

We can add text to a file using the echo command which is shown below:
```
echo "Hello world!" >> file1.txt
```

> Note: The `echo` command can’t be used to add text in arbitrary points in the file. It will, instead, append the text at the end of the text file.

Try out the command in the terminal provided below. The terminals in this lesson already have a file called `file1.txt`, which is present in the working directory `test_project`. You can verify this by using the command `ls`.

> To view the contents of the file itself, use the command `cat file1.txt`, or you can opt to use one of the terminal-based text editors, such as `nano`, which is discussed later in this lesson.

This is a very simple and straightforward way to add text to a file.

- Using `nano` :

`nano` is a very simple terminal-based text editor that comes installed as a default with Linux. Click anywhere on the terminal widget below, and then execute the following command.
```
nano file1.txt
```
From this point forward, you will simply enter any text you plan to add to the file. By using the commands provided at the end of the terminal window, you can save those changes and exit the editor.

Note the `^` key. It represents the `ctrl` key on your keyboard.

In order to get help on the commands, press `ctrl + g` (hold down the control key while hitting `g`).
If you want to exit nano, press `ctrl + x`. If there are unsaved changes, nano will prompt you to save those changes before exiting.

> Note: The ^ is the control key on the MAC keyboard and Ctrl key on Windows.

The image shown below is of the user interface you will encounter when you use the `nano` command.
```
nano <file_name>
```
That is more or less the gist of the very basics you will need to know about terminal-based text editors for this course. Alternatively, if you are comfortable with using any other text editor such as Vim, feel free to use that as well.

In the next sections, we will continue our discussion about Git and how to configure it locally.


## Configure Git Locally

### Git Config
<hr>

Learn how to set up Git for your local machine by familiarizing yourself with the Git config command.

- Installing Git :

The Git software is a powerful command-line tool that you can install on your machine, whether you use Windows, macOS, or Linux. There is a command-line terminal available below for you to try out various Git commands as well.

You can learn how to install Git for whichever operating system you use through this [link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

From this point forward, we will rely on the command-line terminal, so your familiarity with the terminal will help you a lot.

Once you have Git installed on your machine, you will be able to use all the Git commands locally.

To verify that Git is installed successfully in the system, try typing in the following command in the terminal provided at the end of this lesson:
```
git --version
```
If Git is properly installed, the command above should display the installed version of Git that you are going to use.

> Note: You will be provided with terminals in the entire course, which will have Git installed already, so you won’t need to install it on the platform.

- The `git config` command :

The `git config` command works for a large variety of cases. Moreover, the config command works on different levels. Our main goal is to set our credentials that will identify our contributions and changes in the project source code. Doing so will help us identify and differentiate between the changes made by various contributors.

- The config command works on different levels :

We can set our credentials to be limited to a particular project, i.e., locally, or we can set them up globally. Finally, we can also use the config command to work on a system level.

Setting configurations at a local level will only affect the working project directory. Using the global configuration will result in the same configurations to apply to all our repositories that the currently logged in user for that machine makes, except for the projects where the user has assigned a different local configuration. Configurations that are set up on a system level will, by default apply to all the users on that particular computer.

- Setting our email and username for Git :

We will set up our name and email globally for Git by using the following commands:
```
git config --global user.email "educative_learner@example.com"
```
Similarly, we will also set up our username too:
```
git config --global user.name "Educative Learner"
```
You can verify your configurations for setting up the email and username by typing in the commands:
```
git config user.email
git config user.name
```
If they work fine, you should be able to see your desired email and username printed on the terminal.

Now that you have set up your information using the `git config` command at a global level, let’s proceed forward with creating a new project and initializing Git to track it.

- Configure Git with a name and email of your choice :

In the terminal below, and in every terminal you will be provided in the course, you are given two configurable environment variables for inserting an email and name of your preference. Click on the edit button present below, and change the default email and name to what you would prefer.

This change will be reflected in all the proceeding terminals in the course. You can also configure Git using the commands above, but those changes will be restricted to that specific terminal. If you’d like to continue forward with a name and email of your own preference on the platform, you will need to use the environment variables, since they are configured globally, and their values will remain persistent throughout the course.

> Note: The environment variables are used here to make sure the course is more interactive for you as a learner with the terminals provided. You do not need to rely on environment variables to configure Git otherwise and can proceed forward with the course using the default configurations.


### Creating A New Project With Git
<hr>

In this lesson, you will create a new project and learn how to use Git to track it.

- Creating a new project directory :

Let’s start by creating a new working directory or folder in the terminal. We’ll call the new working directory `test_project`. You can create a new directory by using the following command:
```
mkdir test_project
```
Once we have created the new directory, we will need to set that as the current working directory. We will do that by entering the following command:
```
cd test_project
```
Once the `test_project` directory becomes the working directory, which will be initially empty, we will create a plain `text file`. Let’s call it `file1.txt`. We will create the new file using this command:
```
touch file1.txt
```
To verify that the file was created, enter the plain command ls in the terminal window below. It should print all the folders and files present within the working directory, which, in our case, is `file1.txt`.

- The `git init` command :

Now that we have a working project directory with a file in it, we can initialize Git to track this project and its contents:
```
-test_project/
--file1.txt
```
Enter this command in the terminal provided above:
```
git init
```
The `git init` command simply creates an empty repository. Therefore, your project will not automatically come under the ambit of version control with this command alone. What `git init` does, however, is create a `.git` directory. The `.git`; directory will contain all the metadata that Git will require for tracking the project.

The subdirectory `.git` will contain several files and more subdirectories that Git will use to keep track of changes in the project.

- The `git add` command :

Now that we have a project that has a file and an empty Git repository set up, we want Git to track the contents of the entire project.

At this point, the `git add` command will help us. Enter the following command in the `test_project` directory:
```
git add .
```
This will result in all of the contents within the test_project directory to be tracked by Git. Congratulations! Now you have a Git repository that is actively tracking the test_project directory.

- The `git status` command :

To verify what state your files in the repository are in, you can use the `git status` command. It doesn’t change or update anything. Instead, it prints out which files are modified, staged, or untracked.
```
git status
```
Let’s see what has happened to our new repository once we try this command, once before using the `git add` . command and once after we have entered it.

Look at the kind of information you get with `git status`. You can identify when `file1.txt` is untracked by Git and how it then changes to a staged state. As you get more familiar with Git and use it more often, you will find yourself checking the status of your files quite often.


### Git Commit
<hr>

Learn how to create your first snapshot with the git commit command.

The `git commit` command
Once we have a local repository that is tracking our project, we will move towards creating our very first commit.

A commit is a snapshot of the entire state that your project is in at that moment. Git keeps track of your project through a series, or chain, of commits. The most recent snapshot of your repository is referred to as the HEAD.

As soon as you create a new commit, it will directly link to the HEAD. However, since the latest commit is now the most recent one, it will be considered the HEAD instead, replacing the previous one.

- The commit message :

The structure of the commit command is very straight forward:
```
git commit -m "What changes occurred within the commit."
```
From the snippet above, you will notice the -m flag, followed by a string. The string is called the commit message. Usually, the commit message is a phrase that describes what changes or modifications occurred within the commit.

- Our first commit :

Let’s move on to creating our first commit. Since it is the first one, let’s have the commit message be “initial commit.”

Enter the following command in the terminal below and see what happens. Please note that before we create a commit, it is a wise decision to use the `git status` command to check which changes will be reflected in that commit.
```
git commit -m "initial commit"
```
The commit message can be anything you want it to be, so there is no restriction on keeping it as “initial commit.” This decision is up to you. The primary purpose of the commit message is to make sure it is sufficiently descriptive, and it gives an idea of what the snapshot contains.

> Note: It is tempting to use meaningless short messages like “Commit 1,” “Commit 2,” etc. However, it is highly recommended NOT to do that. Descriptive commit messages can save a lot of time.

Once you have successfully created your first commit, try entering git status again and check what has changed. All the staged files become part of your initial commit, and there are no other changes to commit anymore.

You have officially made your first commit!


### Git Logs
<hr>

Let’s take a deeper look at the commit structure and see how we can view our commit history using the Git log command.

- The `git log` command :

Git tracks changes to a project by maintaining a chain of snapshots or commits. If you are working on a collaborative project, you will find that your repository will have commits from different contributors. The `git log` command lets you view the commit history for your project.

Entering the `git log` command in your terminal will allow you to view a list of commits or snapshots that will be sorted based on the time they were created with the latest one at the very top.

Each log will contain information about the author of the commit, displaying their username and email that we set with the git config command (discussed in one of the previous lessons).

The log will also contain a timestamp of when each commit was created along with the commit message.

One more critical piece of information that the log will show is the 40-characters-long unique hash. The hash is vital because it helps identify commits and acts as an excellent way to secure the commit.

The commit hash uses the cryptographic hash function SHA-1. The hash key allows each commit to have integrity. If the hash were to change, we would be able to identify that the commit has been tampered with.


### Undo a Commit
<hr>

Let’s learn how to undo or revert a commit in this lesson.

There are many instances where you will realize that the commit you just created had some things that weren’t supposed to make it into the snapshot. There are several ways to go about correcting these mistakes.

One way would be to create a new commit that fixes the issue you added in the previous one. Another option would be to undo or revert the last commit or at least update it. Let’s look at some options we can try out.

- The `git reset` command :

The `git reset` command is a useful tool to help fix past mistakes. There are a lot of ways it can be used depending on the scenario.

- Undo the last commit :

What if while you are working on your project, you decide to create another file, file2.txt, and want to commit it into a new snapshot?
```
touch file2.txt
git add file2.txt
git commit -m "added a new file"
```
The commands above are all you need. Let’s see how this plays out in the terminal. We can use git status to verify what state our file is in while creating a new commit.

- The `--soft` flag :

If you want to modify or update your changes from the previous commit but don’t want to remove them completely, you can use the following command:
```
git reset --soft HEAD~1
```
The `--soft` flag changes the state of the committed files to “staged." You can see more clearly what happens when you run the command in a terminal. Note how the output that the `git status` command produces will change after you reset the most recent commit using the `--soft` flag. This flag preserves the changes.
```
The --hard flag
```
If you want to completely get rid of the changes that were part of the recent commit, you can use the --hard flag instead. It will reset the changes and not preserve them. Let’s see how this plays out in the terminal. Enter the following command in the terminal below:
```
git reset --hard HEAD~1
```
The `git reset` command can prove to be very useful if we want to update or revert changes made in older commits. The examples shown above dealt with reverting only the most recent commit. You will have noticed the reset commands used in this lesson had the `HEAD~1` portion. The number indicates how many commits you want to go back.

If you’re going to revert several older commits, you can change the number to how many commits you want to be reverted, and that will land you back to an earlier snapshot of your project. For example:
```
git reset --soft HEAD~2
```
would revert the two most recent commits.

This marks the end of the chapter. In the next chapter, we are going to learn about branches. But before we do, let’s take a small quiz to review the new commands we practiced and the concepts we’ve learned in this chapter.


## Branches

### What Is a Branch?
<hr>

In this lesson, you will learn what a branch is and how it is a central feature that allows git for making collaborative work convenient.

- Why are branches useful?

Let’s say you are working on a project with a team. You’ve been working on a significant feature that requires a lot of changes to the codebase, and, all of a sudden, one of your team members tells you that there is a major bug, and you need to prioritize it and fix it.

You will find yourself in a confusing situation. Not only will you need to switch context completely by focusing on the new issue at hand, but where will you store all the code you have been working on for the unfinished feature? The bug has nothing to do with the unfinished feature. Fixing the bug along with the feature is going to create a lot of confusion for everyone.

You will somehow need to go back to a state or snapshot of the source code before you started making changes to it for the feature, fix the bug, and then go back to work from where you had left off. This scenario is precisely where Git branches can work in your favor.

- Branches in Git :

In Git, you start with the one, primary branch called the master. This name is the default, given to the branch the moment you create your very first commit.

All the other commits you make from that point on are made on the master branch. Git, however, allows you to create as many other branches as you like.

You can create a separate branch that diverts away from the master and continue to do your work from there. The changes you make from that point forward and the commits you create will only be reflected in this branch and will not affect the source code in the master branch.

When you decide to create a new branch, what Git essentially does is create a new pointer to the current snapshot or commit to your project.

Therefore, the master branch has its pointer, and when you take a new branch out from the master branch, your new branch will have its pointer separate from the master.

The ability to create different branches allows you to work freely on the source code without affecting any other person’s work or the actual code in the master branch.

All the changes you make will be restricted to your branch and will not spill over to alter things you do not intend to alter.

This also allows you to switch back and forth between contexts without having to worry about what will happen to each branch once you move to another. Git is super flexible in this regard and has made working in collaborative environments extremely easy and convenient.

- Branches out of other branches :

Git lets you create a branch from any other branch. A new branch doesn’t necessarily have to come out of the master branch.


### Creating a Branch
<hr>

Learn how Git lets us create branches seamlessly and quickly.

- The` git branch` command :

The `git branch` command is a useful, multi-purpose tool that lets us do a lot of different things. When used as is (without any other options appended), the command will print out all the branches present in the repository and point out which branch we are currently on.

- git branch :

The `git branch` command will print out the `master` branch with a prepended asterisk. The asterisk denotes that this also happens to be the branch that is currently active in our repository. In other words, we are currently using the master branch. If there were more branches, their names would also be listed.

Let’s see how we can use the `git branch` to create a new one.

- How to create a new branch :

To create a new branch, we will need to modify the `git branch` command by appending a branch name.
```
git branch my_new_branch
```
Now, try to enter this command in the terminal provided below. You can name your new branch anything you like. However, it is preferred that the new branch not have a very long name or spaces in between.

After you create the new branch, enter the plain `git branch` command to double-check that it works. You will know if it works because the name will now be printed along with the master branch. One critical point to realize if you want to create a new branch in this manner is that you will still be using the parent branch in your working directory. That should be easy to identify, given the asterisk (`*`) next to the `master` branch name.

This is a significant point that you shouldn’t ignore. If you want to now switch to the newly created branch from the master, that is where the `git checkout` command will help you.


### Switching Between Branches
<hr>

Learn how Git allows us to quickly switch between different branches. This lesson also discusses an alternative way to create a new branch with Git.

- The `git checkout` command :

Using the `git branch` command lets us create new branches seamlessly. However, the problem is that even though we get to create new branches, we still don’t actually know how to switch over to those branches and use them. The `git checkout` command lets us do just that.

Once you create a new branch (let’s call it `new_branch`), use the following command while still currently on the `master` branch, to switch over to that new branch:
```
git checkout new_branch
```
And there you have it! We can now freely switch over from one branch to another. To test it out for yourself, use the terminal provided above to switch back to the `master` branch using the command:
```
git checkout master
```
To verify that you did switch to the `master` branch, use `git branch` to list all the branches in your repository. You will see the asterisk next to `master`, indicating that you are using the `master` branch once again.

- Creating new branches with `git checkout` :

Right now, we need to rely on entering two separate commands to create a branch and then switch over to it.

What if we could create a new branch that is a child of the branch that we are currently on and directly switch over to it with just one command? Well, `git checkout` lets us do that too.

- The `-b` flag :

Using the `-b` flag along with `git checkout` provides us with a convenient way to first implicitly execute `git branch` and then run `git checkout` to switch over to the newly created branch immediately. As an example, enter the following command in the terminal below:
```
git checkout -b new_branch
```
After entering the command above in the terminal, use `git branch` to see what exactly happens:

Congratulations! You’ve mastered how to create a new branch and switch over to it with one single command. To really see the benefits of working on and creating new branches, try the following scenario out in the terminal provided above. In the new branch that you just created, add a new file using the command:
```
touch file2.txt
```
Then, make Git track this new file:
```
git add file2.txt
```
Finally, commit the newly created file.
```
git commit -m 'created file2'
```
Now, you can switch back to the `master` branch, and you’ll realize that the new file isn’t there. For now, it will only be available to you if the new branch is the active branch in the current directory.


### Renaming Branches
<hr>

Learn how to rename a branch in this lesson.

You might find yourself in a situation where you have to rename the new branch you’ve created. Git provides a very convenient way to do so.

We will, once again, rely on the `git branch` command to rename an existing branch.

Let’s say you have been working on a significant feature. You want to add authentication to your application. The branch that you are making all the relevant changes to is called `new_branch`. The name `new_branch` is not related to what you are doing in any way. No one else will be able to identify what this branch is about, either. It is a better idea to call it something like `authentication_feature`.

- Renaming a branch you are currently on :

1. Switch over to the branch you have to rename with the following command :
```
git checkout new_branch
```
2. Use the git branch command appended with the -m flag to provide the new name:
```
git branch -m authentication_feature
```
To verify that you were able to rename the branch, use the plain `git branch` command to print out the list of branches and you will be able to see that the current branch you are on is now called `authentication_feature` instead of just `new_branch`.

- Renaming a branch without switching over to it :

What if you want to rename the branch but want to remain on the branch that you are originally using at that moment? The `git branch` command can do that too.

The general syntax for doing so is:
```
git branch -m old_name new_name
```
Therefore, if you want to rename `new_branch` as `authentication_feature` but also want to remain on the `master` branch, you would enter this command in the terminal:
```
git branch -m new_branch authentication_feature
```
Once again, you can use the plain `git branch` command to verify if the branch has the new name or not.


### Deleting a Branch
<hr?

Learn how to delete a branch from your local repository in this lesson.

- Using `git branch` to delete a branch :

We can use the `git branch` command to create, list, rename, and delete a branch. In this lesson, we will take a look at how we can delete a branch from our repository.

- The `-d` flag :

The syntax for deleting a branch is fairly simple:
```
git branch -d <branch_name>
```
If you have a branch called `new_branch` in your repository and want to remove it, you will need to enter the following command in the terminal:
```
git branch -d new_branch
```
As always, to double-check that the deletion process has been executed successfully, you can rely on the simple `git branch` command to verify this. The branch that is deleted should no longer be listed in the output.

> Note: You can’t delete the branch you are currently on. You will need to switch over to another branch and then delete it.


### Git Stash
<hr>

Learn how to use the git stash command to stash uncommitted changes in this lesson.

- The `git stash` command :

Often, you will be working on your separate branch and making some changes that you don’t want to commit just yet, but you will be required to switch over to another branch to do something else in between.

You don’t want to get rid of the changes but also don’t want to commit them either. This exact scenario is where you can use the `git stash` command.

`git stash` temporarily stores the staged and modified files in a kind of a cache, all the while making the working branch directory clean.

You could either stash all of the uncommitted changes you have made in the branch or stash individual files.
```
git stash
```
- When to use `git stash` :

Let’s say you are currently working on a branch called `new_branch` and you made some changes to the `file1.txt`. You can verify which branch you are on by using the command `git branch` and check which files have changed using the command `it status`.

Now, for some other task, you are required to move to the master branch. However, the changes to `file1.txt` aren’t ready to be committed yet, but you also don’t want to lose the changes.

Ideally, you want to switch to the master branch where the changes you have made to `file1.txt` do not exist. Once you are done working with the `master` branch, you want to go back to `new_branch` and continue working on the changes you had started.

Here is what you will need to do:

1. Enter the command `git stash` while you are still on `new_branch`.
2. Enter the command `git checkout master` to switch to the `master` branch.
3. After you have done whatever you needed to do on the master branch, you will, once more, enter `git checkout new_branch` to switch back again.
4. You want your changes to be present once again, so you will enter the command `git stash apply`.
5.  Enter `git status` to verify if your changes are back or not.

And there you have it. The uncommitted changes you had made are all back again in your working directory, and you will be able to continue with your work uninterrupted once more. You didn’t have to commit your unfinished work, and you were able to switch branches and still keep your changes! A win-win situation.

Had you decided not to use `git stash`, Git would have prevented you from switching over to any other branch if the other branch had changes that would be overwritten with the new uncommitted changes (since the changes in the other branch would be out of context). You would have to do one of the following:

Commit your unfinished work, switch branches, do your work, switch back to `new_branch`, and revert the most recent commit.
Completely get rid of the changes you had made, switch branches, do your work, switch back to `new_branch`, and start all over again.
In case the altered file does not conflict with the branch you plan to switch to, Git will let you switch over without errors and the uncommitted changes would still be present in that branch as well.


## Merging Branches


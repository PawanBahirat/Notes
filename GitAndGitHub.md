# Git And Github

- [Git And Github](#git-and-github)
  - [Getting Started](#getting-started)
    - [What Is Version Control?](#what-is-version-control)
    - [Why Is Git So Important?](#why-is-git-so-important)
    - [Basic Terminal-Based Text Editors](#basic-terminal-based-text-editors)
   
  
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

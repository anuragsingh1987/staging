 <p style="text-align:center;"><img title="a title" alt="Alt text" src="/git-resources/github_logo.png"></p>

# Using GitHub with PlayPen

*Please Note : Though this repository has been created considering users of all levels (beginners, intermediate and experts) , but it is recommended that before using the repo , you should complete some course offered by pluralsight which is available to all LGB employees. The course will provide all the required and idepth knowledge about docker and should be supplemented by hands On labs supplied as part of this repo.*

**Here is the course link and description -- >   <<Link to be added>>**


## What is Git

Git is a distributed version control system used for tracking changes in source code during software development. It was created by Linus Torvalds in 2005 for managing the development of the Linux kernel, but it has since become widely used for version control in software development projects of all sizes and types.

With Git, developers can keep track of changes made to the source code, collaborate with others on the same project, and easily revert back to previous versions of the code if necessary. It allows developers to work on different features or parts of the codebase in parallel, and then merge their changes together into a single codebase.

Git is distributed, which means that every developer working on a project has a complete copy of the codebase, rather than just a single centralized repository. This makes it easier to work offline and allows for greater flexibility in managing code changes across multiple developers and locations.

## Git Vs GitHub

Git and GitHub are related but distinct tools used for managing source code.

Git is a distributed version control system used for tracking changes in source code during software development. It is a command-line tool that allows developers to manage changes to their codebase locally on their own machines, and to collaborate with other developers by sharing changes with them.

GitHub, on the other hand, is a web-based platform built on top of Git that provides additional features for managing and collaborating on Git repositories. It provides a web-based interface for managing Git repositories, as well as additional tools for managing issues, pull requests, and other aspects of software development.

GitHub allows developers to share their code with others, collaborate on open source projects, and contribute to existing projects. It also provides tools for managing project workflows, such as issue tracking and pull requests, which help developers to review and manage changes to the codebase.

In short, Git is a version control system, while GitHub is a platform for hosting, sharing, and collaborating on Git repositories. While Git can be used without GitHub, GitHub is designed to work seamlessly with Git and provides a convenient way to manage and collaborate on code projects.

## GitHub Actions

GitHub Actions is a powerful tool provided by GitHub for automating workflows and tasks within your software development projects. It allows you to define custom workflows as code, which can then be triggered by events such as code changes, pull requests, or scheduled times.

GitHub Actions can be used to automate a wide variety of tasks, such as building and testing code, deploying applications, and releasing software. You can define workflows using YAML syntax, and you have access to a wide range of pre-built actions that you can use within your workflows, as well as the ability to create your own custom actions.

One of the main benefits of GitHub Actions is that it is tightly integrated with GitHub, allowing you to easily trigger workflows based on events within your repositories. It also provides a robust set of features for managing your workflows, including the ability to monitor the status of your workflows, view logs, and receive notifications when workflows succeed or fail.

GitHub Actions is free for public repositories and offers a certain amount of free usage for private repositories, with additional usage available through paid plans. Overall, it is a powerful tool that can help streamline your development workflows and increase productivity within your team.



## Git Branches

<p style="text-align:center;"><img title="a title" alt="Alt text" src="/git-resources/gitflow2.png"></p>

In Git, branches are used to isolate development work from other branches. This allows multiple developers to work on different features or fixes simultaneously without interfering with each other's code. Here are some key concepts and commands related to Git branches:


1. Creating a new branch: Use the `git branch` command followed by the name of the new branch to create a new branch. For example, `git branch new-feature` creates a new branch called "new-feature".
2. Switching to a branch: Use the `git checkout` command followed by the name of the branch to switch to it. For example, `git checkout new-feature` switches to the "new-feature" branch.
3. Creating and switching to a new branch in one command: Use the `git checkout -b` command followed by the name of the new branch to create a new branch and switch to it in one step. For example, `git checkout -b new-feature` creates a new branch called "new-feature" and switches to it.
4. Merging branches: Use the `git merge` command followed by the name of the branch to merge it into the current branch. For example, if you're on the "master" branch and want to merge the "new-feature" branch, run `git merge new-feature`.
5. Viewing branches: Use the `git branch` command to view a list of branches in the repository. The current branch will be marked with an asterisk.
6. Deleting branches: Use the `git branch -d` command followed by the name of the branch to delete it. For example, `git branch -d new-feature` deletes the "new-feature" branch.
7. Renaming branches: Use the `git branch -m` command followed by the new name to rename a branch. For example, `git branch -m old-branch new-branch` renames the "old-branch" to "new-branch".

These are just a few of the many commands and concepts related to Git branches. By mastering these basic commands, you'll be able to manage your Git repository and collaborate with other developers more effectively.

## Git Push vs Git Pull vs Git Fork

Git push, git pull, and git fork are three different Git operations that are commonly used in software development.

* **Git push** is used to upload local changes to a remote repository. When you commit changes to your local Git repository, you can use the git push command to send those changes to a remote repository, such as on GitHub or GitLab. This is useful for sharing your changes with others or backing up your work.
* **Git pull** is used to download changes from a remote repository. When you want to update your local repository with changes that have been made on a remote repository, you can use the git pull command to fetch and merge those changes into your local repository.
* **Git fork** is used to create a copy of a remote repository. When you want to contribute to a project that is hosted on a remote repository, you can use the git fork command to create your own copy of the repository. This allows you to make changes to the code without affecting the original project. You can then make a pull request to the original repository to propose your changes.

In summary, git push is used to upload local changes to a remote repository, git pull is used to download changes from a remote repository, and git fork is used to create a copy of a remote repository for contribution purposes.


## Frequently used Git Commands

Here are some common Git commands that you can use to manage your Git repository:


 1. `git init`: Initializes a new Git repository in your current directory.
 2. `git add`: Adds files to the staging area for a commit.
 3. `git commit`: Creates a new commit with the changes in the staging area.
 4. `git clone`: Copies a remote repository to your local machine.
 5. `git pull`: Fetches and merges changes from a remote repository to your local machine.
 6. `git push`: Sends committed changes to a remote repository.
 7. `git status`: Shows the current status of the Git repository, including any changes that have been made.
 8. `git log`: Displays the commit history of the repository.
 9. `git branch`: Shows a list of branches in the repository.
10. `git checkout`: Switches to a different branch in the repository.
11. `git merge`: Combines changes from one branch to another.
12. `git remote`: Manages connections to remote repositories.
13. `git stash`: Temporarily saves changes that are not ready to be committed.

These are just a few of the many Git commands available. By mastering these basic commands, you'll be able to manage your Git repository with confidence and efficiency.

## Here are some resources you can use to learn Git and GitHub:

* Official Git documentation: https://git-scm.com/docs
* GitHub's Git cheat sheet: https://github.github.com/training-kit/downloads/github-git-cheat-sheet/
* Atlassian's Git tutorials: https://www.atlassian.com/git
* Git Immersion interactive tutorial: https://gitimmersion.com/
* Pro Git book: https://git-scm.com/book/en/v2
* GitKraken's Git command reference: https://www.gitkraken.com/git-commands
* GitLab's Git tutorial: https://docs.gitlab.com/ee/git/


These resources provide a wealth of information about Git, from basic commands and concepts to advanced techniques and workflows. By using these resources, you can become a more effective and efficient Git user.
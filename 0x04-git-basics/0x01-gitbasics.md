# Git Basics

- First time configuration for git locally
- Install [Git](https://git-scm.com/downloads)
- Download and install git for your preferred OS.
- Connect git to github (_or login into github locally_)
  - You need to have a [github account](https://github.com/)
- Open git bash and run the following commands to connect our local git to github.

```bash
# add email address
git config --global user.email "emailHere"
# username
git config --global user.name "usernameHere"
# add github password (OPTIONAL)
git config --global user.password

# to login
git login
```

- To check your configuration file

`git config --list`

## Create a local repository

- A repo is a folder
- To create a local repository
- Create Folder

```bash
mkdir <folder_name>
cd <folder_name>
```

- Initialize git in the folder.So that git can recognize it as a local repository and track changes in the folder

  `git init`

- Create a file (_files in the airport analogy_) in the folder

  `touch <file_name>`

- Check the status of the repo

  `git status`

> **TIP:** Run `git status` every after a command to see what you have done

- To track the file , we need to add it to the staging area (_plane in the airport analogy_).

```bash
# if we add a file to the staging area

# add a specific file
git add <file_name>

# add all untracked files
git add .
```

- We pass a commit message (_this would be our passport and visa to explain what we are and why we are going adn what we do_)

```bash
git commit -m"Add Filename"

```

## Pushing to github

- To connect our local repository to Github repository.
- Change the branch name to `main` from `master` (_Because of #BLM_)
  `git branch -m main`

```bash
# from
user@Kolynzb MINGW64 ~/Desktop/lessons/Jamstack-shoun (master)
# to
user@Kolynzb MINGW64 ~/Desktop/lessons/Jamstack-shoun (main)
```

- Create a remote repository on github.com

```bash
# create a connection between your local repo and your remote repository
git remote add origin https://github.com/kolynzb/sdsdsd.git
# will create the main branch on your remote repo and push the change to it
git push -u origin main

```

- If you make any other changes , stage them , commit them then run `git push` to update changes on the the remote repository.

## Writing Proper Commit Messages

- Should in command mode
- It should briefly explain what the commit does
- Before you write it recite this `This COmmit will <Commit message>`
- Capitalize all first letters.

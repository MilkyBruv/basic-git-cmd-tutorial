# Basic Git Command Line Guide
Basic guide to using git in the command line

## Install Git
Download the git installer for your machine from [https://git-scm.com/downloads](https://git-scm.com/downloads)

Then run the installer and go through the setup wizard

When you get to the part to override the default branch name, select `Override the default branch name for new repositories`, and set it to `main`

To check if git is installed, go to your terminal and type `git --version`, and if you get no errors proceed forwards to the next section

If you get any errors, uninstall git (if possible) and go back through the steps


## Repository Setup

To setup a basic git project, go to github and create a new repository

Copy the link to the repository

Create a new folder where you wish to have your project, then open a terminal window at that directory

Type `git init`, it should say `Initialized empty Git repository in <your directory>/.git/`

Next, type `git remote add origin <link to github repository>`, this will setup the link between your directory and the repository

Finally, type `git checkout main` to switch to the main branch


## Basic Usage

### Add, Commit, Push

Once you have made the changes you want to your local files, type `git add .` in the base directory

Then, type `git status`, which will show you all your applied changes in green text

After that, type `git commit -m "<commit message>"`, which will stage your changes and get them ready to push

Finally, type `git push -u -f origin main`, this will push the files to github


### Fetching vs. Pulling

To fetch the files from github, type `git fetch remote origin`, this will download any files that are not present to your local directory

If that does not fetch all the files, try typing `git fetch <link to github repository>`

`git fetch` will copy across any files that are not present in your local directory from github, but it will NOT update any changes to files


To pull the files from github, type `git pull`, this will update the files in your local directory

`git pull origin main` will copy across any files that are not present in your local directory from github, and it WILL update any changes to files


### Cloning

To clone a repository, type `git clone <link to github repository>`, this will download all the files from the repository

Note that this will not let you edit the files on the repository

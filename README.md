# github-tutorial
An example repo used to teach git and Github

## Installing git
**Note**: You may have used git for class (eg. through Eclipse for 401), but you should still follow this tutorial to learn how we use git.

If you would like to use git through command line,
follow [this link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install git. **[Recommended]**

If you would like to use git through a GUI, follow [this link](https://desktop.github.com/) to install Github for Desktop.

## Cloning the Repository
### Command Line
1. On Linux or MAC, open your terminal. On Windows, open Git Bash. This will be your command line for using git commands.
1. Navigate to the location where you want to create the project folder for the git repository.
    - I will navigate to my `Documents` folder.
    - These commands will help you navigate in your command line:
    1. `pwd`: Print working directory. This command will tell you where you are in your file directory.
    1. `ls`: List. This command will list all the files and folders at your current location.
    1. `cd`: Change directory. This command will let you move around your file directory.
        - If I am in `/c/Users/AustinWang` and I use `cd Documents`, I will end up in `/c/Users/AustinWang/Documents`. 
        - Alternatively I can use `cd /c/Users/AustinWang/Documents` to navigate to the same folder directly. 
1. Go back to the [Github repository page](https://github.com/unc-cs-sg/github-tutorial) and find the green button on the right that says "Clone or download". Copy the link.
1. Return to your command line. Type `git clone GIT_REPO_LINK` where `GIT_REPO_LINK` is the link you copied.
1. You will now have a folder named `github-tutorial` at your current location. Use `ls` to see it and use `cd github-example` to move to the folder. This folder is your local git repository.
### GUI
1. Go to the [Github repository page](https://github.com/unc-cs-sg/github-tutorial) and find the green button on the right that says "Clone or download". Copy the link.
1. Open Github for Desktop and login to your Github account.
1. Click `Clone a repository from the Internet...`
1. Click the `URL` tab.
1. In `URL or username/repository` enter the repo link you copied earlier. In `Local path` enter where you want to create the project folder.
1. Click `Clone`. You should now be able to access the project in the Github for Desktop.

## Making Changes to a Branch
### Command Line
1. Open your command line. Navigate to your `github-example` repository.
1. You will now make a new branch. A branch is like a separate version of the repository. Choose a name for your branch (your Github username works). 
1. Create a new branch and switch to it. All your changes will now edit this branch.
    - You can create the branch and switch to it in one command by typing `git checkout -b NAME_OF_BRANCH`.
    - You can also do this by typing `git branch NAME_OF_BRANCH` to create your branch and `git checkout NAME_OF_BRANCH` to switch to it.
1. Open the `README.md` file from the `github-example` folder in any editor.
1. Go to the bottom of the file and add your name under `CS+SG Team`.
### GUI
1. Open Github for Desktop and open the `github-example` project.
1. You will now make a new branch. A branch is like a separate version of the repository. Choose a name for your branch (your Github username works).
1. Click the `Current branch: master` tab. This should give you a dropdown.
1. Click `New branch`. This should open a pop-up.
1. Enter the name for your new branch and click `Create branch`.
    1. If you have already made changes, a pop-up will appear. If you would like to keep your changes click `Bring my changes...` and click `Switch to branch`.
1. Open the `README.md` file in any editor. You can go to the `Repository` menu (in the top menu bar) to open the project in your file explorer, text editor, or command prompt if you don't remember where you cloned it.
1. Go to the bottom of the file and add your name under `CS+SG Team`.

## Pushing to Github Remote Repo
### Command Line
1. Open your command line. Navigate to your `github-example` repository.
1. Type `git status`. You should see the files you've changed. `README.md` should show up here.
1. Type `git add README.md`. This command will add `README.md` to the files you want to commit (or save).
1. Type `git commit -m COMMIT_MESSAGE` where `COMMIT_MESSAGE` is a short description of your changes. This will create a commit (or save a snapshot of your changes).
1. Type `git push origin NAME_OF_BRANCH` where `NAME_OF_BRANCH` is the name of your new branch. This will send the local commits you made to the Github repository.
### GUI
1. Open Github for Desktop and open the `github-example` project.
1. In the left panel, open the `Changes` tab.
1. At the bottom of the panel, find the text box next to your profile picture. It should say `Update README.md`. Type a short description of your changes here.
    1. If you have a longer description, you can add it in the `Description` box.
1. Click `Commit to NAME_OF_BRANCH`.
1. Click `Publish branch`.

## Making a Pull Request
1. Open your web browser and go the the [Github repo](https://github.com/unc-cs-sg/github-tutorial).
1. Go to the `Pull requests` tab.
1. Click `New pull request`.
1. For `base` choose `master` and for `compare` choose your new branch.
1. Click `Create pull request`.
1. Once this pull request is approved, the changes in your branch will be merged into the master branch.

## CS+SG Team
- Austin Wang

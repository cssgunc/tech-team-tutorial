# Tech Team Tutorial
In this tutorial you'll learn some basics of React, Git and Github. You're not expected to be an expert by the end of this guide, but you'll get a glimpse of the tools we use on our Tech Teams.

## Installing Software
### Git
At CS+SG (and in the software industry), we use Git through the command line.
Follow [this link](https://Git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install Git. The default installation options should be fine.

Notes: 
- **DO NOT** install Github Desktop. While it's a useful tool for learning Git, it has some limitations and is not commonly used in industry.
- You may have used Git for class (eg. through Eclipse for 401), but you should still follow this tutorial to learn how we use Git.

### Text Editor
You may already have a text editor that you're comfortable with, but if not, we recommend [Visual Studio Code](https://code.visualstudio.com/).

## Learning the Command Line
Once you have Git installed, we'll start working in the command line.
1. Determine what terminal you'll be using.
    - On **Mac**, you can simply use **Terminal**. 
    - On **Windows**, you can use **Powershell** or **Git Bash** (this should have been installed along with Git for Windows).
    - On **Linux**, you're probably familiar with the command line already.

Next we'll learn how to navigate the command line.
1. Read over these commands and try them out in your terminal. You'll use these to navigate in your command line:
    1. `pwd`: Print working directory. This command will tell you where you are in your file directory.
    1. `ls`: List. This command will list all the files and folders at your current location.
        - You can run `ls -a` to list any hidden files as well.
    1. `cd`: Change directory. This command will let you move around your file directory.
        - If I am in `/c/Users/AustinWang` and I use `cd Documents`, I will end up in `/c/Users/AustinWang/Documents`. 
        - Alternatively I can use `cd /c/Users/AustinWang/Documents` to navigate to the same folder directly.
        - Running `cd ..` will bring you up one folder relative to your current location.
            - Eg. If I am in `/c/Users/AustinWang/Documents` and I run `cd ..`,  I will end up in `/c/Users/AustinWang`
1. Determine where you want to create the folder for this project. You don't need to actually create a folder yet.
    - Eg. I've decided to use my `Documents` folder.
1. Using the commands above, navigate to the location you've chosen.

## Cloning the Repository
Now we'll copy the project from GitHub to your computer.
1. Go to the [Github repository page](https://Github.com/unc-cs-sg/Github-tutorial) for this tutorial (if you're already here just scroll up) and find the green button on the right side of the page. It should say **"Clone or download"** or **"Code"**. Click on the button and copy the link under **Clone with HTTPS**.
    - TODO: Add screenshot
1. Return to your command line. Type `Git clone GIT_REPO_LINK` but replace `GIT_REPO_LINK` with the link you copied. This will download the project from GitHub onto your computer.
    - TODO: Add screenshot
1. You will now have a folder named `Github-tutorial` at your current location. Use `ls` to see it and use `cd Github-tutorial` to move to the folder. This folder is your local Git repository.
    - TODO: Add screenshot

## Making Changes to a Branch
Now you'll learn how to make a new branch in Git. Each branch is like a separate copy of the Git repository. Each repository will have a main branch. A new branch can be used like a working copy of your project. You can make changes in a branch without affecting the main branch, and merge your changes in once you're done.
1. Open your command line. Navigate to your `Github-tutorial` folder.
1. Choose a name for your branch.
    - For this tutorial, you can name your branch after yourself or your GitHub username. Try not to pick something that other people might also use.
1. Create a new branch and switch to it. You can  do this in one command by typing `Git checkout -b NAME_OF_BRANCH`.
    - You can also do this by typing `Git branch NAME_OF_BRANCH` to create your branch, and `Git checkout NAME_OF_BRANCH` to switch to it.
1. Open the `README.md` file from the `Github-tutorial` folder in any text editor.
1. Go to the bottom of the file and add your name under `CS+SG Team`.

## Commiting your changes and Pushing to GitHub
Now that you've made changes locally, you'll learn how to save those changes and upload them to GitHub.
1. Open your command line. Navigate to your `Github-tutorial` repository.
1. Type `Git status`. This will show you what files you've changed. `README.md` should show up here.
1. Type `Git add README.md`. This command will add `README.md` to the files you want to commit (or save).
1. Type `Git commit -m COMMIT_MESSAGE` but replace `COMMIT_MESSAGE` is a short description of your changes. This will create a commit (or save your changes).
1. Type `Git push origin NAME_OF_BRANCH` but replace `NAME_OF_BRANCH` is the name of your new branch. This will upload the local commits you've made to the GitHub repository.

## React
This semester, our Tech Teams will most likely be working with React. In this section, we're asking you to follow the official React tutorial. This will get you familiar with React, but you'll also be expected to pick up new skills during the semester.

1. Navigate to your `Github-tutorial` repository and create a new folder named after your GitHub username. 
1. `cd` into the new folder. This is where you'll create the project for the React tutorial.
1. Follow the [React tutorial](https://reactjs.org/tutorial/tutorial.html#setup-option-2-local-development-environment). This will require you to use the command line.
    - In **Setup for the Tutorial**, please follow **Option 2: Local Development Environment**.
1. Once you're done commit and push your changes to GitHub.

## Making a Pull Request
After you've finished working on your branch, you can create a pull request to merge your branch back into the main branch.
1. Open your web browser and go the the [Github repo](https://Github.com/unc-cs-sg/Github-tutorial).
1. Go to the `Pull requests` tab.
1. Click `New pull request`.
1. For `base` choose `master` and for `compare` choose your new branch.
1. Click `Create pull request`.
1. Once this pull request is approved, the changes in your branch will be merged into the master branch.

## CS+SG Team
- Austin Wang

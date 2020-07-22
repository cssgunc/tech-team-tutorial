# Tech Team Tutorial
In this tutorial you'll learn some basics of React, Git and GitHub. We don't expect you to be an expert by the end of this guide, but you will get a glimpse of the tools and technologies we use on our Tech Teams.

## TL;DR
If you're already familiar with React, Git, and GitHub, please do the following:
1. Fork this repo and clone it. Create a new branch.
2. Add your name to the bottom of this README.
3. Create a new folder named after your GitHub username in the `react-projects` folder. Within this new folder create a React app following the [React tutorial](https://reactjs.org/tutorial/tutorial.html).
4. Push to your fork and open a pull request to the master branch of this repo.

## Create a GitHub account
If you don't already have one, you'll need to create an account on GitHub.

## Installing Software
### Text Editor
You may already have a text editor that you're comfortable with. If not, we recommend [Visual Studio Code](https://code.visualstudio.com/).

### Git
At CS+SG, we use Git for version control.

1. Follow [this link](https://Git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install Git. The default installation options should be fine.
    - **DO NOT** install GitHub Desktop. While it's a useful tool for learning Git, it has some limitations and is not commonly used in industry.
    - You may have used Git for class (eg. through Eclipse for 401), but you should still follow this tutorial to learn how we use Git.

## Learning the Command Line
Once you have Git installed, you can start working in the command line.
1. Determine what terminal you'll be using.
    - If you're using Visual Studio Code, you can open a terminal by going to the top menu and selecting Terminal > New Terminal.
    - On **Mac**, you can use **Terminal**.
    - On **Windows**, you can use **Powershell** or **Git Bash** (this should have been installed along with Git for Windows).
    - On **Linux**, you're probably familiar with the command line already.
1. Open your terminal. First we'll need to set up Git with your GitHub account information.
    - Type `git config --global user.email "you@example.com"` and set your email to the same one you used to create your GitHub account.
    - Type `git config --global user.name "Your Name"` and set it to your name (or the name you want to be shown on the code you write). This does not have to be the same as your GitHub username.
1. You'll use these commands to navigate in your terminal. Read over these commands and try them out in your terminal:
    1. `pwd`: Print working directory. This command will tell you where you are in your file directory.
    1. `ls`: List. This command will list all the files and folders at your current location.
        - You can run `ls -a` to list any hidden files as well.
    1. `cd`: Change directory. This command will let you move around your file directory.
        - If I am in `/c/Users/AustinWang` and I use `cd Documents`, I will end up in `/c/Users/AustinWang/Documents`.
        - Alternatively I can use `cd /c/Users/AustinWang/Documents` to navigate to the same folder directly.
        - A single dot `.` refers to the current folder you're in. Two dots `..` refers to the folder one level up. Running `cd ..` will bring you up one folder relative to your current location.
            - Eg. If I am in `/c/Users/AustinWang/Documents` and I run `cd ..`,  I will end up in `/c/Users/AustinWang`
            - You can chain these with slashes. So `cd ../../..` will bring you up three levels.
    1. `code`: If you installed Visual Studio Code and added it to your path during installation, this command will open it from terminal. If you're not using VS Code, you can ignore this command.
        - You can type `code PATH/TO/FOLDER_OR_FILE' to open a folder or file directly in VS Code.
        - Eg. Type `code .` to open the folder you're currently in with VS Code.
1. Determine where you want to create the folder for this project. You don't need to actually create a folder yet.
    - Eg. I've decided to use my `Documents` folder.
1. Using the commands above, navigate to the location you've chosen.
    - Eg. For me, I'd run `cd /c/Users/AustinWang/Documents`

## Forking and Cloning the Repository
The first thing you'll do here is fork the repository. This will make a copy of the GitHub repository under your GitHub account.

1. Go to the [GitHub repository page](https://github.com/unc-cs-sg/tech-team-tutorial) for this tutorial (if you're already here just scroll up). In the top right corner of the page, click **Fork**.

![Forking the repo](/images/github-fork.png)

Next you'll copy the project from GitHub to your computer.

1. Go to the **fork** repository you just made (not the original repo). Find the green button on the right side of the page. It should say **"Clone or download"** or **"Code"**. Click on the button and copy the link under **Clone with HTTPS**.

![Getting the repo link](/images/github-clone-link.png)

1. Open your command line and use `cd` to navigate to the folder where you want to download the project (eg. `Documents`). Type `git clone GIT_REPO_LINK` but replace `GIT_REPO_LINK` with the link you copied. This will download the project from GitHub onto your computer.
    - Eg. For my fork, I would run `cd /c/Users/AustinWang/Documents` and then run `git clone https://github.com/Dafondo/tech-team-tutorial.git`
1. You will now have a folder named `tech-team-tutorial` at your current location. Use `ls` to see it and use `cd tech-team-tutorial` to move into the folder. This folder is your local Git repository.

## Making Changes to a Branch
Now you'll learn how to make a new branch in Git. Each branch is like a separate copy of the Git repository. A new branch can be used like a working copy of your project. You can make changes in a branch without affecting the main branch, and merge your changes in once you're done.

1. Open your command line. Navigate to your `tech-team-tutorial` folder.
1. First, to make sure your local repo is up-to-date, run `git pull`. This will pull any new changes that other people have made to the GitHub repository. This is always a good idea if you haven't worked on a Git project in a while.
1. Choose a name for your branch. For this tutorial, you can name your branch after yourself or your GitHub username. Try not to pick something that other people might also use.
    - Eg. I'll name my branch `dafondo`, my GitHub username.
1. Type `git checkout -b NAME_OF_BRANCH` but replace `NAME_OF_BRANCH` with the branch name you've chosen. This will create a new branch and switch to it.
    - Alternatively, you can type `git branch NAME_OF_BRANCH` to create your branch, and `git checkout NAME_OF_BRANCH` to switch to it.
1. Open the `README.md` file in the `tech-team-tutorial` folder with any text editor.
1. Go to the bottom of the file and add your name under `CS+SG Team` and **save** the file.

## Commiting your changes and Pushing to GitHub
Now that you've made changes locally, you'll learn how to save those changes and upload them to GitHub.
1. Open your command line. Navigate to your `tech-team-tutorial` repository.
1. Type `git status`. This will show you what files you've changed. `README.md` should show up here.
1. Type `git add README.md`. This command will add `README.md` to the files you want to commit (or save).
    - You can type `git add -A` to add all changed files or `git add .` to add all changed files in your current working directory.
1. Type `git commit -m COMMIT_MESSAGE` but replace `COMMIT_MESSAGE` with a short description of your changes. This will create a commit (or save your changes).
    - If you made a mistake in your commit or commit message, you can type `git commit --amend` to fix it before pushing.
1. Type `git push origin NAME_OF_BRANCH` but replace `NAME_OF_BRANCH` with the name of your new branch. This will upload the local commits you've made to your fork's GitHub repository.

## React
This semester, our Tech Teams will most likely be working with React. In this section, we're asking you to follow the official React tutorial. This will get you familiar with React, but you'll also be expected to pick up new skills during the semester.

1. Navigate to the `react-projects` folder within the `tech-team-tutorial` repository. Create a new folder named after your GitHub username and `cd` into it. This is where you'll create the project for the React tutorial.
1. (Read the bullet points below for important info) Follow the [React tutorial](https://reactjs.org/tutorial/tutorial.html). This will require some software installation and use of the command line.
    - In **Setup for the Tutorial**, please follow **Option 2: Local Development Environment**.
    - If you're on Windows and using **Git Bash** as your terminal, follow the Mac/Linux commands in the tutorial instead of the Windows commands.
1. Once you're done commit and push your changes to GitHub.

Tips:
- Please read the sections between the coding portions. Sometimes they give additional instructions that you might otherwise miss.
- If you get lost on what part of the code to edit, re-read the section, and try CTRL-F to find the appropriate section in your code.
- If you make a mistake and get an error when running your React app in the browser, it should give you a line number to check.
    - This is typically formatted as `lineNumber:characterNumber`.
    - Check for typos!

## Making a Pull Request
After you've finished working on your branch, you can create a pull request to merge your branch back into the main branch.
1. Open your web browser and go your fork's GitHub page.
1. Go to the `Pull requests` tab.
1. Click `New pull request`.
1. Make sure these values match
    - `base repository`: `unc-cs-sg/tech-team-tutorial`
    - `base`: `master`
    - `head repository`: your fork repo
    - `compare`: your new branch.

![Opening a pull request](/images/github-pr.png)
1. Click `Create pull request`. This will create a request to merge your new branch from your fork into the main branch of the original repository.
1. Once this pull request is approved, the changes in your branch will be merged into the master branch.

## Congrats, you're done!
We hope you've learned something through this tutorial. It's okay if you still have a lot of questions. You'll be putting these skills to practice on the Tech Teams, and picking up new ones along the way!

## CS+SG Team
- Austin Wang
- Sami Habib
- Amaya Jenkins
- Tanying Lin
- Kavish Gandhi
- Pranith Koppula
- Lucas Zhang
- Avery Marsh

# How to contribute to PSR

Contributing to PSR can be as easy as answering questions about the runs in their respective Discord channel, or as complex as writing in depth guides. Every bit of help and every bit of knowledge shared helps.

## Writing Guides

In the past years an effort was put in streamlining all guides to be available at one place, that place being the [PSR GitHub Pages](https://pokemon-speedrunning.github.io/speedrun-routes/#/).  
GitHub Pages acts as a wiki replacement, allowing people to suggest changes that then need to be approved by selected reviewers before they go public.  

All pages are formatted with GitHub flavored Markdown. To learn more about this, click [here](https://guides.github.com/features/mastering-markdown/).

### Setting up Git

* Download and install [Git (https://git-scm.com/downloads)](https://git-scm.com/downloads) for your appropriate OS.
    * You can leave all the installation options as default
* Go to [GitHub](https://github.com) and sign up for an account.
* Navigate to the [Speedrun Routes Repository](https://github.com/pokemon-speedrunning/speedrun-routes) and hit `Fork` in the top right corner.
    * You should be on a copy of the speedrun-routes repository in your own account.
* Click the green `Code` button and copy the link in the box.
* On your computer, navigate to the location where you want to store a local copy of `speedrun-routes`.
* Once you have that location open, you should be able to right click and press `Git Bash Here` if you installed Git with the default options.
* In your Git Bash shell, type `git config --global user.name "YOUR USERNAME"`, with the quotation marks included as part of the command.
* In your Git Bash shell, type `git config --global user.email you@example.com`, with your email address
* In the Git Bash window, type `git clone ` followed by the link you copied from GitHub and press Enter. In Git Bash, you can paste using `shift+ins`
    * e.g. `git clone https://github.com/hwangbro/speedrun-routes.git`
* After the command finishes, you should have a copy of `speedrun-routes` downloaded to your computer.


### Configuring your local copy
* In Git Bash, navigate to the `speedrun-routes` folder with the command `cd speedrun-routes`
    * To navigate to different folders in Git Bash, you can do `cd <folder_name>` to go into a folder, and `cd ..` to leave that folder.
    * You can also do `ls` to list the files in the current folder, or `pwd` to list the current directory you are in.
* Once here, we need to setup our repo to point to the original copy. Enter the command `git remote add upstream https://github.com/pokemon-speedrunning/speedrun-routes`
* Now our repo is properly setup to start contributing!


### Updating your local copy
* The first thing you should do when you want to start on a new change is to create a new branch in your repo. In Git, branches allow you to contain related sets of changes so they can be suggested as a group. When you want to add a new feature or fix a bug - no matter how big or how small - you should spawn a new branch to encapsulate your changes.
* First, we want to make sure our repo has the latest version of the original copy. Enter the command `git fetch upstream main` in your Git Bash shell.
    * You should be prompted with a window to sign in to your GitHub account. Click `Sign in with your browser` and log in.


### Creating a new branch
* For every feature, bug fix, or chnage that we want to work on, we want to create a new branch to separate this work from anything unrelated.
    * For example, we would want separate branches for adding a route, fixing typos, and/or deleting outdated manip pages.
* To create a new branch, enter the command `git checkout upstream/main -b YOUR_BRANCH_NAME`, where your branch name can be anything you want to call it.
    * It's common to group branches as `feature` or `bugfix`
    * For example, if I'm updating a beginner guide for Yellow NSC I might call it `feature/beginner-ynsc`, but if I'm fixing spelling in gold glitchless I might call it `bugfix/gold-glitchless-spelling`
* To see a list of your current branches, you can use the command `git branch -l`.
* In order to switch between branches, you can use the command `git checkout <branch_name>`
* Now that we're here, you can start making changes to the route files you downloaded locally.


### Making Changes and Uploading them to GitHub
* First, we need to make sure we're in the correct branch. Start by doing a `git checkout YOUR_BRANCH_NAME`, where your branch name is the same one as the one you created above.
* In your Git Bash shell, you can use `git add -A` to stage files.
    * You can do the command `git status` to see a summary of what files you've made changes to in red
* Staging files helps bundle even more closely related changes into a "commit". You can run the commit by doing `git commit -m "YOUR DESCRIPTION HERE"`, where you give a short description of your changes. The quotation marks need to be part of this command.
    * For example, `git commit -m "Update Moon Rocket fight in Beginner Guide"`
* Then we want to push this commit back to GitHub. Do this by doing a `git push origin`.

* If you need to make more changes, you can go repeat the steps outlined in the above section for any additional files or changes.


### Making a Pull Request
* In GitHub, a Pull Request represents a proposal to make some changes, and is usually reviewed and approved by someone else. To start, we need to upload our changes to our local fork of `speedrun-routes`.
* If you go back to your fork of speedrun-routes (https://github.com/<YOUR_GITHUB_NAME>/speedrun-routes) on your GitHub account and click the `branches` button, you should see your newly created branch listed there.
* Once you click the branch that you created, you should see a green "Compare & pull request" button at the top. Click that once you are ready to have your changes reviewed.
* On this page, you can add a short description to represent your changes, then click the green `Create pull request` to submit a pull request.


### Updating a Pull Request
* If a reviewer of your pull request has some changes they want you to make, you can repeat the steps in `Making Changes and Uploading them to GitHub`, and your pull request should automatically be updated.

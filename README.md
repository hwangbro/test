# How to contribute to PSR

Contributing to PSR can be as easy as answering questions about the runs in their respective Discord channel, or as complex as writing in depth guides. Every bit of help and every bit of knowledge shared helps.

## Writing Guides

In the past years an effort was put in streamlining all guides to be available at one place, that place being the [PSR GitHub Pages](https://pokemon-speedrunning.github.io/speedrun-routes/#/).  
GitHub Pages acts as a wiki replacement, allowing people to suggest changes that then need to be approved by selected reviewers before they go public.  

All pages are formated with GitHub flavored Markdown, to learn more about this, click [here](https://guides.github.com/features/mastering-markdown/).

### Setting up GitHub Desktop

* Download and install [Git (https://git-scm.com/downloads)](https://git-scm.com/downloads) from one of the top links for your the appropriate OS.
    * You can leave all the installation options as default
* Go to [GitHub](https://github.com) and sign up for an account.
* Navigate to the [Speedrun Routes Repository](https://github.com/pokemon-speedrunning/speedrun-routes) and hit `Fork` in the top right corner.
    * You should be on a copy of the speedrun-routes repository in your own account.
* Click the green `Code` button and copy the link in the box.
* On your computer, navigate to the location where you want to store a local copy of `speedrun-routes`.
* Once you have that location open, you should be able to right click and press `Git Bash Here` if you installed Git with the default options
* In the Git Bash window, type `git clone ` followed by the link you copied from GitHub and press Enter. In Git Bash, you can paste using `shift+ins`
    * e.g. `git clone https://github.com/hwangbro/speedrun-routes.git`
* After the command finishes, you should have a copy of `speedrun-routes` downloaded to your computer.


### Configuring your local copy
* In Git Bash, navigate to the `speedrun-routes` folder with the command `cd speedrun-routes`
* Once here, we need to setup our repo to point to the original copy. Enter the command `git remote add upstream https://github.com/pokemon-speedrunning/speedrun-routes`
* Now we our repo is properly setup to start contributing!

### Making changes
* The first thing you should do when you want to start on a new change is to create a new branch in your repo. In Git, branches are like effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug - no matter how big or how small - you should spawn a new branch to encapsulate your changes.
* First, we want to make sure our repo has the latest version of the original copy. Enter the command `git fetch upstream main` in your Git Bash shell.
* Next, we want to create a new branch. Enter the command `git checkout upstream/main -b YOUR_BRANCH_NAME`, where your branch name can be anything you want to call it.
    * For example, I usually name my branches something related to the change I'm working on. If I'm updating a beginner guide, I might call it `beginner`.

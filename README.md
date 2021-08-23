# How to contribute to PSR

Contributing to PSR can be as easy as answering questions about the runs in their respective Discord channel, or as complex as writing in depth guides. Every bit of help and every bit of knowledge shared helps.

## Writing Guides

In the past years an effort was put in streamlining all guides to be available at one place, that place being the [PSR GitHub Pages](https://pokemon-speedrunning.github.io/speedrun-routes/#/).  
GitHub Pages acts as a wiki replacement, allowing people to suggest changes that then need to be approved by selected reviewers before they go public.  

All pages are formated with GitHub flavored Markdown, to learn more about this, click [here](https://guides.github.com/features/mastering-markdown/).

### Setting up GitHub Desktop

* Download and install [Git (https://git-scm.com/downloads)](https://git-scm.com/downloads) for your appropriate OS.
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
    * To navigate to different folders in Git Bash, you can do `cd <folder_name>` to go into a folder, and `cd ..` to leave that folder.
    * You can also do `ls` to list the files in the current folder, or `pwd` to list the current directory you are in.
* Once here, we need to setup our repo to point to the original copy. Enter the command `git remote add upstream https://github.com/pokemon-speedrunning/speedrun-routes`
* Now our repo is properly setup to start contributing!

### Making changes
* The first thing you should do when you want to start on a new change is to create a new branch in your repo. In Git, branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug - no matter how big or how small - you should spawn a new branch to encapsulate your changes.
* First, we want to make sure our repo has the latest version of the original copy. Enter the command `git fetch upstream main` in your Git Bash shell.
    * You should be prompted with a window to sign in to your GitHub account. Click `Sign in with your browser` and log in.
* Next, we want to create a new branch. Enter the command `git checkout upstream/main -b YOUR_BRANCH_NAME`, where your branch name can be anything you want to call it.
    * For example, I usually name my branches something related to the change I'm working on. If I'm updating a beginner guide, I might call it `beginner`.
* Now that we're here, you can start making changes to the route files you downloaded locally.


### Setting up Git Information
* We need to setup some basic information for Git to communicate with GitHub.
* In your Git Bash shell, type `git config --global user.name "YOUR USENRAME"`, with the quotation marks included as part of the command.
* In your Git Bash shell, type `git config --global user.email you@example.com`, with your email address


### Creating a Pull Request
* In GitHub, a Pull Request represents a proposal to make some changes, and is usually reviewed and approved by someone else. To start, we need to upload our changes to our local fork of `speedrun-routes`.
* In your Git Bash shell, you can go and do a `git add <file_name>` for each file that you changed.
    * You can do the command `git status` to see a summary of what files you've made changes to in red
    * For example, if you changed `docs\gen-1\red-blue\catext\catch-em-all-classic\resources\pokemon-by-index.md`, you would do `git add docs\gen-1\red-blue\catext\catch-em-all-classic\resources\pokemon-by-index.md`
    * Note that you can tab complete file and folder names when typing this out.
    * You can do another `git status` and you should see the files you add in green.
* After you have added all the files you made changes to, we want to bundle them into a "commit". Do this by doing `git commit -m "YOUR DESCRIPTION HERE"`, where you give a short description of your changes. The quotation marks need to be part of this command.
    * For example, `git commit -m "Update Moon Rocket fight in Beginner Guide"`
* Then we want to push this commit back to GitHub. Do this by doing a `git push origin`.
* If you need to make more changes, you can go through these steps again to make changes to a file, do a `git add <file>`, `git commit -m "commit description"`, and `git push origin`.

* If you go back to your fork of speedrun-routes (https://github.com/<YOUR_GITHUB_NAME>/speedrun-routes) on your GitHub account and click the `branches` button, you should see your newly created branch listed there.
* Once you click the branch that you created, you should see a green "Compare & pull request" button at the top. Click that once you are ready to have your changes reviewed.

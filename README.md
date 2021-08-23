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

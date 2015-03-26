---
  tags: git, kids, environment-setup 
  languages: git
  level: 1
  type: environment-setup 
---

## Ready, set, git!

Git and GitHub are very important to the productivity of a developer. In a nutshell, they help you save all of your work and share it with other coders. You'll be learning a lot more about git and GitHub, but first let's *git* you all set up. (Forgive the pun!)

***If you are using a Chromebook, ignore these instructions. You will not be using Homebrew, and you completed the rest of these steps when you received your computer.***

***If you have Yosemite installed on your computer, you will need to manually install the command line tools first, by typing into terminal `xcode-select --install`***

###1. Set Up a GitHub Account

If you are looking at this on Learn, then you've already created an account on [GitHub](github.com). This first step was easy. 

###2. Download Homebrew

[Homebrew](http://brew.sh/.) is an awesome package manager that makes downloading lots of software really easy. Download Homebrew by entering:

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

into your command line. Once downloading is complete, enter `brew doctor` to make sure that you don't have any conflicts.

###3. Update Git

To see what your current version is, enter `git version` into your command line. To update and make sure you are using the most current version, enter `brew install git`.

###4. Git Tab Autocompletion

This is a super handy shortcut, we'll explain how this works more in depth, but git can autocomplete words for you.

`brew install bash-completion`

###5. Set Up a .gitconfig File

a `.gitconfig` file is a file that automatically logs you in to git through terminal. This will be incredibly helpful later on. 

* Make sure you're in the correct place before we create this file by entering the command `cd ~`.

* Enter `touch .gitconfig`, then `open .gitconfig`.

* Copy and paste the [Flatiron School Gitconfig](https://github.com/flatiron-school/dotfiles/blob/master/hs-gitconfig) into this file.

* You're going to need to replace some values with your own information from GitHub including:

  * The email address that you used to register for GitHub, where you see `<GITHUB EMAIL ADDRESS>`. You'll be replacing the whole thing, you don't want any of the < > angle brackets around the information you enter.

  * Your GitHub username and API token. This is how you find and generate API tokens on github.com:

    * On `https://github.com/settings/applications`, next to "Personal access tokens" you should see a button for "Generate new token". Click on it. 
    * Under "Token description" enter 'flatiron-school', then click the green "Generate token" button. 
    * Once the screen refreshes, you'll see a token (a series of randomly generated letters and numbers). Copy that and paste it into your .gitconfig file, replacing `<API token>`. (It's in a couple of places. Don't forget to replace the < > angle brackets, too.) 

* Now scroll all the way to the top of the file and replace the text `<YOUR_HOME_DIRECTORY>` with the name of your computer user. You can type `pwd` in terminal to see your computer username and figure out what you need to type in.

* Finally, you don't want any of the < > angle brackets around the things you replaced, like your email, username, or tokens, so make sure you replaced everything properly.

###6. Set Up a .gitignore File

A `.gitignore file` basically tells GitHub not to keep track of certain files.

* Make sure you are in the home directory. You should see this `~` in your command line. If you're not there, enter `cd ~`.

* Enter `touch .gitignore`, then `open .gitignore`.

* Copy and paste [Flatiron School's Gitignore](https://github.com/flatiron-school/dotfiles/blob/master/gitignore).

## Congrats! 
Phew! That was a lot of work, but now you are all set to use git and GitHub. Now, git 'er done!

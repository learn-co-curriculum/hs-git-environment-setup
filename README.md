---
  tags: git, kids, environment-setup 
  languages: git
  level: 1
  type: environment-setup 
---

## Ready, set, git!

Git and github are very important to the life of a developer. Essentially they help you save all of your work and share it with other coders. You'll be learning a lot more about git and github, but first let's get you set up.

###1. Set Up a Github Account

Go to (Github)[github.com], and fill out the form to create a username and click signup. You will need to then check your email to verify your new account by clicking a link in an email.

###2. Download Homebrew

[Homebrew](http://brew.sh/.) is an awesome package manager that makes downloading lots of software really easy. Download Homebrew by entering:

`ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"`

into your command line. Once downloading is complete, enter `brew doctor` to make sure you don't have any conflicts.

###3. Update Git

To see what your current version is, enter `git version` into your command line. To update and make sure we are using the most current version, enter `brew install git`. Once the download is complete, you'll want to open a new terminal tab, and reenter `git version` to compare and see if we have a new version number.

###4. Git Tab Autocompletion

This is a super handy shortcut, we'll explain how this works more in depth, but git can autocomplete words for you.

`brew install bash-completion`

###5. Set Up a .gitconfig File

a .gitconfig file is a file that automatically logs you in to git through terminal. This will be incredibly helpful later on. 

* Make sure you're in the correct place before we create this file: `cd ~`.

* Enter `touch .gitconfig` then `open .gitconfig` 

* Copy and paste the [Flatiron School Gitconfig](https://github.com/flatiron-school/dotfiles/blob/master/gitconfig) into this file

* You'll going to need to replace some values with your own information from Github including:

  * the email address that you used to register for github in three different places where you see `<github email address>`. You'll be replacing the whole thing - you don't want any of the < > angle brackets around the things you replace, like your email, username, or tokens.

  * Your github username and API token. This is how you find your API token on github.com:

    * Click settings in the top right corner (it's an icon that looks like a cog), it should bring up a menu on the left side. 
    * Click applications in that menu.
    * Click "Generate new token" next to "Personal access tokens". 
    * Enter 'flatiron-camp' under "Token description" then click the green "Generate token" button. 
    * Once it refreshes the screen and displays your token (a series of randomly generated letters and numbers), you'll want to copy that and paste it into your .gitconfig file. 

* Now scroll all the way to the top of the file and after [core], you'll want to replace the text <YOUR_HOME_DIRECTORY> with the name of your computer user. You can type pwd in terminal to figure out what you need to type in!

* Finally, you don't want any of the < > angle brackets around the things you replace, like your email, username, or tokens, so make sure you replaced everything properly.

###6. Set Up a Gitignore File

A .gitignore file basically tells Github to not keep track of certain files.

* Make sure you are in the home directory. You should see this `~`. 

* Enter `touch .gitconfig` then `open .gitconfig`

* Copy and paste [Flatiron School's Gitignore](https://github.com/flatiron-school/dotfiles/blob/master/gitignore).

###7. Set Up Github SSH Keys

An SSH key is how github can identify you without you having to enter your username and password every single time you want to push code up to the server. Github has a great online documention here.

* Make sure you are in the home directory. You should see this `~`. 

* See if you have a .ssh directory. Typing `ls -la` will show you all the hidden files. If you don't even have a .ssh directory, you can make it with `mkdir .ssh`

* Now we need to generate the SSH key, `ssh-keygen -t rsa -C "your_email@example.com"`. (Enter the same email address that you used to set up your github account between the quotation marks.)

* You'll get prompted to type the password to your computer twice (the letters won't actually show up when you type. Don't worry, it's just for security purposes).

* Once the SSH key generation is done, you'll enter `ssh-add ~/.ssh/id_rsa`

* Then `pbcopy < ~/.ssh/id_rsa.pub` which just adds your SSH key to your clipboard.

* Then you'll need to go to your github account online, and in the top right corner select account settings (the symbol with the cog). 

  * In the left toolbar, you'll select SSH Keys. Then you'll select Add SSH Key.

  * Enter the name "Github SSH" and then paste your SSH key into the key field. 

  * Click the green Add Key button.

  * Go back to terminal and verify that you successfully added the SSH key, `ssh -T git@github.com`. You should get back `Hi username! You've successfully authenticated, but GitHub does not provide shell access.`

## Congrats! 

Phew! That was a lot of work, but now you are all set to use git and github.
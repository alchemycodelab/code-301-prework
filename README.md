# Code 301 Pre-work: Intermediate Software Development

## Computer Setup

## Install VSCODE

If you haven't already, install [VSCode](https://code.visualstudio.com/). If you have used an advanced text editor like Sublime Text, or Atom, then VSCode will feel familiar to you. VSCode is free, open-source, cross-platform, and has a wide array of useful plug-ins available. Please use VSCode during Code 301. (If you are proficient with another text editor that you *love*, you may use that instead, but please note that your instructional team may not be able to assist with debugging any issues with your editor)

[VSCode's documentation](https://code.visualstudio.com/docs) is top-notch. Review it now to familiarize yourself with the basics. Make sure you're looking at the docs for the latest version. If you find that you are unable to call `code` in the terminal, you can enable shell commands through VSCOde by first opening it through your graphical desktop interface, and typeing `CMD + SHIFT + P` (or `CTRL + SHIFT + P` on Windows/Linux), and then type Shell Commands and selecting `Shell Command: Install 'code' in command in PATH` in the drop-down menu.

## Install Ryver (if you haven't already)

We use an app called Ryver to share resources, chat, make announcements and collaborate. 

You can either use the Ryver web app (codefellowspdx.ryver.com) or use the following link to download the installable app:

[Ryver Downloads](ryver.com/downloads/).

Once you have joined, add a nice profile picture of your lovely face. Then say hello in your class channel, and introduce yourself.

----

## Install Node

*Note* If you get an error while installing these packages such as "try again as root/administrator", you may need to use the `sudo` command to get administrator access. For example `sudo apt-get install nodejs`.

#### Linux instructions

  To install Node, open your Terminal, and copy and paste the following line, then hit Enter:

  `sudo apt-get install nodejs`

  If this did not work, try the following:

  `curl -sL https://deb.nodesource.com/setup_5.x | sudo -E bash -`

  It will churn away for a while, and then once it's done you can run the following command:

  `sudo apt-get install nodejs`

  If, once again, you did not achieve success, try [these instructions to build from source](https://gist.github.com/toastynerd/d3e563522977f6750c32).

  Finally, `sudo apt-get install npm`

#### Mac instructions

  If you took Code 201, you should already have Homebrew installed. If you have not, follow the guide on [this page](https://github.com/codefellows/code-201-prework/blob/master/prework/mac/2_homebrew.md#install-homebrew).

  To install Node, open your Terminal, and enter:

  `brew update && brew install node`

#### Windows instructions

  To install Node, go [here](https://nodejs.org/en/download/), and then download and run the Windows Installer. Make sure you do not deselect any of the Node components such as NPM during the installation.

### Verify the Node installation
Now let's verify that it is installed. Enter the following into your terminal:

`node -e 'console.log("works")'`

You should get a response that says "works". If not, try reinstalling Node again

----

## Install eslint and live-server Node packages

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your Terminal (Git Bash on Windows) and enter:

`npm -g i eslint live-server git-open`

You should see a lot of feedback as it installs.

### Verify the Node packages installation
Now let's verify that it is installed. Enter the following into your terminal:

`npm list -g --depth=0`

You should get a list back that includes `live-server` and `eslint`.

![](http://i.imgur.com/1ITioP1.png)

----

### What is this linter thing?

Linting is the process of running a program that will analyze code for potential errors. It is an important part of the quality assurance process.

> `lint` was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs) in C language source code. The term is now applied generically to tools that flag suspicious usage in software written in any computer language.

That means the linter is your friend! It will help you write syntactically correct code, so you can catch errors in your text editor, rather than having to hop over the browser, refresh your page, and search for errors. Faster feedback makes for happier developers (that's you!).

## Install linter and linter-eslint vscode extensions

In VSCode, chose the extension icon in the lefthand toolbar(or `View > Extensions` from the menu). Search for "ESLint" and click install.

It will prompt you to restart to load the extension. If you check afterwards, it should show the extension in the default installed list.

----

## Install PostgreSQL Database Software
*Please note that if you have a previously installed version of PostgreSQL on any operating system, you should be aware of any username and password that you've set for that installation. If you're unsure please uninstall and reinstall a fresh copy, which will also install the latest stable version.*

For both Windows and Linux users, please follow the default installation instructions taking care not to change values such as the default port numbers (You may be prompted to change them, but should also be given default values).

#### Windows

Follow the download and installation instructions on this page: [Installing Postgresql](http://www.postgresqltutorial.com/install-postgresql)

- Your **Default** database super user is: *postgres*
- You will be asked to enter and confirm a database password.
- **Be sure you document your default user and password**, as you will need them later in the course. We are working securely on your computer, so a simple password like `1234` will suffice, and there's no need to change the default user.

#### Linux

Follow the download and installation instructions on this page for your Linux distribution: [Installing Postgresql](https://www.postgresql.org/download/)

- If asked to provide or set a username and password, **be sure to document the username and password**, as you will need them later in the course.

#### MacOS

You should have already verified during the Node installation that you have Homebrew installed. Please see that section above for more details if not.

To install PostgreSQL, open your Terminal, and enter:
`brew update && brew install postgresql`

This will create a user for you, that matches your logged in user account. Run the `whoami` command in the terminal if you aren't sure what that is. This user has a blank password set as the default.

### Create some databases

Now that Postgres is installed, you should be able to create some databases to use in the class. From a command prompt, run these commands, utilizing the username and password form your set up. :

```
createdb -U USERNAME kilovolt
createdb -U USERNAME portfolio
```

These commands should run without an error. 
----

Congrats! You're all done. Well, except for your class-specific directory instructions :wink:

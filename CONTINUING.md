# Bootcamp: Part 2
## Intermediate Software Development

## Overview of tasks
- Customize Canvas
- Setup your laptop dev environment
  - install live-server
  - install postgres
- Codecademy jQuery course
- Sign up for Code Wars
  


## Customize Canvas (Canvas assignment)

You will not be able to complete this assignment until the Canvas course is published; the details for fulfilling this assignment are located there.

## Setup of Your Laptop Dev Environment (Canvas assignment)

Completion of the following setup tasks are all to be submitted in a single Canvas assignment. Keep a log of any errors or difficulties you encounter, and include those with your submission.

### ☐ Install live-server

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your Terminal (Git Bash on Windows) and enter:

`npm -g i live-server`

You should see a lot of feedback as it installs.

#### Verify the Node packages installation
Enter the following into your terminal:

`npm list -g --depth=0`

You should get a list back that includes `live-server`.

![](http://i.imgur.com/1ITioP1.png)


### ☐ Install PostgreSQL Database Software
*Please note that if you have a previously installed version of PostgreSQL on any operating system, you should be aware of any username and password that you've set for that installation. If you're unsure please uninstall and reinstall a fresh copy, which will also install the latest stable version. Additionally, if you are using a version before 9.5, you should uninstall and reinstall. You will be unable to complete certain labs if you are using version 9.4 or previous!*


For both Windows and Linux users, please follow the default installation instructions taking care not to change values such as the default port numbers (You may be prompted to change them, but should also be given default values).

#### Windows

*For reference, these instructions are taken from the following documentation: http://www.postgresqltutorial.com/install-postgresql/*

**NOTE: If you are running Windows 8 or 10, you need to create a Windows user with administrator role e.g., postgres and use this user to run the installation file.**

- Your **Default** database super user is: *postgres*
- You will be asked to enter and confirm a database password.
- **Be sure you document your default user and password**, as you will need them later in the course. We are working securely on your computer, so a simple password like `1234` will suffice, and there's no need to change the default user.

**There are three steps to complete the PostgreSQL installation**:

1. Download PostgreSQL installer for Windows
1. Install PostgreSQL
1. Verify the installation

**Downloading the installer**

- Go to the PostgreSQL [official website](http://www.postgresql.org/download/windows/).
- Click on the [download installer from EnterpriseDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads#windows). Choose the latest version to download. It takes a few minutes to complete the download.

**Installing**

Double click on the installer file. An installation wizard will appear and guide you through multiple steps where you can choose different options that you would like to have in PostgreSQL. For now, just select default values.

**Verify Installation**

When you installed PostgreSQL, the installer also installed some extra tools. One of them is psql (it may be called SQL Shell).

- Launch psql.
- When it prompts you for input, just hit enter to select default values until it asks for a password. You will put in the password you entered during installation.
- You should have a window that [looks like this](http://www.postgresqltutorial.com/wp-content/uploads/2012/08/psql.png).
- In this window, you can enter SQL statements, which must all end with semicolons. Congratulations, you've installed correctly!

**If you are having issues with the installation, please contact your instructor.**

#### Linux

*For reference, these instructions are taken from the following documentation: https://www.postgresql.org/download/*

- If asked to provide or set a username and password, **be sure to document the username and password**, as you will need them later in the course.
- `sudo apt-get install postgresql`
- You will be prompted with the message that a certain amount of disk space will be used and asked if this is OK. Type `y`, then hit enter.
- Several commands will automatically run, this may take a few minutes.
- **You will likely NOT be prompted for a default username or password.** You will need to set one in psql if this is the case.

**Verifying Installation And Setting A Password**
- You should be able to run the command `sudo -u postgres psql`. You will be asked for your administrator password - this is what you usually enter when you run `sudo` commands. This will log you into the psql prompt as the user postgres.
- You should now have a prompt that looks like `postgres=#`. You can run SQL commands from here, which must end in semicolons.
- If you were not prompted for a default user or password, we will set one using psql. If you type `\du`, you can get a list of users associated with PostgreSQL. You should see a single user, `postgres`. In order to give this user a password, enter the following command: `ALTER ROLE postgres PASSWORD 'your-password-here';`, replacing "your-password-here" with whatever you want it to be. Remember that your password must be wrapped in quotes. *Don't forget the semicolon*.
- If successful, you will receive the feedback `ALTER ROLE`.

**If you are having issues with installation, please contact your instructor.**

#### MacOS

You should have already verified during the Node installation that you have Homebrew installed. Please see that section above for more details if not.

To install PostgreSQL, open your Terminal, and enter:
`brew update && brew install postgresql`

This will create a user for you, that matches your logged in user account. Run the `whoami` command in the terminal if you aren't sure what that is. This user has a blank password set as the default.

Run this command: 
`brew services start postgresql`

#### ALL USERS: Startup and Create some databases

1. Login to psql.
  - For Mac, type `psql`.
    - If the response is, "Can't find database *yourUserName*", run `createdb -U yourUserName`, then run `psql` again.
  - For Windows, open up your psql program (SQL Shell)
  - For Linux, run `sudo -u postgres psql`
2. You should be at a prompt that looks like `postgres=#`
3. Enter the following command: `CREATE DATABASE kilovolt;`. *Note the semicolon. If you forget it, your prompt will go to a new line and look like* `postgres-#`. *This means you have an unterminated command and the prompt will just keep going to new lines until you enter a semicolon*.
  - You should receive the feedback "CREATE DATABASE".
4. Verify that your database was created by running `\l` (no semicolon). You should see a list of databases, including `kilovolt`. You should be able to connect to a database by running `\c DATABASE_NAME`, e.g. `\c kilovolt`.

## Codecademy: jQuery (Canvas assignment)

Complete all of the free portions of the [Codecademy course on jQuery](https://www.codecademy.com/en/tracks/jquery). The Canvas submission is a screenshot indicating that the course is complete.

## Sign up for Code Wars

Part of growing as a programmer is to practice, practice, practice. Throughout this course, there will be weekly Code Wars challenges. You are also expected to complete 15 pts worth of kata each week. The weekly challenge will be posted Monday morning and will be due by Friday night.

For now, sign up for Code Wars at [Code Wars](https://www.codewars.com/) and familiarize yourself with the interface: specifically, understand where to find your profile to see how many points (aka honor) you have and how to find challanges to work on (aka Kata).


---

Congrats! You're all done.

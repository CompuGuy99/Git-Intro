# Git: Useful for Self Tracking and Partnerships

**WARNING:** If you are not comfortable with your skill with Java at this time, you should not follow this guide. This guide is for more advanced coders who are comfortable with some extra time investment in their projects.

**WARNING 2:** Your Git can access public and private projects. Class code shall be always kept in private Git projects. If it is discovered you have class code in a public project, you may face disciplinary action for plagiarism, which is taken very seriously in the School of Computing.

- [Git: Useful for Self Tracking and Partnerships](#git-useful-for-self-tracking-and-partnerships)
  - [Introduction](#introduction)
  - [Getting Started on Windows](#getting-started-on-windows)
    - [Git for Windows](#git-for-windows)
      - [Select Components](#select-components)
      - [Default text editor](#default-text-editor)
      - [Name of initial branch in repositories](#name-of-initial-branch-in-repositories)
      - [Adjusting PATH environment variable](#adjusting-path-environment-variable)
      - [Choosing SSH executable](#choosing-ssh-executable)
      - [Choosing HTTPS transport backend](#choosing-https-transport-backend)
      - [Line Ending Conversions](#line-ending-conversions)
      - [Terminal Emulator](#terminal-emulator)
      - [Default behavior of `Git pull`](#default-behavior-of-git-pull)
      - [Credential Helper](#credential-helper)
      - [Extra options](#extra-options)
      - [Experimental options](#experimental-options)
      - [Installing](#installing)
  - [Git for macOS](#git-for-macos)
  - [Github for Desktop](#github-for-desktop)
    - [Getting Signed into Github Desktop](#getting-signed-into-github-desktop)
    - [Set up your first repo](#set-up-your-first-repo)
  - [Git in IntelliJ](#git-in-intellij)
    - [Connect to Github](#connect-to-github)
    - [Share Project on Github](#share-project-on-github)
  - [Collaboration](#collaboration)
    - [Important info about shared code in repos](#important-info-about-shared-code-in-repos)
    - [Sharing the Repo](#sharing-the-repo)
    - [Cloning the Repo](#cloning-the-repo)
    - [Push and Pull](#push-and-pull)
  - [Miscellaneous Items](#miscellaneous-items)
    - [Branches](#branches)
    - [Gradescope](#gradescope)
    - [`.gitignore`](#gitignore)
  - [Conclusion](#conclusion)
    - [Postscript](#postscript)

## Introduction

Git is a free and open-source version control system. You have probably heard of Github, which is a common implementation of Git, used by coders everywhere. Git allows us to save our work in the cloud while keeping track of who wrote what code and resolving conflicts between different code versions. The finer details are not super important for you to know right now. You will gain more experience in Git in CS 3500 if you are a CS major/minor.  
Git comes preinstalled on most Unix operating systems like Linux (all the distros I know about) and macOS (after a little setup). It does not come with Windows. This is a guide for getting you started with Git on Windows and macOS. Linux is not included due to few students who use this and the fact that git is already installed on most Linux distros. Windows is included first as there is some more setup required for this OS over macOS and Linux.

## Getting Started on Windows

We need to install a couple programs on Windows in order to make Git usable, especially in IDEs that use git for version control. We need to have the basic installation, and a program I highly recommend.

### Git for Windows

Windows does not come with Git preinstalled. At minimum, you will need to install the Git-scm client from the developers. Go to <https://Git-scm.com/download/win> and download the Standalone Installer for 64-bit Windows. Read (or don't and sell your soul) the terms and conditions and agree to them. For your intents and purposes any defaults that are listed on the installer are fine, with a couple exceptions. I do recommend a few changes to settings, all of which will be discussed here. Once this is installed, any program that uses git for version control will be able to perform all the necessary operations.

#### Select Components

No changes needed here. You will receive a bash that can be used for Git. Learning the Git Command Line Interface can be a very valuable skill, especially if you do low level programming (C as an example) or work a lot on Linux. You will also receive a GUI Program that isn't very intuitive which is why I recommend another visual tool that I will discuss later.

#### Default text editor

Shows you different choices for the various text editors available at the time the installer is running. Notepad and Notepad++ are my two choices, where Notepad++ is favored. Notepad is default on Windows, Notepad++ is another great notepad with some great coding features built in. If you install Notepad++ while the installer is running, you will need to leave this setup and come back to refresh the list. I recommend you run the Notepad++ installer before even running the Git installer if you want to use it. If you want to work with another program, you may but you may just not end up using it much due to the program we will use and install later.

#### Name of initial branch in repositories

"Let Git decide" is default here. Git currently defaults to master when a Git repository is initialized. Plans are in place to change this to a more inclusive title due to connections with slavery according to some. This is up to you, but in the future, the default will likely be changed to main.

#### Adjusting PATH environment variable

Use the recommended option. This will allow you to use any terminal to do Git command line. I don't recommend the optional Unix tools. You won't need them at this time. This can be changed in the future.

#### Choosing SSH executable

I recommend you use the bundled SSH exe from Git. OpenSSH is great for what you need it for.

#### Choosing HTTPS transport backend

Go with default here. You don't need the extra features from the Windows Secure Channel Library until you're in the workforce.

#### Line Ending Conversions

Use the default setting. This will make sure you can edit on both Windows and any Unix operating system (Linux, macOS).

#### Terminal Emulator

Either one is good here. If you choose to use the Git bash, it just changes what window your Git bash opens in, MinTTY or Command Prompt (or whatever default terminal is set up on your computer).

#### Default behavior of `Git pull`

Anything but "Only ever fast-forward" is good here. You want to be able to save your changes onto the current branch whenever you pull someone else's work. I've only ever used the Default setting.

#### Credential Helper

Use Git Credential Manager. You'll thank me later when we get to logging into your Github.

#### Extra options

No reason to change any options here.

#### Experimental options

Don't add anything here. You don't need it.

#### Installing

After all those options (exhausting, right?), it will install Git onto your Windows computer and allow all programs that have integration with Git to properly run. You're done with this step.

## Git for macOS

macOS has a command line call for Git but it's just a shell for installing the full features on the command line. Running the command `Git` in your macOS terminal will result in a message that says  
`note: install required for command line developer tools`   followed by a window prompt that asks if you want to install the developer tools so Git can run on macOS in the Terminal (and in other programs that use that executable). You should accept that so you can run `Git` in the command line. Make sure you agree to sell your soul in the terms and conditions for the command line developer tools if you do choose to install. It may or may not be necessary, but I recommend having the command line tools available. Once this is done, you should be able to move on to the next step where we rejoin your Windows cohort.

## Github for Desktop

I mentioned above that you will get a GUI program from Git to use on Windows. I don't recommend this as it won't be easy to publish your local Git repository to Github. Instead, I recommend a program from Github called Desktop. It is a graphical program that allows you to manage any Git repository that is initialized on your computer. It is also so much easier to use the the Git GUI program that comes with Git for Windows. I find it very handy for my Git repositories that don't have well built Git features in them (IntelliJ has a wonderful interface. This is a useful program no matter the language you use.).

Go to <https://desktop.github.com> and download the exe or zip depending on your OS. (Linux, you are on your own for this one. I looked up how to install on Ubuntu and there are shell scripts that people have made. Keep in mind that this does not connote official support by Github) Running on Windows, the installer will run automatically and run the program immediately upon completion. For macOS, once the zip is downloaded, unzip it and run the executable within. More detailed instructions on installing and setting up Github Desktop are contained at [this link](https://docs.Github.com/en/desktop/installing-and-configuring-Github-desktop/overview/getting-started-with-Github-desktop).

### Getting Signed into Github Desktop

Upon first installation, Github Desktop will likely ask you to sign into your Github account automatically. In the case it does not do that, We will need to sign in ourselves. On Windows, open the "File" menu in the top left and choose "Options". On macOS, the same can be achieved by selecting the program dropdown from the menu bar and selecting "Preferences".

Once this window is open, select the "Accounts" pane from the left-hand side. You will want to select the sign in button for Github.com instead of Github Enterprise. You should have your account set up before this, otherwise, set up an account now.

### Set up your first repo

Now that you're signed in, you can initialize a Git repository on your machine in the location you choose, (I recommend the project folder of your CS code but you can also set it to your entire IntelliJ Project folder). Once the repository is initialized, you can publish it to Github. **REMEMBER:** Class code must be kept private or you risk disciplinary action by the School of Computing if you are discovered with class code in a public repo. Below is a picture of my Github Repos page where I have all my repos. All of them are private. If the repo is public, that Private tag won't be there.

![Private Repos](Screenshot/Github%20Private%20Repos.png)

After publishing (which sets up the repo on Github's servers), you're all set. I recommend you commit and push changes to your code after every session of coding you do, at a bare minimum. Multi-hour sessions will benefit from more frequent commits. Make sure you describe your changes well!

## Git in IntelliJ

When this guide was originally written, it was designed to be used for Eclipse. Now that CS 1420 teaches using IntelliJ, this section is added to allow students to use the features of IntelliJ to use Version Control on their code. IntelliJ uses Github's third party authorization system to connect an IntelliJ installation to a Github account. This is fabulous and allows us to use IntelliJ to manage our repos. This section of the guide is dedicated to getting you set up on IntelliJ with your repo.

### Connect to Github

There are a variety of ways to get your project on Github. This is just one way. First you need to connect your IntelliJ to Github. Go into settings with `Ctrl+Alt+S` on Windows or `Cmd+,` on macOS. On the left find the sidebar and expand **Version Control**.

![IntelliJ Settings for Github](Screenshot/IntelliJ%20VCS%20Settings.png)

Select the Github settings and you should see something similar to the following image:

![IntelliJ Github Account View](Screenshot/IntelliJ%20Github%20Account.png)

Click the plus icon, and select "Login via Github" and follow the steps shown on your web browser. This will log you in through Github. Once done, you should see something similar to this on the settings screen when you switch back to your IntelliJ window.

![IntelliJ Github Signed In](Screenshot/IntelliJ%20Github%20Account%20Signed%20In.png)

You are now able to use your Github with IntelliJ.

### Share Project on Github

Let's share a project on Github with this! Close your settings and find the `VCS` or `Git` context menu. Select the option to **Share Project on Github** which should be toward the bottom of the list. The following popup will show:

![Share Project Settings](Screenshot/IntelliJ%20Share%20Project%20on%20Github.png)

Choose the repository name that best describes what is contained in your project (I choose to name it with a class number and semester. This generally matches how I name the projects. No whitespace characters are allowed here so I use dashes to separate words.). Mark whether this project is private or not (**This must be marked for class code or you may be subject to disciplinary action**) and provide a description for the repo (optional). Click Share. IntelliJ will spend a little bit of time setting up Git settings on your project with some custom stuff that will be helpful to you. The following popup will show:

<img src="Screenshot/IntelliJ%20Initial%20Commit%20Files.png" height="500">

This allows you to choose what to publish as the first commit. I don't recommend you change anything here unless you want a unique initial commit message. IntelliJ will take care of the rest for you. That's it! You now can use Git to manage your IntelliJ project.

## Collaboration

You are done with setting up Version Control for a project. This section discusses collaboration with multiple individuals in the Same Github Repo. If it is discovered you have shared a Github repo containing code for individual class work with another individual, you will be referred for Academic Misconduct. The details are on the syllabus for this policy.

When you need to work on the same code as a pair, do not follow the recommendation of putting your entire CS 1420 IntelliJ project into a Git repo. I would follow Dr Jensen's advice of adding your Final Project code in a separate project and initializing a Git repo there. **Important: Only one partner should initialize this repo, as this repo will be shared between the two of you.**

### Important info about shared code in repos

The partner that initializes the repo and publishes the repo to Github *in a private repo* will also handle the sharing of the repo with the other partner. Both partners are required to have a Github account in order properly share repos.

### Sharing the Repo

Navigate to your Github home page and select the repo to be shared. Your code in all the folders and other misc files you have uploaded to Github will appear as organized on the system that initialized the repository. Navigate to the repo settings (shown by the cog on the upper bar above the files), and select the collaborators view. You will probably need to enter your password again to enter "sudo mode". You will see the area where collaborators are shown. You want to add a collaborator, by the name your partner supplied to Github, their username, or their email as supplied to Github. (I recommend username or email as these will be guaranteed to find your partner vs names which can be common). Once you have added them, they will be able to accept and clone the repository to their machine.

### Cloning the Repo

Cloning is something you will do with every Git repo you do not create and init. You will likely do this more often than starting a new project locally. Github Desktop makes cloning quite easy. When navigating between repositories you have, select the "Add" button, and then "Clone repository". Select the repository you are cloning and set the path of where the repository will be located. If the directory you select is non-empty, Github Desktop will force create a folder for your new repository. If you are cloning an IntelliJ project, I recommend you select your Workspace folder (IdeaProject is the name of the default if you did not change it) as the project will be then downloaded and IntelliJ should automatically see the project you cloned. (Don't expect this to work the first try, this is new of course.)

If you have done this properly and IntelliJ still hasn't found it, you may need to import an existing project into IntelliJ. Select File &rarr; Import in IntelliJ. In the import wizard, select Existing Projects into Workspace, found under the General folder. Select the root directory as your IntelliJ Workpsace folder. The projects that are already part of the workspace are greyed out, but any ones that aren't part of the workspace can be selected and added.

### Push and Pull

These are the two major operations you will do as part of using git for your code. To Push in git means to take the local files (like the code you have written) and making that the most recent update on your Github repo. This only works when you have made changes on your computer that aren't already on Github. Before you can actually push to Github, you need to commit, which tells your local repository that these changes are now part of the history of the repository. Make sure to specify what changes you made in the description of the commit (bottom left corner of the Github Desktop window). Make a commit and push every time you are done with coding on your computer.

![Changes to Commit](Screenshot/Github%20Desktop%20Local%20Changes%20to%20Commit.png)
![Commits to Push](Screenshot/Github%20Desktop%20Commit%20to%20Push.png)

To Pull in git means you are pulling changes from the Github repo to your local repository. This assumes Github has more recent changes to the code than your local repository. This is a good idea to do right before beginning of a session. Github Desktop will occasionally check if there are changes on Github that aren't on your computer. This is called "fetch". It's always a good idea to do a fetch (which compares your local repo to Github) to see if any changes exist, even if Github Desktop doesn't see any immediately.

![Commits to Pull](Screenshot/Github%20Desktop%20Commits%20to%20Pull.png)
![Default View Screen](Screenshot/Github%20Desktop%20Nothing%20to%20Push%20or%20Pull.png)

**BEWARE:** Trying to push changed code from two different computers to Github will likely result in a merge conflict. Should this happen to you, see a TA immediately. They will be able to help.

## Miscellaneous Items

Once you have the repo set up on both your computers, you're done! The following items are just a discussion of different features that may be useful in the future. None of these items are required for the basic functionality you would need for your pair programming or for this class in general.

### Branches

More things you can do are branches to your code. You don't need to worry about branches as part of your Pair programming, as all the work will be done on one computer at a time. When multiple collaborators are working on the same code at one time on different local repos, branches become extraordinarily useful. On your local repo, you will create a branch for your changes to the code. This branch will now no longer change what's contained in the 'master' or 'main' branch but store all the changes on the side. When you are done, the most common method for merging the changes with the main branch is to create a pull request. A Pull request essentially says hey I updated code off to the side and I want the owner or major collaborator of the Github repo to merge it. You are going to be that person on your own code or on code you collaborate on most of the time. Once a pull request is made, you or another can review the pull request and merge it with the 'main' branch.

### Gradescope

Did you know Gradescope has integrations with Github? That's right! You can actually submit your code from a Github repo straight to Gradescope. There is a large caveat to this. You will submit the entire repository, miscellaneous files and all to the submission. CS 3500 is a class for CS Majors and Minors that frequently uses Github to keep track of version control as well as help the instructors track misconduct through the way students are versioning their code. You will likely use the Github integration with Gradescope in that class. **Do not submit an entire IntelliJ Project onto Gradescope unless explicitly told to.**

For the intent and purpose of this class, continue submitting your code as normal.

### `.gitignore`

This is an extremely useful file extension that Git reads to exclude files and folders from a repo. Many IDEs with Git integration will create their own `.gitignore` files that are especially relevant to the files generated through use of that specific IDE. Visual Studio (not Visual Studio Code) is a great example of this, which you will likely use in CS 3500 for C# development.

I would recommend googling syntax for a `.gitignore` file and experimenting on your own with this. Most repos should have this so elements that are unnecessary for the contents of the repo are ignored.

*Caution*: Once a file/folder is committed and pushed as part of a repo, it cannot be removed simply by placing the file/folder as an element of the `.gitignore`. It must be removed (deprecated is the term Git uses for this) from the repo in a commit and then re-added (especially if it's a necessary folder for the project on the client side). then `.gitignore` will not track changes and commit to the repo.

## Conclusion

Whether you are working alone or working with a partner, you may find Git useful in keeping track of code and being able to roll back code to a previous version if you break something. The power of Git is many of the features that were not discussed here. As you work with Git, you will find those useful portions and be able to expand your capability in coding. Employers also love to see when a prospective Software Engineer knows their Git. Happy Coding!

### Postscript

Please ask me any questions if you need any extra help beyond the guide. Also, any feedback you have will help make this guide better for the future.

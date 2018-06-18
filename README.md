# Deploy on Day One

## Contents

|Section                            |
|-----------------------------------|
|[History](#history)                |
|[Assignment](#assignment)          |
|[Requirements](#requirements)      |
|[File Structure](#structure)       |
|[Getting Started](#getting-started)|
|[Next Steps](#next-steps)          |
|[Final Steps](#final-steps)        |
|[Resources](#resources)            |
|[Issues](#issues)                  |

## History

Welcome to VFA Training with Flatiron School! At Flatiron School, every semester, we create student index pages to help in the process of getting to know each other. An index page looks something like [this](http://students.flatironschool.com/). Links from this page go to individual profiles, which look like [this](http://students.flatironschool.com/students/lauraconwill.html). You will be making and deploying an index page that contains info for all of the fellows at your current table.

## Assignment

Your assignment is to create a profile page for someone sitting at your table. By the end of this project, every fellow should have a profile for themselves that was created by someone else and every fellow should have created a profile for someone else. If you're sitting at a table of four, it might be easiest to pair up. If you're sitting at a table of three, it might be easiest to create the profile of the fellow clockwise to you. If you're sitting at a... well, you get the picture.

Now if you're anything like me, you might be freaking out and wondering, "Am I making a webapp?!?!" The answer is no. You're just working with HTML and file structures. You don't need to know Rails, JavaScript, or even Ruby for this project. No need to freak out. Calm down! Seriously, you're making the rest of us nervous!!!

You'll have about three hours to complete the first section of this lab. Use that time to get to know your table, get familiar with git workflows, and re-familiarizing yourself with HTML. If you feel stuck, ask your Flatiron School trainer or any of the TAs for help. **Keep in mind everyone in your table will be pushing to the same repository.**  Think about using a workflow with your teammates that will minimize conflicts.

## Requirements

Please collect the following content from your assigned classmate for their profile. This content doesn't have to be finalized, but you need something. They'll be using this content as the project evolves for their resume and other profiles online.

* Name
* Github Username
* Blog Url (if they don't already have a blog, we'll set one up at their-github-username.github.io)
* Tagline
* Profile Picture (something semi-professional, a headshot, of a good reusable size that can be easily cropped)
* Background Picture
* Favorite Websites
* Previous Work Experience
* Short Bio
* Twitter URL
* LinkedIn URL
* Education

### Background and Profile Images

**Instead of manually adding image files to our project, we will be uploading our images to imgur.com (a free image hosting site), and linking to the images respective URLs in our css file.**

1. Select your cover and profile pictures
1. Upload your cover and profile pictures to imgur (they should be jpg or png files):
  * Head to <a href="http://imgur.com/" target="_blank">imgur.com</a>
  * click on the blue 'Upload images' button on the top of the page
  * You can then drag and drop the cover, and profile images to that page, or use the 'browse your computer option to find them manually'
  * Click on the 'Start Upload' button to upload the images
  * If you hover over the top right of each image, you should see a link with 3 little dots on the left, hover over those dots and copy the *direct link* URL and paste that somewhere safe. *You will need to use these links in the `css/styles.css` file to be able to display the images in your profile*.
2. Share links to your cover and profile images with your partner

## Structure

The structure of this project looks something like this:

```text
├── assets
│   └── fonts
│       └── font files
├── css
│   ├── fonts.css
│   ├── normalize.css
│   └── style.css
├── students
│   ├── student_name1.html
│   └── student_name2.html
├── index.html
└── README.md
```

### Files you will need to alter:

* `index.html`
* `css/styles.css`

### Files you will need to add:

* You'll be adding one HTML file to the `students` directory

## Getting Started

### Group Logistics

* Figure out who is going to write whose profile.
* ![fork](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/fork.png)
* Have one person at your table [fork](https://help.github.com/articles/fork-a-repo) this repo.
* Git clone the forked repo to that person's machine. Ensure that your index.html file has the same amount of ```<div class="student-card">``` elements (surrounded by the 'begin student' and 'end student' comments) as you have persons on your team. We have provided four by default, but you should either remove these or copy/paste to reflect the correct amount of people on your team. Assign individuals to specific ```<div class="student-card">``` elements (order matters!).
* Once the count is accurate, the person who forked the repo must git [add](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files), [commit](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes), and [push](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes) to your remote master.
* Next, the person who forked the repo must add all team members as collaborators. Learn more about that [here](https://help.github.com/articles/adding-collaborators-to-a-personal-repository/).
* Following, this person should then send the link to their fork to everyone sitting at their table.
* ![clone](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/clone.png)
* Everyone at the table should then [clone](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository) this forked repo.

### Individual Instructions

Now that you have the repo, you'll want to get into it. Remember [cd](http://linux.about.com/od/commands/a/Example-Uses-Of-The-Command-Cd.htm)? When you type `pwd` into your terminal and the last part of the text that gets returned is `deploy-on-day-1...`, you're in the right place. **NOTE In all the hypothetical examples, we're writing a profile for Zoe Perez.**

Take a look at `index.html` and `students/example-name.html` in the browser. You can do this many ways but one is by opening finder and right clicking on `index.html`. Then click on "Open with" then the name of your favorite browser.

#### Make a New Branch

1. From the root directory, [checkout a new branch](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching). This new branch's name should be the name of the student whose profile you're going to create.
  * For instance, the branch would be titled `zoe-perez`.
  * Note: The `master` branch of a project is NEVER a place to do any work. `master` is considered the build and you never break the build. So make sure you are not working or committing to the `master` branch.

2. If you haven't already, switch to the branch you created. To make sure you're where you need to be, type `git branch` in your terminal. It should return the name of your assigned student emphazised with an asterisk and master.
  * For instance, typing `pwd` in the terminal would return:

```text
  master
* zoe-perez
```

#### Add Profile

1. In this new branch, make a new HTML file in the `students` directory. The file name should be the name of the fellow you're creating the profile for.
  * For instance, we would create a file `zoe-perez.html` in the main `students` directory.
2. Add all the collected information about your partner (links, bio, etc.)
  * Use any of the example `students/student-name.html` files for reference. In fact, feel free to copy as much of the HTML from one of the examples into the new file you've created

#### Add Images

1. Still in this branch you created, open the `css/styles.css` file
2. Check out the student profile and cover image css in the file to see what you'll need to do.

#### Add To The Index

1. Still in this branch you created, open up `index.html`
2. Copy one of the existing `div`s to make a new slot for your partner. Add in your partner's information.
3. Re-use the profile image from the profile page and link to the profile page


#### Stage and Commit Changes

1. Once you're happy with the profile you've created and the changes you've made to the index page, type [git status](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Checking-the-Status-of-Your-Files). The file you've altered, `index.html`, should appear in the "Tracked Files" section and the files you've created should appear in the "Untracked Files" section.

2. You'll want to [add](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files) then [commit](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes) these changes with a message.

3. If you type `git status`, you should see "nothing to commit, working directory clean". If you type `git remote -v`, it should display something like:

|remote | url                                                               |         |
|-------|-------------------------------------------------------------------|---------|
|origin |https://github.com/table-member's-github-name/deploy-on-day-1...git| (fetch) |
|origin |https://github.com/table-member's-github-name/deploy-on-day-1...git| (push)  |

#### Push Up Your Branch

1. Now it's time to [push](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes) to a remote branch. This remote branch doesn't exist yet, you're going to create it by pushing.
  * **NOTE: Do not push to master. Do not type anything that contains the word master!**
  * You're going to push to a branch that is the same name as your local branch.
    * For instance, if we're on the branch zoe-perez, we're going to push to zoe-perez.

2. To confirm this push worked you can do two things:
  * Type ```git branch -a``` which will show the remote branch on github.com you just created when you pushed.
  * You could also go to the url of the forked repo. Notice the section that looks like ![branches](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/branches.png). You should be able to click on that arrow and to see a dropdown. From this dropdown, select the name of the branch you've been working on.

## Next Steps

### Group Logistics

Since your table is going to be deploying a single web page with all of your tables profiles, you'll need to merge every branch that your table created into a single branch. This branch will contain every profile from your table. The process of merging these branches may result in merge conflicts in `index.html` and possibly elsewhere. That's totally okay and expected!

Think about the best way to merge all the branches together. Should one person do it? Should everyone do it in order? Should you merge into a prexisting branch, like `master`, or create a totally new branch? You might be wondering what the best answer is but there isn't a "best answer", just decide on a strategy and go for it!

### Merge Conflicts

When [merging](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merging), [merge conflicts](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merge-Conflicts) can happen. Generally they look like:

```text
> git branch
  └── master
> git merge zoe-perez
  └── Auto-merging index.html
  └── CONFLICT (content): Merge conflict in index.html
  └── Automatic merge failed; fix conflicts and then commit the result.
```

This just means that you will have to open the files where there are merge conflicts, in this case `index.html`, and find the part that looks like:

```text
<<<<<<< HEAD
content here
=======
other content here
>>>>>>> zoe-perez
```

Just decide which one you want to keep or if you want to keep both. Then delete the parts you don't want and delete the `<<<<HEAD`, `======`, and `>>>>>` parts.  In the process of trying to merge two files, you may notice that chunks of html end up in the wrong place on the page, and there is a chance you may need to move things around to be in the proper order again.  If you'd like a visual reference of what your index page looks like, you can also run `open index.html` from your command line, in order to view the current state of your page in the browser.

Remember, if you have multiple files with merge conflicts, you'll have to repeat this process with each file. Once you're done selecting which code to retain, `git add` and `git commit` these changes. Now when you type `git status`, your terminal should not display "You have unmerged paths."

## Final Steps

Once every profile is on a single branch that is hosted remotely, it's time to deploy your table's profile page! This will look like the sample link at the top of this lesson, but with the cards/profiles for your group only.

 - In your browser, navigate to the main github repo for your table.
 - At the top of the page, click on the `Settings` tab (the one with the gear symbol)
 - Once on the Settings page, scroll down to the `GitHub Pages` section
 - Under "Source," choose "master branch" and click "Save."
 - Navigate to ` http://username.github.io/repository_name`, and have a look at your page!

When you have fixed any errors and are ready to share, post your link in Slack so the rest of the class can read who you are!

Congratulations, you've completed the workshop!


## Resources

* Git Step Resources
  * [Forking a Repo](https://help.github.com/articles/fork-a-repo)
  * [Cloning a Repo](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository)
  * [Branching](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching)
  * [Adding](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files)
  * [Committing Changes](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes)
  * [Pushing to Remote Branches](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes)
  * [Merging Branches](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merging)
  * [Submitting a Pull Request](https://help.github.com/articles/using-pull-requests#sending-the-pull-request)
* Git Workflow Resources
  * [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
  * [Git Workflow](https://github.com/diaspora/diaspora/wiki/Git-Workflow)
  * [Git Rebase Workflow Explained](http://mettadore.com/analysis/a-simple-git-rebase-workflow-explained/)
  * [How GitHub uses GitHub to Build GitHub](http://zachholman.com/talk/how-github-uses-github-to-build-github)
  * [GitHub Workflow for Submitting Pull Requests](https://openshift.redhat.com/community/wiki/github-workflow-for-submitting-pull-requests)
* Deploying to GitHub Pages
    * [Documentation for how to deploy to GitHub Pages (choose "Project Site" rather than "User or Organization Site")](https://pages.github.com/)

## Issues

A common issue is not being able to authenticate with GitHub. You need to use HTTPS/SSH correctly when cloning the repository in order to be authenticated with GitHub. Checkout and follow:

* [Setting Up Git](https://help.github.com/articles/set-up-git)
* [HTTPS Cloning Errors](https://help.github.com/articles/https-cloning-errors)
* [Setting Up SSH](https://help.github.com/articles/generating-ssh-keys)

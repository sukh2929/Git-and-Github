---
layout: post
---
Git and GitHub - In a simple way\!

Why would you care?

Do you want to develop the code? Do you want to manage it? You want to know when and what changes you made? Do you want to collaborate with your team? Do you want to see and review what others are developing? Do you want to maintain history?

Good news\! This all can be done using Git and GitHub\!\!

What are Git and GitHub?

Git -

> Git is an extremely popular version control system that gives you the power to manage, review and restore earlier versions of saved programs/codes of your project. It is installed and maintained on your local machine.

GitHub -

It is a cloud-based service that uses git to stores the code that you developed in your local machine to the cloud which can be shared, reviewed by the team or other people. The user interface is extremely intuitive and provides programmers with built-in control and task-management tools.

Now, let’s dig a little deep into some Terminologies used in Git and Github:

1.  > Snapshots
    
    1.  > This is how your code looks at a certain time

2.  > Repo
    
    1.  > Also called a repository
    
    2.  > It is a collection of all the files and history of those files or basically contains all of the commits
    
    3.  > A software project can be one repo having submodules or in a complex case, it can be divided into multiple repos.

3.  > Branch
    
    1.  > A branch is a lightweight pointer to one of the commits
    
    2.  > The default branch name in git is master
    
    3.  > Every time there is a new commit, the branch pointer moves forward.
    
    4.  > There can be many, many branches. For example, for a software project, branches can be staging, development, and production.

4.  > Commits
    
    1.  > It is used to take the snapshot of your code
    
    2.  > It contains three pieces of info
        
        1.  > Info about how files changed from the previous snapshot
        
        2.  > A reference to the previous commit called parent commit
        
        3.  > A hash code to uniquely identify the commit

5.  > Merging
    
    1.  > People work on different branches and finally merge the changes in the main branch. For example, feature-1 branch has new code which needs to be deployed onto the production server then a person can merge this feature-1 branch into the master which will be finally deployed onto the production server.

GitHub Features

1.  > People can push a local repository created by git to their or organization’s GitHub account. Repo on GitHub is called remote repo. Also, They can pull remote repo to a local directory. So, basically, Github hosts remote repositories for a better team collaboration

2.  > It enables you to use git operations via UI and also review branch merges via pull requests. Pull requests are raised when a person wants to merge one branch into another. for e.g merging the development branch into production can be done by creating PR so that the code owner can review the new changes.

3.  > New features like GitHub actions allow you to do automate the CICD process.

Now let’s see these terms and relate them :

1.  > Local repository(present in your local system) - This image shows local repo “Labzen” and the default branch “main”

![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image3.png)

2.  > Remote Repository(present on Github.com or enterprise) with default branch “main”

> ![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image5.png)

Now, let’s see the high level working of git and Github

1.  > Create a repo on the local system/copy(clone in git world) repo from remote(that is from GIthub.com)

2.  > Make some modifications different files as per your requirement

3.  > Add those files - add the changes in the staging area (where you would keep the files before committing the changes)

4.  > Commit those files - add the changes in the repository (that is new snapshot of your change is captured in the history)

5.  > Push those files - push the changes to remote so that your remote and local is synced

6.  > Merge those files on github.com when collaborating with your team

Let’s us actually implement the steps:

1.  > Create a repo on the local system/copy(clone in git world) repo from remote(that is from GIthub.com)

<!-- end list -->

1)  > I have created a repo on Github.com

![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image8.gif)

2)  > Copy the remote repo so that we can clone it on the local machine

![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image6.gif)

3)  > Clone to remote repo to local machine

> ![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image2.png)

7.  > Make some modifications different files as per your requirement

> I am making changes to the README.md file. Open any editor to edit the file.

8.  > Add those files

Go to root of your repo

![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image1.png)

9.  > Add, Commit and Push the changes from local repo to remote repo

![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image7.gif)

10. > Check on GIthub.com to see the changes

> ![]({{ site.url }}{{ site.baseurl }}/assets/img/2021-03-28-Git-and-Github---In-a-simple-way/media/image4.png)

Ahaaa\! You are done\!

Your first repo is created. Congratulations\!

Git & GitHub user guide

1.  > Installation and configuration
    
    1.  > [<span class="underline">Installation</span>](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
    
    2.  > [<span class="underline">Configuration</span>](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
    
    3.  > To authenticate with the organization’s GitHub account, you need to add an ssh key to the GitHub account. Follow this [<span class="underline">process</span>](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

2.  > Create repo
    
    1.  > Create and enter into your project directory and use the command “git init“.This will create a “.git” directory inside your project folder which will have all the git files for .e.g logs/index
    
    2.  > For e.g.
        
        1.  > mkdir git\_learn
        
        2.  > cd git\_learn
        
        3.  > git init
    
    3.  > we need to set up the remote repo
        
        1.  > Command - “git remote add origin [<span class="underline">git@GitHub.com</span>](mailto:git@github.com):{username}/git\_learn”
    
    4.  > Push the local branch to remote
        
        1.  > Command ‘git push -u origin master’
        
        2.  > Git push is used to push local changes to the remote repo
        
        3.  > Git pull is used to pull remote repo changes to your local repo for e.g. changes which are made by other team members.

3.  > Add files
    
    1.  > Once you add some files to the project they will be counted as untracked files until they are not added to git
    
    2.  > .gitignore file is used to ignore the directory and files which we don’t want to add to the git
    
    3.  > “git add {file\_name}/{directory}” is used to add files/directories.You can also use a relative path.
    
    4.  > Now, these files are added but they are still not committed. Currently, git started just tracking them.

4.  > Commit Files
    
    1.  > To commit the file we use “git commit -m ‘commit message’ ”
    
    2.  > Now we took the snapshot of our code. So, how many commits we made, we can always revert to this commit and start work from this commit.
    
    3.  > Git commit messages are about why this commit was made. This is helpful for reviews.
    
    4.  > Now will use git push again to push changes to remote
        
        1.  > git push -u origin master

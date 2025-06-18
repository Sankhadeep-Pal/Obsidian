# [Git & Git hub tutorial](https://www.youtube.com/watch?v=Ez8F0nW6S-w&t=2693s)

## GitHub 
Website that allows developers to store their code using Git.
[Click here](https://github.com/) to start with GitHub.

### Fork
A **fork** is a new repo that shares code and visible settings from original *upstream* repo.
**Fork** is a rough copy that we use to change anything to code in our own account. To change in the original *upstream* repo we create [[Pull Request|PR]].

## [[git-cheat-sheet-education.pdf|Git]]
Git is a [[version control system]].
It is widely used because:

- Popular

- Free & open source

- Fast and scale-able

---

### Start with Git
Firstly we have to [download](https://git-scm.com/) Git in our system.
Some operating system can have Git installed out of the box, like:

- Linux

- Mac OS

 But some OS doesn't include Git. so, we have to download manually.
 
 To check that you have Git installed type:
```
 git --version
```

---

### Configuring Git
Configuring user information used across all local repositories

- set a name that is identifiable for credit when review version history
```
 git config --global user.name “[firstname lastname]”
```

- set an email address that will be associated with each history marker
```
 git config --global user.email “[valid-email]”
```

- set automatic command line coloring for Git for easy reviewing
```
 git config --global color.ui auto
```

To see & verify our inserted data type:
```
git config --list
```

---

### Basic Git commands
Some basic commands that we use in daily basis.

- ***Clone:*** Cloning a repository in our local system.
```
git clone <--some_link-->
```

- ***Status:*** Display the status of the code.
```
git status
```
- 
	- There are four major status. Which are: 
		 
		 - **Untracked:** New file that Git doesn't yet track.
		 
		 - **Modified:** Changes are done in old file but Git doesn't track that.
		 
		 - **Staged:** Changes are added in the local repo of Git but it is not finalized.
		 
		 - **Unmodified:** Files are up to date With our local repo.

- ***Add:*** Add *untracked* or *modified* file to the local repo of git & make it ready for finalized.
```
git add <--file_name-->			# to add all file use file name --> .
```

- ***Commit:*** Finalized the changes.
```
 git commit -m "<--some meaningful massage-->"
```

- ***Push:*** Upload the local repo content to remote repo.
```
 git push -u origin main
```
> **Breakdown of the above command:**
> 	1) *git push* is the main command
> 	2) *-u* is a tag that creates a macro. With this in future if we type `git push` it automatically pushes to `origin main`. 
> 	3) *origin* (by convention) is the name of the remote repo in witch we are working 
> 	4) *main* is the branch name (It can vary)

==**Disclaimer:** It is suggested to use the internal terminal feature of code editor, else there will be a [[personal access token]] needed.==

- **Pull:** Used to fetch & download form remote repo & immediately match our local repo with that content.
```
git pull prigin main
``` 

---

### Uploading locally created repo to GitHub
Here we discuss How we can upload our local repo which we created in our system to GitHub through Git.

1) First we have to initialize Git in the folder which we want to upload.
```
 git init
```

2) *Create README.md* file.

3) Then, we can *add & commit* our project files and make our local repo upload worthy. 

4) Now we can *create a empty repo* (Without README.md file) at GitHub.
	 ==**Disclaimer:** It is suggested to not include README.md file. Because it we created it at GitHub then our README file can create problem, in that case we have to clone the README file from GitHub.==

5) At this point we create a stage to Upload our project file. Now we have to *connect our Git* (.git folder inside our project folder) *to remote repo* of GitHub.
```
 git remote add origin <--Link_provided_at_GitHub-->
```
> **Breakdown of the above command:**
> 	1) *git remote add* is the main command
> 	2) *origin* (by convention) is used to setup our remote empty repo as the uploading  and downloading repo for our .git folder
> 	3) The link is provided by GitHub

6) To verify our remote repo use:
```
 git remote -v
```

7) To check our current brunch use:
```
 git brunch
```

<mark style="background: #BBFABBA6;"><b>Problem:</b> By default Git uses the name 'master' as the core brunch, but by convention we use the name 'main'. So we have to change the name.</mark>

<mark style="background: #FFB8EBA6;"><b>Solution:</b></mark>
8) To rename the branch name:
```
 git branch -M <--branch_name-->
```

9) Now we can *push* our local repo.
 ---

### Workflow
Now we learn about two workflows to use Git & GitHub.

- [[Initializing through GitHub then clone it.canvas|Initializing through GitHub then clone it]]

- [[Working on local system then create & upload it To GitHub.canvas|Working on local system then create & upload it To GitHub]]

 But, we primarily use 1<sup>st</sup> method.

---

### Accessing Commit history 
To see commit history we use `git log` command.
```
git log
```

<mark style="background: #BBFABBA6;"><b>Problem:</b> At first 'git log' can show only few commit and you're unable to scroll to see more (or scrolling doesn't reveal anything further).</mark>

<mark style="background: #FFB8EBA6;"><b>Solution:</b></mark>
By default, `git log` uses a pager like `less` to display output.
If you're not seeing all commits because of the pager, you can disable it like this:
```
git config --global pager.log false
```

---

### Undoing Changes
There are some different scenarios according to which some different command is needed to be learn.

#### **Case 1:** Staged Changes
- To undo any staged (only added) changes use `git reset` command.
```
git reset <--file_name-->
``` 

- For multiple files:
```
git reset
``` 

#### **Case 2:** Committed changes (for one commit)
- We use `HEAD~` tag.
```
git reset HEAD~1
``` 
> **Breakdown of the above command:**
> 	1) *git reset* is the main command
> 	2) *HEAD~* is the tag
> 	3) *1* represents the number which indicate that we want to reset our code to that many commit behind

#### **Case 3:** Committed changes (for many commit)
For reset many commit behind we just copy the hash of the commit from `git log` command.

- Here we use `git reset` command.
```
git reset <--commit_hash-->
``` 

<mark style="background: #BBFABBA6;"><b>Problem:</b> After this command the commit after the resetting point are deleted, but the code in the IDE are unchanged.</mark>

<mark style="background: #FFB8EBA6;"><b>Solution:</b></mark>
To change the code in IDE we use `--hard` tag.
```
git reset --hard <--commit_hash-->
```

---

### Git branches
In Git, **branches** are pointers to commits. They help manage different lines of development within a repository. ![[Screenshot From 2025-06-04 22-33-25.png]]

---

#### Branch Commands
It will help to create, change, manage & merge Branches through command line.

- To see your current branch & the list of branches use `git branch`.
```
 git branch
```

- To rename any brunch we use `-M` tag.
```
git branch -M <--Branch_name-->
``` 

- TO navigate through branches use `git checkout`.
```
git checkout <--branch_name-->
```

- To create a new branch we use `-b` tag.
```
git checkout -b <--new_branch_name-->
``` 

- To delete any brunch that is same code as default *main* brunch, we use `-d ` tag.
```
git brunch -d <--branch_name-->
``` 

- To delete any brunch that is different code from default *main* brunch, we use `-D ` tag.
```
git brunch -D <--branch_name-->
``` 

---

## Merging Branches
We can merge two branches using both Git & GitHub.

#### Using Git
There is some command that allow use to safely merge two branches in our local repo. To show the changes in GitHub we have to `push` both branches.

1) To see the difference b/w two branches we use `git diff` command.
```
git diff <--branch_name--> 				
# Branch_name means the branch that you willing to compare your current branch 
```  

2) To merge two branches we use `git merge` command.
```
git merge <--branch_name-->
```

==**Disclaimer:** It is suggested to use the [[Integrated Development Environment]] For merging assistance. ==

#### Using GitHub
On GitHub we create [[Pull Request]] For merging Branches. [[Pull Request|PR]] allows you to tell other changes you've pushed to a branch in a repo on GitHub.

### Resolving Merge Conflict
**Merge Conflict** is an event that takes place when Git is unable to automatically resolve the differences in code b/w branches. Use [[Integrated Development Environment|IDE]] or [GitHub](https://github.com/) for merging assistance.


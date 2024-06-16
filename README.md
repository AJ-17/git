#                               GIT_COMMANDS

These Document is to get a brief idea about using git command line interface
for  a more Practical explanation You can Watch my Video on that [link](https://youtube.com/).

Using git we can easy excess the data files in a group or individualy and work
on to a project.

## Content 

- [Installing Git](#instalation)
- [Configuration/setup](#setup)
- [DATA FLOW STRUCTURE](#stages)


## Instalation
###  Windows
You can Install the latest version from the [git-scm site](https://git-scm.com/download/win)
### Linux
```bash
sudo apt-get update
sudo apt-get install git
```
### MacOS
```bash
brew install git
```
## Setup
```bash
mkdir dict
cd dict
git init
```

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```


## Stages

There are different steps to make the file handling between a group safer and secure

<img src='https://res.cloudinary.com/practicaldev/image/fetch/s--M_fHUEqA--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/128hsgntnsu9bww0y8sz.png'>

First when we delete modify or make a file it is untracked by git but to track
it we send it to the stag and then we commint all the thing which are in 
stack and are being tracked.
Once it is ready in stack we push it on to the site.


To add a file to stag or track it 

```bash
git add file_name
```

To add all the files in stag

```bash
got add -A
```


To remove a file from stag and harddisk
when we use rm a if the file is in the commited area (or say modefied)then  a delete tag is generated in the stage to be commited 
```bash
git rm file_name
```

To Remove files only from being tracked or stag

```bash
git rm --cached file_name
```

To commit the files avaliable in stag

```bash
git commit
```
In the above command a file would open having details about what changes would
be made and we can pass there some text and save the file as an comment to
that commit 

To add a modified file to stage and commit 
Note: its only for modified files

```bash
git commit -a
```

To get info about which file is in the stag & which is not 

```bash
git status
```
For a short result we can use 
?? mean untracked A mean staged AM mean modified  AD mean deleted 
```bash
git status -s
```
If you want to backup the files from the previous commit we can use 
```
git checkout filename
```
for complete match use
these is like a backup. newly made files not in the commeted area won't be affected if they are not staged .if they are staged then will be deleted  
```
git checkout -f
```                                                                                                                                                                       
To get the logs of what things are done and who have done it use 
```
git log
```
to get specific number of log like last 5 log use
use -p only if you need a detailed desprition of what changes are made 
To get a moderate Log we use --stat flag 
The --pretty=oneline flag shows only the commits that are done in one line 
--pretty=short adds who did the commit
--pretty=full adds who is the author,who did commit
--since=2.days or =2.years or =2.months or 2.hours or 2.weeks or 2.minute is for getting the log of last 2 days or year or month etc      
--until=1.day can specify the end day like since is start
-- eg git log --since=2024-06-10 --until=2024-06-12
```
git log -p -5
```


To see the differece betweent the modified file and staged file use diff ,if we don't use filename then all the diff will be displayed
```
git diff filename
```

To see difference between the commited and staging area use 
```
git diff --staged
```
To remove a file from the staging area without adding a delete tag of the file to be commited we use 
if the file is not stagged and we use  ```git restore filename``` then the file will be restored from commit
```
git restore --staged filename
```
if there any any files which we don't want to be tracked when we use git add -A  then we can make a .gitignore file and add its name in it .even if there is a file with that name inside a folder it will be ignored . even if the folder name is same as the file name compete folder will be ignored
if we add a use /filename in the gitignore file then only the files in the main directory will be ignored
if we want all the files will extension .jpg to be ignored then we can use *.jpg
by using * we can form any regix acc to the needs

To get a github file from github you can use the command 
these folders are already Initialized.so we can use git commands
```
git clone url.git 
```
or use these to change the folder name

```
git clone url.git new_name
```

when we rename a commited file the git assume that a new file is created and the privous name file is deleted to tell git that its renamed we use .
although its not a proper way git add . will act like git add -A or git add --a
```
git add .
```
the proper way to rename a file is 
```
git mv a.txt 1.txt
```

To do a new commit in the privous commit iself we use 
```
git commit --amend
```

## Connecting to the github repo

**Step 1**
Make a repositry public/private in github & copy the ssh url 
The below commad shows all the url's names only saved in our git eg
```
git remote 
```
a -v flag added to it will show the url + url name
To add a new url use the below command
```
git remote add origin url
```
the url will be know by the name origin 
**Step 2**
Making a ssh-key
these will create two files id_rsa(private key) id_rsa.pub inside the folder path that you will give
```
ssh-keygen -t rsa -b 4096 -C "example@example.com"
```
-t rsa: Specifies the type of key to create. RSA is one of the most common types.
-b 4096: Specifies the number of bits in the key. 4096 bits is a strong key size.

```
eval "$(ssh-agent -s)"
```
ssh-agent -s: This command starts the SSH agent, a program that runs in the background and manages your SSH keys. The -s flag outputs commands to set environment variables.

eval: This command executes the output of ssh-agent -s in the current shell. Essentially, it sets the environment variables for the SSH agent so that it can be used in your current session.

the below commad gives the private key to the ssh agent to handel it .
```
ssh-add ~/.ssh/id_rsa
```
**Step 3**
Now copy the content in id_rsa.pub & add a ssh key in your github repo setting

**Step 4**
Now you can push and pull in the repo
```
git push -u origin master
```
master is the branch name will discuss below later

```
git pull origin master
```
       
Done 

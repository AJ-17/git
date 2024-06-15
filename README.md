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
```bash
git status -s
```
If you want to backup the files from the previous commit we can use 
```
git checkout filename
```
for complete match use
```
git checkout -f
```
these is like a backup newly made files not in the commeted area won't be affected 

#                               GIT_COMMANDS

These Document is to get a brief idea about using git command line interface
for  a more Practical explanation You can Watch my Video on that [link](https://youtube.com/).


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
it we send it to the stack and then we commint all the thing which are in 
stack and are being tracked.

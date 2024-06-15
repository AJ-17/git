## GIT Commands

This document provides a brief introduction to using the Git command-line interface. For a more practical explanation, you can watch my video on [link](https://youtube.com/).

With Git, you can easily manage data files collaboratively, both individually and as a group, for version control purposes.

## Content

* [Installing Git (macOS)](#macos-installation)
* [Configuration/Setup](#setup)
* [Data Flow Structure (Stages)](#stages)
* [Comparing Changes (Diff)](#diff)
* [Undoing Changes](#undoing-changes)
* [Ignoring Files (.gitignore)](#gitignore)
* [Cloning Repositories](#cloning-repositories)
* [Renaming Files](#renaming-files)

## Installing Git (macOS)

There are two common ways to install Git on macOS:

**1. Using Homebrew (package manager):**

   - Install Homebrew if you don't have it already: [https://docs.brew.sh/Installation](https://docs.brew.sh/Installation)
   - Run the following command in your terminal:

     ```bash
     brew install git
     ```

**2. Downloading the installer:**

   - Go to the official Git SCM downloads page: [https://www.git-scm.com/downloads](https://www.git-scm.com/downloads)
   - Download the latest installer for macOS.
   - Run the downloaded installer and follow the on-screen instructions.

## Configuration/Setup

**1. Initialize a Git repository:**

   - Open a terminal window and navigate to your project directory.
   - Run the following command to initialize an empty Git repository:

     ```bash
     git init
     ```

**2. Configure your name and email:**

   - Set your user name and email address for Git commits:

     ```bash
     git config --global user.name "Your Name"
     git config --global user.email "your_email@example.com"
     ```

## Data Flow Structure (Stages)

Git uses a staged workflow to manage changes to your files. Here's a breakdown of the stages:

1. **Untracked:** New or modified files that haven't been added to Git's tracking system.
2. **Staged:** Files explicitly added to the staging area, ready to be included in the next commit.
3. **Committed:** Files that have been permanently saved in the Git repository history through a commit.
4. **Working Directory:** Your local project directory where you create, modify, and interact with files.

The image you provided can be helpful to visualize these stages. Consider using a free online tool like [https://www.drawio.com/](https://www.drawio.com/) to create a custom diagram if needed.

This staged workflow allows you to review changes before committing them permanently to the repository's history.

## Comparing Changes (Diff)

**To see the difference between a modified file and the staged version:**

```bash
git diff filename

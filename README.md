# Instructions

These are the instructions to install Git and Node in your local Linux or Mac machine!

## To get started
### Environment Set Up
**Mac Users:**
In order to set up our environment, we need to make sure that you have [Homebrew](https://brew.sh/) and XCode installed in your machine. Once that is done, you can use the `brew` command to install packages:

```bash
brew update
brew install curl
```

**Lubuntu Users:**
The Debian/Ubuntu package manager is `apt-get`. Run the following commands to install the `curl` and `build-essential` packages.

```bash
sudo apt-get update
sudo apt-get install curl build-essential
```
### Install Git
**Mac Users:**
```bash
brew update
brew install git
```

**Lubuntu Users:**
```bash
sudo apt-get update
sudo apt-get install git
```

### Configuring Git
You should always configure git and let it know who you are the first time you install it on a new machine. This way the commit log will always have proper author information.

```bash
git config --global user.name "First Last"
git config --global user.email "my@email.com"

git config --global push.default simple
git config --global core.autocrlf input
```

#### Explanation of the final two commands

```bash
git config --global push.default simple
```

This tells git to only push updates from your current branch up to remote repositories (like github). If you don't do this, then the original behavior could be to push all branches, even your experimental ones, up to remote repositories.

```bash
# mac/linux
git config --global core.autocrlf input
```

This setting deals with the end of lines (EOL) in your code files. For the best compatibility across platforms, it is best if Mac/Linux users set this to `input`.

## NVM and Node

The best way to manage your Node.js installations is to use the NVM (Node Version Manager) tool. It allows you to have multiple versions of Node.js installed simultaneously and provides commands to easily switch between different versions.

```bash
# Mac users should run this command first
touch ~/.bash_profile

# Install nvm
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash

# After nvm installs you should close your terminal and open a new one to access nvm

# Verify that nvm is working
nvm ls

# Install the LTS node.js version
nvm install 10.13.0

# Install another node.js version
nvm install 8.1.3

# You are now using version 8.1.3, to switch back to 10.13.0 run
nvm use 10.13.0

# Run the node repl (read-eval-print loop)
node
```
The node command runs the interpreter allowing you to run and evaluate JavaScript code. 
**Exiting Node:** Press `ctrl+d`

If the nvm command is not working for you on the Mac, then check this section for additional troubleshooting: [https://github.com/creationix/nvm#install-script](https://github.com/creationix/nvm#install-script).

## Tools to Test API
For the purposes of testing the API, we will be using [Postman](https://www.getpostman.com/apps). Download the version corresponding to your machine.

# zsh-setup-guide

## Table of Contents
- [Introduction](#introduction)
- [What is Zsh?](#what-is-zsh-)
- [What are the benefits?](#what-are-the-benefits-)
- [What is Oh My Zsh?](#what-is-oh-my-zsh-)
- [Must-have Plugins](#plugins-that-i-have-tried-myself-and-which-i-think-are-a-must-for-everyone-to-use)
- [Setup and Installation](#setup-and-installation-)
- [Notes](#notes)
- [Before vs After](#difference-between-how-the-terminal-looks-before-and-after)
- [References](#reference-used)

## Introduction
- This is a short and crisp support document for anyone looking to get started with installing and using zsh.
- I’ve found myself scrambling through articles every time I have to set this up from scratch, thinking I’ll remember it next time.
- So, this time I decided to summarize the steps along with the resources I used.

## What is Zsh ?
- The Z shell (also known as zsh) is a Unix shell (shell describe below) that is built on top of bash (the default shell for macOS) with additional features.
- A shell is a program that lets you interact with the operating system using commands. It takes your input, passes it to the OS, and shows the output. Examples: Bash, Zsh, Fish.

## What are the benefits ?
- It makes interacting with the OS through commands much easier and more configurable.
- You can customize how the shell looks and much more—for me, it also makes using the machine more enjoyable.
- You can make the terminal as much fancy as you want.


**At the very least, it should be clear by now that using Zsh over Bash offers more advantages and makes the experience much easier.**

## What is Oh My Zsh ?
- Oh My Zsh is an open source, community-driven framework for managing your zsh configuration. It comes with a bunch of features out of the box and improves your terminal experience.
- On top of that, the framework lets you add plugins created by other developers, which you can easily plug in based on your needs.
- Oh My Zsh simplifies:
  -   Shell customization (themes, aliases, settings).
  -   Plugin management (Git, Docker, auto-suggestions, etc.).
  -   Zsh configuration via a central `.zshrc` setup.
  -   Making Zsh beginner-friendly with sane defaults.
- Putting the list of all the plugins that you can use as per your need - https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins

## Plugins that I have tried myself and which I think are a must for everyone to use
- zsh-autosuggestions : This will add auto suggestions to your terminal based on your command history.
- zsh-syntax-highlighting : The Syntax Highlighting plugin adds beautiful colors to the commands you are typing.
- powerlevel10k : I think this is my favorite so far as it lets me choose my preferred theme through an interactive, step-by-step setup menu.

## Setup and installation :
- `brew install zsh` : install zsh.
  - Note : Only for mac users, that too brew will have to be installed first.
- `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` : install oh my zsh (this is the magic)
- Follow `https://github.com/ohmyzsh/ohmyzsh/wiki` to make changes and source the changes with `source ~/.zshrc`
- Add plugins to your shell by adding the name of the plugin to the plugin array in your `.zshrc` like below.
  - `plugins=(git colored-man-pages colorize pip python brew osx)`
- Example for adding `zsh-autosuggestions` :
  - Clone the zsh-autosuggestions plugin’s repo and copy it to the “Oh My ZSH” plugins directory.
  - `git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
  - Add the name to plugins like `plugins=(git brew zsh-autosuggestions)`
  - Enforce changes : `source ~/.zshrc`


## Notes
- Oh My Zsh is not the only way to customise zsh there are others as well but it's recommended to have only one at a time.
- The command in this guide are mac specific as of now and I invite collaboration to this to make sure all relevant commands are setup so that this becomes one stop solution to install and setup zsh and oh my zsh.

## Difference between how the terminal looks before and after

**Kinda dull**
<br/>
<br/>
<img width="600" alt="Before" src="https://github.com/user-attachments/assets/8a72a7ca-b4b3-49f6-8e8e-6e7962a72bac" />

<br/>
<br/>
<br/>

**Much more crisp and interesting**
<br/>
<br/>
<img width="600" alt="After" src="https://github.com/user-attachments/assets/8485180f-fb06-4733-a7b6-97b0093b6dd6" />


## Reference used 
- For Mac, a one-stop installation guide can be found here: https://sourabhbajaj.com/mac-setup/iTerm/zsh.html (this one has other cool stuff for mac as well 😉)
- Different plugins : https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins
- Wiki : https://github.com/ohmyzsh/ohmyzsh/wiki

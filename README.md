# Tmux (Terminal Multiplexer) Tutorial

## Table of Contents
* [Introduction](#introduction)  
* [Installation](#installation)
* [Basic Commands](#basic-commands)
* [Configuring Tmux](#configuring-tmux)
* [Sessions](#sessions)
* [Text Manipulation](#text-manipulation)
* [Advanced Commands](#advanced-commands)
* [Tmux for SSH and Pair Programming](#tmux-for-ssh-and-pair-programming)

## Introduction
[Tmux](https://tmux.github.io/ "tmux") is a command-line program through which one can control one or more virtual windows and processes from a single window. 

Go to [Top](#table-of-contents)

## Installation

### Linux
If you are on Debian or Ubuntu, on the command line type `sudo apt-get install tmux`.

Go to [Top](#table-of-contents)

## Basic Commands

### Start Tmux

To start a new session, either type `tmux` or `tmux new -s <session-name>`.

#### Prefix

The __prefix key__ (denoted by `<Prefix>`) is a special key in tmux that precedes most of the keyboard shortcuts. By default, the prefix key is bound to `C-b` (`Ctrl + b`). It is pretty cumbersome to type `C-b`. So, it is best if one swaps the functions of `Ctrl` and `CapsLock`, and then rebinds the prefix key to `C-a`. Over a period of time, this decreases typing time considerably, and boosts productivity several fold. Seriously!

#### Tmux Command Prompt

You can access the tmux command prompt by typing `<Prefix>-:`. This opens up a prompt at the bottom of the screen. Having done that, type any command tmux command without preceding it with `tmux`. For example, typing `<Prefix>-:`, followed by `list-sessions` (see [Session](#session) below) shows the list of active and inactive tmux sessions. The same result can be achieved by typing `tmux list-sessions` on the (normal) command line. 

#### Quick access to Key Bindings

Typing `<Prefix>-?` shows the list of key bindings. By default, tmux enables `emacs` mode. See [below](#configuring-tmux) on how to change to `vi` mode. 

### Session

A _client-server_ system underlies the tmux architecture. Whenever a tmux session is first started, a server instance is created (behind the scenes and automatically), and the session runs as a client of that server. More than one session may be created, and all such sessions may be assigned as clients of the same server instance. A client may be attached to or detached from a server instance.

Within a single session, there may be multiple shell instances called _windows_. One or more _panes_ may populate a window. By default, when a new window is first created, there is just one pane populating that window.

The name of each session can be changed, like so: `tmux rename-session <new-session-name>`. Or, one could just type `<Prefix>-,` (the prefix key followed by comma), wherein a prompt appears at the bottom of the screen.

#### Windows

To create a new window in an existing session, type `<Prefix>-c`.

If there are multiple windows open in a current session, type `<Prefix>-1` to jump to window `1`, and so on.



Go to [Top](#table-of-contents)

## Configuring Tmux

Go to [Top](#table-of-contents)

## Sessions

Go to [Top](#table-of-contents)

## Text Manipulation

Go to [Top](#table-of-contents)

## Advanced Commands

Go to [Top](#table-of-contents)

## Tmux for SSH and Pair Programming

Go to [Top](#table-of-contents)

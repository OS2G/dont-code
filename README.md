# Don't code: Using existing programs

This guide shows how to use programs with zero knowledge of programming. The lone requirement is a computer. Common sense is recommended but not required.

By the end of this tutorial, you will have downloaded, installed, and used the youtube-dl python library on your local machine.

If you learn best by doing, start at the Demonstration section. Reference the Key Components section if you have issues you can't figure out.
DISCLAIMER: Legalese saying you are responsible for using this library legally. Will ask a lawyer.

- [Don't code: Using existing programs](#dont-code-using-existing-programs)
  - [Why-write-this-guide?](#why-write-this-guide)
  - [When to code](#when-to-code)
  - [Identifying your needs](#identifying-your-needs)
  - [Key Components](#key-components)
     - [Runtime Environment](#runtime-environment)
     - [Executing the Source Code](#executing-the-source-code)
     - [Debugging](#debugging)
  - [Demonstration: Safely Downloading MP3s from Youtube](#demonstration-safely-downloading-mp3s-from-youtube)
    - [Runtime Environment: Python and Pip installation](#runtime-environment-python-and-pip-installation)
      - [Getting Python](#getting-python)
        - [Windows](#windows)
        - [Mac](#mac)
        - [Linux](#linux)
      - [Pip Package Manager](#pip-package-manager)
      - [Verify Environment](#verify-environment)
    -  [Executing Source Code: Youtube-dl](#executing-source-code-youtube-dl)
        -  [Installing Youtube-dl](#installing-youtube-dl)
        -  [Youtube-dl Command Line Usage](#youtube-dl-command-line-usage)
        -  [Skimming Manuals](#skimming-manuals)
    -  [Debug Issues](#debug-issues)
        -  [Finding Known Good Components](#finding-known-good-components)
        -  [Tips on Googling Errors](#tips-on-googling-errors)
        -  [Ask Questions: Developer Communities](#ask-questions-developer-communities)
  -[Next Steps From Here](#next-steps-from-here)
  
## Why write this guide?
As a result of several very interesting factors, nontechnical people today tend to see modifying their machine as a major hurdle, even though this could not be further from the truth.

It is a widespread misconception that knowing how to code is necessary to make use of a program. There is also much confusion and debate over the difference between a coder and a programmer. Though these terms are used interchangeably, one UNL CS grad now working in the Bay Area explained his reality succinctly: "I make six figures for having a degree in Stack Overflow."

Most commonly used tools in the tech sector (computers, operating systems, programming languages, frameworks, etc) required a significant amount of work to build. As a result, almost all programmers spend most of their time working on top of or modifying someone else's existing system. LINUX itself was born this way. 

Coding has become something mystical and learning to do so becomes a mental stumbling block. Several popular platforms meant to teach programming spend little to no time talking about how to actually use the machine you are currently on (after all, if you can execute programs locally why keep the subscription when the information is freely available online?). As a result, burnout among novices has become a norm.

Programming was born as a way to tell computers how to automate, accelerate, and augment our ability to crunch numbers. Computers are not a magical solution to everything (the answer to life is 42). Programs are tools that can be replicated at practically no cost. Getting these tools to accomplish a desired task is the true goal. 

So how do you decide if you should make a tool or using an existing one?

## When to code
If you take anything from this guide, it should be this: Before you ever write a line of code, go find out what other people have already done.

Writing a major program from scratch is time consuming. The more you want it to do, the more convoluted the program becomes. People commonly work together on larger programs because of these issues (git and github exist for this reason).

It is extremely rare that you are the first person to encounter the problem you are trying to solve. Sorry. The good news is that whoever got there first either solved it or complained somewhere about whatever made the task infeasible. If fact, there's a decent chance that somebody else disliked something about the first solution and made a slightly different one.

![Philosophy of this guide in a nutshell](https://imgs.xkcd.com/comics/standards.png)

Building something from scratch can be incredibly fun and rewarding. Most of the time, you just need something done. A paperclip and a screwdriver can accomplish remarkable things if you figure out what has to happen. Good solutions come about when the problem is well defined.

## Identifying Your Needs
This section helps a person assess what they're trying to do and different approaches to do it.

## Key Components

This section explains the general steps involved in installing and using someone's program.

### Runtime Environment

This covers why programming languages or tools are installed to make them usable

### Executing the Source Code
This section covers figuring out how/where to download certain code and how to then use it

### Debugging
Stuff breaks. This sections explains common ways to make things work.

## Demonstration: Safely Downloading MP3s from Youtube
Legal disclaimer will go here, also explains why this simple tutorial was chosen.

### Runtime Environment: Python and Pip installation
This area explains that we're installing Python and Pip to accomplish the usecase and how we figured out that we'd need it (RTFM) Should also cover the value/utility in having a package manager like Chocolatey, MacPorts, or Homebrew.

In order to complete our projects, we need to create what's known as a runtime environment. In essence, it's gathering all the required tools and preparing your computer to be able to run a program - similar to gathering all the required ingredients, appliances, and utensils needed to make a meal. For this demonstration we will need two things: the Python programming language and Python's package manager, Pip.

You're probably familiar with the concept of a programming language, but a package manager may be more foreign. Package managers are basically a one-stop shop for software. You don't need to worry about independently upgrading software, resolving dependency issues (what other software your software needs to run), or what order things must be installed in. All of this is taken care of by the package manager. There are different package managers out there for different use cases, but the one we are focusing on is Pip which manages software libraries written in Python. We'll go over installing both of these things below.


#### Getting Python
Python was chosen for this tutorial because it's incredibly well known, easy to learn as a language, and very well documented. Installing it takes less than five minutes. There's also a large userbase to ask questions. Python 2 or 3 will work for this demonstration.

##### Windows
Installing Python on Windows is very straightforward.
 1. Follow this link that brings you to the download page for Windows: https://www.python.org/downloads/windows/
 2. Click on the latest stable release for Python 3
 3. Scroll to the bottom of the page where the files to download are listed and download the `Windows x86-64 executable installer`
 4. Install the program just selecting the defaults as you go through the menus

##### Mac
Should come baked in, slim chance you may need to deal with X-Code nonsense. Skip to the Verify Enviroment section. If it isn't, please let us know by making an issue on this repo.

##### Linux
Python comes pre-installed on many distributions of Linux. Check to make sure it's there by entering `python --version` into your terminal. If you get a reply that Python is not installed on your computer, install it with the following commands (for an Ubuntu-based distribution):
```
$ sudo apt update
$ sudo apt install python3.6
```
It should be noted, if you have Python already installed on your Linux machine, it's most likely Python 2. If you decide to install Python 3 alongside, how you use Python on the terminal will be different:
`$ python` will bring up Python 2
`$ python3` will bring up Python 3

For other distributions that do not use the apt package manager, you will have to Google how to install it. If you got such a distro installed, you can clearly RTM and will be just fine.

#### Installing Pip Package Manager
Pip allows you to use python libraries, which are awesome. Installing pip opens up lots of doors through the larger python ecosystem. 

Python generally comes baked in with pip, which can be confirmed by using the following commands for Python 2 and 3 respectively:
```
$ python -m pip --version
$ python3 -m pip --version
```

TODO: show the install instructions if it doesn't come baked in. Never had this issue, probably worth talking about how to link pip with the installed python version.

#### Verify Environment
This section explains why you'd want to verify all the above stuff worked correctly (debugging purposes, knowing which versions of stuff you installed, checking that pathing is good).
``` python --version ``` will tell you which version of python is being used when you use the "python" command.
``` pip --version ``` will tell you which version of pip is being used when you use the "pip" command.

### Executing Source Code: Youtube-dl
This section explains how we figured out how to get youtube-dl on our machine and how to figure out/learn its usage.

#### Installing Youtube-dl
This section explains why we're using pip to install Youtube-dl (convenience) and how to do so.
``` [sudo] pip install youtube-dl ```

#### Youtube-dl Command Line Usage
This section details a few basic usages of Youtube-dl. 

#### Skimming Manuals
This section explains how to search documentation for the specific issues 

### Debug Issues
Stuff breaks. This section shows how to use the general tips from the debugging section specifically for/on this particular usecase (youtube-dl)

#### Finding Known Good Components
This section covers basic reverse engineering and how to trace back the root cause of an error you are experiencing.

#### Tips on Googling Errors
This section details how to increase or decrease the specificity of an error you are currently trying to understand.

#### Ask Questions: Developer Communities
When you can't figure out the answers (or what questions to ask), generally phoning a friend is the way to go. This section is meant to help people understand how to find the relevant communities for a particular problem they are currently working on.

## Next Steps From Here
Find usecases you care about and try to find code that does them! Lots of room in this space, feel welcome to submit PRs!

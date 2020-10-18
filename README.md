# Don't code: how to use existing programs

- [Don't code: how to use existing programs](#dont-code-how-to-use-existing-programs)
  - [When to code?](#when-to-code)
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
  
TBD: Add an overview of this document and the purpose it serves.

## When to code?

This section described why you may not want to write a program from scratch.

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
This area explains that we're installing Python and Pip to accomplish the usecase and how we figured out that we'd need it (RTFM) Should also cover the value/utility in having a package manager like Chocolatey for Homebrew

In order to complete our projects, we need to create what's known as a runtime environment. In essence, it's gathering all the required tools and preparing your computer to be able to run a program - similar to gathering all the required ingredients, appliances, and utensils needed to make a meal. For this demonstration we will need two things: the Python programming language and Python's package manager, Pip.

You're probably familiar with what a programming language is, but a package manager may be more foreign. Package managers are basically a one-stop shop for software. You don't need to worry about independently upgrading software, resolving dependency issues (what other software your software needs to run), or what order things must be installed in. All of this is taken care of by the package manager. There are different package managers out there for different use cases, but the one we are focusing on is Pip which manages software libraries written in Python. We'll go over installing both of these things below.


#### Getting Python
Python was chosen as a great starting point in this tutorial because it's incredibly well known, easy to learn as a language, and very well documented. There's also a large userbase to ask questions.

##### Windows
Installing Python on Windows is very straightforward.
 1. Follow this link that brings you to the download page for Windows: https://www.python.org/downloads/windows/
 2. Click on the latest stable release for Python 3
 3. Scroll to the bottom of the page where the files to download are listed and download the `Windows x86-64 executable installer`
 4. Install the program just selecting the defaults as you go through the menus

##### Mac
Most likely just comes baked in, may need to deal with X-Code nonsense

##### Linux
Python comes pre-installed on many distributions of Linux. Check to make sure it's there by entering `python --version` into your terminal. Python 2 or 3 will work for this demonstration. If you get a reply that Python is not installed on your computer, install it with the following commands (for an Ubuntu-based distribution):
```
$ sudo apt update
$ sudo apt install python3.6
```
It should be noted, if you have Python already installed on your Linux machine, it's most likely Python 2. If you decide to install Python 3 alongside, how you use Python on the terminal will be different:
`$ python` will bring up Python 2
`$ python3` will bring up Python 3

For other distributions that do not use the apt package manager, you will have to Google how to install it.

#### Installing Pip Package Manager
Pip allows you to use python libraries, which are awesome. Installing pip opens up lots of doors. Doesn't make sense to have subsections for this given it's probably a single command line command to make it work.



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

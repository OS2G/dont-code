# Don't code: how to use existing programs

- [Don't code: how to use existing programs](#dont-code-how-to-use-existing-programs)
  - [When to code?](#when-to-code)
  - [Identifying your needs](#identifying-your-needs)
  - [Key Components](#key-components)
    -[Runtime Environment]
    -[Executing the Source Code]
    -[Debugging]
  - [Demonstration: Safely Downloading MP3s from Youtube](#demonstration-safely-downloading-mp3s-from-youtube)
    - [Runtime Environment: Python and Pip installation](#runtime-environment-python-and-pip-installation)
      - [Getting Python](#getting-python)
        - [Windows](#windows)
        - [Mac](#mac)
        - [Linux](#linux)
      - [Pip Package Manager](#pip-package-manager)
    -  [Executing Source Code: Youtube-dl](#executing-source-code-youtube-dl)
        -  [Installing Youtube-dl](#installing-youtube-dl)

This tutorial and reference is in no way exhaustive. However, we do hope you still find it useful. Start here, however if you can't find the answer to your question *~~Google~~ DuckDuckGo is your friend*.

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
This area explains that we're installing Python and Pip to accomplish the usecase and how we figured out that we'd need it (RTFM)

#### Getting Python
Python was chosen as a great starting point in this tutorial because it's incredibly well known, easy to learn as a language, and very well documented. There's also a large userbase to ask questions. Should also cover the value/utility in having a package manager like Chocolatey for Homebrew
##### Windows
Brief guide explaining how to install Python on Windows (probably just a link)
##### Mac
Most likely just comes baked in, may need to deal with X-Code nonsense
##### Linux

This depends entirely on your distribution, lots of variety (maybe cover how to install on ubuntu or link to some other tutorial)

#### Pip Package Manager
Pip allows you to use python libraries, which are awesome. Installing pip opens up lots of doors. Doesn't make sense to have subsections for this given it's probably a single command line command to make it work.

### Executing Source Code: Youtube-dl
This section explains how we figured out how to get youtube-dl on our machine and how to figure out/learn its usage.

#### Installing Youtube-dl


Everything below this stayed for the sake of convenient templating


##### Debian based

```
sudo apt install git
```

##### Arch based

```
sudo pacman -S git
```

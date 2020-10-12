# Don't code: using programs without programming 

- [Don't code: using programs without programming](#dont-code-using-programs-without-programming)
  - [What is it?](#what-is-it)
  - [History](#history)
  - [How does one get it?](#how-does-one-get-it)
    - [Command-line Solutions](#command-line-solutions)
      - [Linux](#linux)
        - [Debian based](#debian-based)
        - [Arch based](#arch-based)
        - [The rest](#the-rest)

This tutorial and reference is in no way exhaustive. However, we do hope you still find it useful. Start here, however if you can't find the answer to your question *~~Google~~ DuckDuckGo is your friend*.

## What is it?

First, you need to know what `git` is and why you need it. It's not the only solution on the market, but it's one of the most popular. Source-control management (SCM) is a way to manage source code. If you ever have code you need to share with others, post online, or keep a history of, you will want an SCM. In the past, people would just self version files and hope they don't get mixed up, or they would just share code via emails and the likes. This it not a great way of doing things and gets quickly out of hand.

That's why we use and SCM and why we use `git`. To keep track of your code and changes, and to allow for others to collaborate on code. As long as everyone follows proper `git` etiquette, then there's usually nothing that goes wrong. It's easy to see when and what someone changed in the history and whether it's the reason your program no longer compiles. You can integrate repositories with build systems as well so you can automate testing and building of new code, as well as deploy changes quickly. It's the reason people in the industry use it.

## History

Every program has a purpose and a story. `git` was "lovingly" created out of the need for a better way to manage code and code history. By better, I mean free and open source. The Linux kernel was previously using BitKeeper, a proprietary SCM system that they had been using to maintain the project since 2002. The copyright holder of BitKeeper, Larry McVoy, had withdrawn free use of the product after claiming that Andrew Tridgell had created SourcePuller by reverse engineering the BitKeeper protocols. The same incident also spurred the creation of another version-control system, Mercurial (`hg`). It's been maintained since 2005.

The name has no real original meaning, but many people have given it meaning depending on their mood, such as:
- random three-letter combination that is pronounceable, and not actually used by any common UNIX command. The fact that it is a mispronunciation of "get" may or may not be relevant.
- stupid. contemptible and despicable. simple. Take your pick from the dictionary of slang
- "global information tracker": you're in a good mood, and it actually works for you. Angels sing, and a light suddenly fills the room.
- "goddamn idiotic truckload of sh*t": when it breaks

This all doesn't really matter however. What you're here to do is learn how to use it.

## How does one get it?

`git` was and always will be, at its core, a command-line based program. People aren't command-line adept however. They like to see colors, visuals, and buttons they can click on. Because of this, countless GUI based programs have been spurred which run the `git` protocol. However, it's important to know how to get around on a terminal.

### Command-line Solutions

If you're on Linux or macOS, you might already have it. Just open up a Terminal and type in `git --version` to see if you get any output. If you get a "Command not found" error, then you'll need to install it. In Windows, you will have to install it; it doesn't come prebaked.

#### Linux

This depends entirely on your distribution.

##### Debian based

```
sudo apt install git
```

##### Arch based

```
sudo pacman -S git
```

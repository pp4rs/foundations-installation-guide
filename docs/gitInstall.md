<!--
TODO: Should we add a GIT GUI to installation guide?
-->

# Installing Git and Setting Up Accounts

Git is a Version Control System (VCS) that has gained a lot of traction among the programming community.
We will want to use version control to keep track of the files we write, and the changes we make to them.

## Account Creation

During the course we will show you how to use [GitHub](https://www.github.com) to host some of your work and do code related project management. You will need to set up an account:

<!-- During the course we will show you how to host some of your work on GitHub and the Economics Department's internal GitLab server.
You will need to setup accounts for each of these: -->

*   Please [register](https://github.com/join) for a [GitHub](https://github.com/) account
    - We recomment choosing a username that is independent of your workplace (i.e 'janesmith' rather than 'janesmith_uzh' so it can be portable when you change jobs).
<!-- *   Sign into the [Economics Department's GitLab server](https://econgit.uzh.ch/). Use your UZH shortname and your web-access password (same as for OLAT). You will need to access "Econ Git" while on-site at UZH or whilst using a UZH VPN if you are off-site. -->

!!! danger Privacy, Data Sharing and GitHub
    GitHub was recently acquired by Microsoft, so by providing

<!-- !!! danger "Non-UZH Economics Students"
    The UZH Department of Economics has a internal Git server that may be hard for you to access.
    It looks and behaves almost identically to [GitLab](https://about.gitlab.com/).
    We recommend that you register for an account here, so you can follow along in class. -->

## Mac Users

On MacOS, download and install Git from [here](http://git-scm.com/download/mac). If your system says it can't be opened, because it is from an unidentified developer, then open it via right-lick and `open`.
Also install the command-line auto-completion script. For this go to [this website](https://github.com/git/git/raw/master/contrib/completion/git-completion.bash). You should now see a the text file starting with

```
# bash/zsh completion support for core Git.
#
# Copyright (C) 2006,2007 Shawn O. Pearce <spearce@spearce.org>
# Conceptually based on gitcompletion (http://gitweb.hawaga.org.uk/).
# Distributed under the GNU General Public License, version 2.0.
```

save this file as `git-completion.bash` to your user folder by pressing `CMD+s`. If you want to know where your user folder is, open a terminal and type ```pwd```. For Uli it is for example under `/Users/ubergmann`.

If you use Safari, make sure to save the file as `Page Source` and don't append a `.txt` to its filename (Chrome does this automatically). If everything went right, you can now type `ls` in your terminal window and should see `git-completion.bash` there between other files.


## Linux Users

Follow the steps documented [here](https://git-scm.com/download/linux) to install on Linux from the terminal.

!!! danger
    To install system software using `apt-get`, you need `Super User` rights. So please add `sudo` in front of each `apt-get` command in the document above, like so: ```sudo apt-get install git```


## Windows Users

Download and install the latest versions of [msysgit](http://msysgit.github.io)

<!--, and
*   [TortoiseGit](http://code.google.com/p/tortoisegit/wiki/Download)
-->

After installing these programs use Windows Explorer to go to a folder that contains some documents (any folder) and right click on it.
You should see some additional items - "GitBash" appear in the context menu upon right-clicking.


!!! danger "Windows PATH Setting Redux"
    We also want Git from the command line, so we again need to update our PATH settings.

    Right-click on Computer. Then go to "Properties" and select the tab "Advanced System settings". Choose "Environment Variables" and select `Path` from the list of system variables.

    Choose `Edit`.

    **On Windows 7 or 8 machines:**
    If you accepted all defaults during your installation, and didn't have any other non-default setting prior to starting this guide, modifying the following string, copy and paste the following string without spaces at the start or end:

           ;C:\Program Files\Git\bin

    **On Windows 10 machines:**
    Click `New` and paste the following string:

            C:\Program Files\Git\bin

    Click on `OK` as often as needed.


## Verifying your install

<!-- We will need to make Git accessible from the command line. Windows and Mac users will need to follow the steps on the page "Modifying Path Settings." Linux users will already have git accessible from the command line. -->

To verify your installation, type the following command in a terminal and press the return key:

```bash
       git --version
```

You should get an output that looks like:

```bash
        git version 2.18.0
```

Ensure that you have a version greater than `2.15.0` installed.

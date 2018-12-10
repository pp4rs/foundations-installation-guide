# Command Line Tools

A command-line interface or command language interpreter (CLI), also known as a terminal, is a means of interacting with a computer program where the user issues commands to the program in the form of successive lines of text (command lines).

Throughout the course we will emphasize use of the terminal and executing commands within it as our modus operandi.

## Windows Users

So that we can work as closely as possible to the Mac and Linux users we will install [Cygwin](https://www.cygwin.com/).

*   Download Cygwin [here](https://cygwin.com/install.html) and use the graphical installer. Accept all the default options.
*   Choose any server from which to download cygwin and packages when prompted.
*   Verify your installation by opening Cygwin. When it opens you should see a black box with some text that looks like:
```bash
userName@computerName: ~$
```
i.e. for Lachlan he sees:
```bash
lachlan@lachlan-ThinkPad: ~$
```
We will explain what all this means in the first day or so of the course.

!!! tip "Why Cygwin"
    *   We will uses Cygwin as our command line tool, and unlike other Windows shells such as PowerShell it uses Unix syntax.

    *   Anywhere throughout the remainder of the installation guide where we suggest you to enter a command into a terminal, enter the text-based command into your Cygwin terminal followed by pressing `Return`, for example:

            userName@computerName: ~$ whoami


    Should return your username.

!!! danger "Do Not Delete the Install File"
    *   **Do not delete the setup-x86_64.exe file.** It needs to be kept so that we can add on some additional packages to use in the course.

## Mac Users

A command line interface comes already installed with OSX.

You will need to install some other software from the terminal thoughout the course, so it will be useful to install some additional "command line tools" now:

*   First we want to install X-code command line tools. Open a terminal by searching for it with spotlight, `cmd + spacebar` then type terminal and press `Return` when it appears. Then, copy and paste the following

```bash
xcode-select --install
```

If you get an answer that the command line tools are already installed, you can just continue to the next step.

* Second,  install Homebrew by opening a terminal and pasting the following command:

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

* To verify that Homebrew installed correctly, enter the following into your terminal
```bash
brew doctor
```
And you should see the following output
```bash
Your system is ready to brew
```

* Now we can use homebrew to easily install software. We want to make sure you have some basic system tools that some packages require. Let's (re)install them real quick. First `libxml2`:

```bash
brew reinstall libxml2
```

If you system tells you that it is not yet installed, then try  ```brew install libxml2``` instead.

We also want to link this so that terminal finds it later:

```bash
echo 'export PATH="/usr/local/opt/libxml2/bin:$PATH"' >> ~/.bash_profile
```

* Second, we also need `openssl`:

```bash
brew reinstall openssl
```
Again, if it is already installed, then use ``` brew install openssl``` instead.

Again, we need it to link to terminal:

```
echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile
```

* Finally, we need `libgit2`:

```bash
brew install libgit2
```

If terminal tells you it is not yet installed, then go for ```brew reinstall libgit2```

## Linux Users

Linux comes with a  command line interface already installed.
We need to install some additional system tools. For this open a terminal session with `Crtl` + `Alt` + `T`.

* Now copy the following command into terminal and press `Enter`:

```bash
  sudo apt-get install libcurl4-gnutls-dev librtmp-dev
```

* After the installation succeeded successfully repeat this one-by-one with the following two other commands:

```bash
sudo apt-get install libxml2-dev
sudo apt-get install libssl-dev
```

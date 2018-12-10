# Installing Anaconda Python

Anaconda is a pre-packaged Python distribution for scientific users.

Direct your browser to [Anaconda download page](https://www.anaconda.com/download/) and download the Python 3.7 Graphical Installer for your machine.
Follow the steps provided on the website.

During the installation you will be asked whether you want Anaconda Python to be added to your PATH. **Click yes!** Even if the installation window gives a warning about adding it to your PATH, please still check that box.

!!! note "For Windows Users:"
    *   When asked if you want single or multiple user installation, choose single user
    *   Accept all defaults that are set in the installation window
    *   Check the box for adding Anaconda to your PATH
    *   In the last step, you are asked if you want Visual Studio, click **Yes**.

!!! note "For Linux Users:"
    For some users Python was not added to the path. To quickly do this, please open a terminal window, paste ```echo '$HOME/anaconda3/bin:$PATH' >> ~/.bashrc``` and press `Return`.

## Verifying that the installation was successful

To verify that the correct version of Python has been installed and was made available in your PATH settings, close your terminal and open a **new** terminal interface and enter:


```bash
python --version
```
followed by hitting the `Return` key.

You should see the following information returned:

###   Windows users:

```bash
Python 3.7.x :: Anaconda, Inc.
```

###  Mac & Linux/Ubuntu users:

```bash
Python 3.7.x :: Anaconda custom (64-bit)
```

!!! tip "Python 2 vs Python 3"
    Python 2 and 3 are incompatible in syntax. If you had Python 2 previously installed on your machine, you might have seen `Python 2.x.x` above. In that case try typing

    ```python3 --version```

    instead. Now you should see a message like the one above and are good to go for the course.

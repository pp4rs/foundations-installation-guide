# Snakemake

Snakemake is an easy to use workflow management system.
It will allow us to control the execution of a set scripts by by running them from the command line.
We will use make to automate the execution of our research projects with a "single click" so that our entire work flow is reproducible.

<!-- !!! tip "Why a Tool to Manage Project's Execution?"
    We strongly believe in using build tools to manage the execution of a research project - and we hope that by the end of the course you do too.

    Some reasons we push this topic are:

    * Your workflow / order of execution is explicitly documented.
    * Each time you run Snakemake, it only executes each script if the output is expected to be different from the last time your ran it. That is, it runs 'partial builds.'
    * Its written in Python, which minimizes the learning curve needed to pick up the essentials relatively small
    * It was designed for academic/professional research (in Bioformatics) so it feels more intuitive than most alternatives for our desired audience. -->

Snakemake is a Python package - so you will need Python installed on your computer.
We recommend installing [Python](../python/) from Anaconda.

## Mac & Linux Users:

In a terminal window enter the command:

```bash
pip install snakemake
```
followed by pressing the `Return` key.

Verify that your installation worked correctly by entering

```bash
snakemake --version
```
into a terminal and pressing `Return.`

The expected output is the current version on the software, which should be greater than

```bash
5.2.2
```

## Windows users

We need one extra step here. In a cygwin window enter the command:

```bash
conda install datrie
```

followed by pressing `Return`.

If you get an access denied error, you may have not clicked on single user install in the Anaconda installation. De- and re-install Anaconda and try again.

If the above command works, your terminal will look something like this:

```bash
The following NEW packages will be INSTALLED:
datrie: 0.7.1
proceed ([y]/n)
```

Type `y` and hit enter. Once this is done, type:

```bash
pip install snakemake
```

followed by pressing the `Return` key.

The expected output is the current version on the software, which should be greater than

```bash
5.2.2
```

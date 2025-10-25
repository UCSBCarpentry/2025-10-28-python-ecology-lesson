---
title: Setup
---

::::::::::::::::::::::::::::::::::::::::::  prereq

## Data

Data for this lesson is from the
[Portal Project Teaching Database](https://figshare.com/articles/Portal_Project_Teaching_Database/1314459).
Specifically, we use the following eight data files:

- [bouldercreek\_09\_2013.txt](data/bouldercreek_09_2013.txt)
- [plots.csv](https://ndownloader.figshare.com/files/3299474)
- [portal\_mammals.sqlite](https://ndownloader.figshare.com/files/11188550)
- [species.csv](https://ndownloader.figshare.com/files/3299483)
- [speciesSubset.csv](data/speciesSubset.csv)
- [surveys.csv](https://ndownloader.figshare.com/files/10717177)
- [surveys2001.csv](data/yearly_files/surveys2001.csv)
- [surveys2002.csv](data/yearly_files/surveys2002.csv)

Please download them (by clicking on the corresponding links) and move them to the same directory, or
[download all the files as a zip](data/portal-teachingdb-master.zip)
which will give you everything in a single compressed file. You'll need to unzip
this file after downloading it.


::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::  prereq

## Installing Python and JupyterLab using Pixi

[Python][python] is a popular language for scientific computing, and great for
general-purpose programming as well. Installing all of the scientific packages we use in the lesson
individually can be a bit cumbersome, and therefore recommend using [Pixi](https://pixi.sh/latest/) by prefix.dev.

Regardless of how you choose to install it, please make sure you install Python
version 3.x (e.g., 3.10 is fine and will continue to receive security patches unitl 2026-OCT-04).


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::: discussion

## Installing Pixi

Select your operating system from the options below.

:::::::::::::::::::::::::::::::::

:::::::::::: solution

### Windows {#windows}

1. Open [https://pixi.sh/latest/installation/](https://pixi.sh/latest/installation/) in your web browser.

2. Under Installation, select Windows.

3. Open the Command Prompt, paste the following command, and press <kbd>Enter</kbd>.

  ```bash
  powershell -ExecutionPolicy ByPass -c "irm -useb https://pixi.sh/install.ps1 | iex"
  ```
  
4. Close your Command Prompt window.

::::::::::::

:::::::::::: solution

### MacOS & Linux {#macos-linux}

1. Open [https://pixi.sh/latest/installation/](https://pixi.sh/latest/installation/) in your web browser.

2. Under Installation, select "Linux & macOS".

3. Open the Terminal, paste the following command, and press <kbd>Return</kbd>.

  ```bash
  curl -fsSL https://pixi.sh/install.sh | sh
  ```
  
  If your system doesn't have curl, you can use wget:
  
  ```bash
  wget -qO- https://pixi.sh/install.sh | sh
  ```
  
4. Close your Terminal window.

::::::::::::



## Add Python and required libraries

Now that you've installed Pixi, we can install Python, JupyterLab, and the required libraries.

1. Open your Terminal or Command Prompt. Move to your Desktop folder. There, create a new project with Pixi, which we'll call python-intro

```bash
cd ~/Desktop
pixi init python-intro
```

2. Move intro your project and add Python as a dependency of your Pixi project

```bash
cd python-intro
pixi add python
```

3. Add also JupyterLab and the other required packages

```bash
cd python-intro
pixi add jupyterlab pandas numpy matplotlib
```

## Launch a Jupyter notebook

After installation, in the Terminal or Command Prompt you have open, launch a Jupyter notebook by typing this command:

```bash
pixi run jupyter lab
```

The notebook should open automatically in your browser. If it does not or you
wish to use a different browser, open this link: [http://localhost:8888](https://localhost:8888).

::: prereq :::::
## Leave terminal used to launch Jupyter open

Jupyter depends on a server running in the background associated with the window used to launch it. Closing that window will results in web interface errors in the web interface. When done, you can either close the terminal or shut down the server using <kbd>CTRL</kbd>+<kbd>C</kbd> and submitting <kbd>y</kbd> within 5 seconds if the terminal is needed for other tasks.

::::::::::::::::::::

For a brief introduction to Jupyter Notebooks, please consult our
[Introduction to Jupyter Notebooks](jupyter_notebooks.md) page.

[python]: https://www.python.org/
[anaconda]: https://www.anaconda.com/
[jupyter]: https://jupyter.org/




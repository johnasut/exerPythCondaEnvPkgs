# Setting up Environments and Installing Packages Using Conda

## Summary of steps to complete

- [ ] Fork this repository so you have your own copy to work on.
- [ ] Clone the repository on your local machine. 
- [ ] Edit this README.md file on your machine.
- [ ] Run the Conda commands shown in the video and describe them in the table below.
- [ ] Push your changes to your GitHub repository.
- [ ] Submit a link to this GitHub repository in Canvas.

## 1. Fork & Clone this repository

* We did this in a previous assignment. Instructions are here: https://github.com/cmcntsh/exerGitPractice
* This can also be done directly in VSCode
  * Create a new folder on your machine where you want to put this repository if you don't already have one you want to use.
  * Copy the Clone or Download path for this repository from GitHub.
  * In VSCode from the command pallette (Ctrl-Shift-P) run Git: Clone
  * Paste the path into the path field which pops up
  * Select your new folder you created on your machine
  * A new folder for the repository with the repository files should be in the folder you selected showing in the Explorer window in VSCode on the left side.
  
## Edit your README.md file

* [ ] In an editor of your choice (i.e. VSCode) edit this README.md file to add the answers requested in the tables.

## Follow along with this tutorial

* Conda What and Why? (27 min): https://www.youtube.com/watch?v=23aQdrS58e0&list=PLG9A6ovzPqX6d9uWzx0UYN9pm0zzl5ofA&index=13&t=0s
  * He installs Miniconda. We will be using Anaconda. Don't install Miniconda.
  * Follow along with the rest of the tutorial.
  * Go ahead and create the environments as he creates them in the tutorial.

## Conda Concepts

* [ ] Describe the Conda concepts used in the video and listed in the table below.

|   Concept   |         Description or short answer         |
|     ---     |                     ---                     |
|What is the purpose of having different environments?     |To allow work using different tools like packages or software versions that may be required for different projects without having to make changes to your computer every time you switch between projects.|
|What is the default package manager in Python?            |PIP|
|How do you manage environments and packages in Anaconda?  |Use Conda installed with Anaconda.|
|`conda list`       |Lists all packages installed with Conda in the environment you are currently using.|
|`conda env list`       |Lists all environments available.|
|How do you keep your base environment unchanged?       |Create a new virtual environment and conduct your tasks there.|
|What is the link to the Conda cheat sheet? (link in video notes is broken)      |https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf|
|`conda create --name XXXX`       |Creates new Conda environment named XXXX.|
|`source activate XXXX`       |Switch from whatever environment you are currently in to the XXXX environment (although mine seems to prefer the command `conda activate XXXX` for some reason.)|
|`conda install YYYY`       |Install the specified package into the active environment.|
|channels in Conda       |Where Conda is looking to find packages available for installation.|
|`conda install -c ZZZZ YYYY`       |Search the specific channel ZZZZ to find and install package YYYY. Does not remember this channel for future installations.|
|`conda config --show channels`       |List the channels Conda is currently searching when the `conda install YYYY` command is used.|
|`conda config --add channels ZZZZ`       |Add the channel ZZZZ to the list of channels Conda will search when the `conda install YYYY` command is used when installing packages in any environment.|
|conda-forge.org       |"A community led collection of recipies, build infrastructure, and distrbutions for the conda package manager." A channel with lots of custom packages that can be installed.|
|`source deactivate`       |In the video this returns the user to the base environment. Mine would only accept the command `conda deactivate` which instead returned me to the last environment active prior to the one I was in.|
|`conda config --get channels`       |List available channels along with their "priorities" or the order in which the channels are searched for packages. Important in case a higher priority channel has a different version of the package than the one you want. In this case, you would want to specify the installation using the `conda install -c ZZZZ YYYY` command.|

* After creating the environments he created in the video on your computer, what would the results of running the command `conda env list` look like with the da35 environment activated. Paste the output from your command prompt in the code block below.

```
# conda environments:
#
base                     C:\Users\John\Anaconda3
Playpen                  C:\Users\John\Anaconda3\envs\Playpen
ai37                     C:\Users\John\Anaconda3\envs\ai37
ai38                     C:\Users\John\Anaconda3\envs\ai38
da35                  *  C:\Users\John\Anaconda3\envs\da35
test                     C:\Users\John\Anaconda3\envs\test


```
* What command would you use to remove the environments you created for this exercise from your computer?

```
conda env remove --name XXXX

```

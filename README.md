# Geophysical modeling & inversion with pyGIMLi

![](https://i.imgur.com/J5ukNhT.png)


The [pyGIMLi tutorial at Transform 21](http://schedule.softwareunderground.org/)

Instructors:
[Florian Wagner]("") <sup>1</sup>, [Carsten Rücker]("") <sup>2</sup>, [Thomas Günther]("")<sup>3</sup>, [Andrea Balza]("")<sup>1</sup> ]

> <sup>1</sup>c University of Bonn, Steinmann Institute, Department of Geophysics, Bonn, Germany
> <sup>2</sup> Berlin University of Technology, Department of Applied Geophysics, Berlin, Germany
> <sup>3</sup> Leibniz Institute for Applied Geophysics, Hannover, Germany
><sup>4</sup> RWTH Aachen, Applied Geophysics and Geothermal Energy, Germany

|         | Info |
|--------:|:-----|
| When | Monday , April 19 • 8:00 - 9:00 UTC |
| Slack (Q&A) | [Software Underground](https://softwareunderground.org/) channel `t21-mon-pygimli` |
| Live stream | https://www.youtube.com/watch?v=HPxG5BgRf5g |
| conda environment  | `` |
| pyGIMLi documentation | https://www.pygimli.org/documentation.html |


## BEFORE THE TUTORIAL

Make sure you've done these things **before the tutorial on Monday**:

1. Sign-up for the [Software Underground Slack](https://softwareunderground.org/slack)
1. Join the channel `t21-mon-pygimli`. This is where **all communication will
   happen** and where we will answer any question about installation.

## About

*Information about the tutorial*


## Setup

There are a few things you'll need to follow the tutorial:

1. A working Python installation (Anaconda or Miniconda). For details on how to install Anaconda, we refer to: https://docs.anaconda.com/anaconda/install/
2. Install the pyGIMLi or tutorial  *environment*
3. A web browser that works with JupyterLab or Jupyter Notebook (Internet explorer will not work)

To start the tutorial setup, please follow the next steps:


### Step 1

**Install the tutorial environment:**

1. Open a terminal (Linux & Mac) or the Anaconda Prompt (Windows) and type:

```
conda create -n pg -c gimli -c conda-forge pygimli=1.1.0
```
If you are using Windows or Mac, type `conda env list ` in the same terminal to check if a a new environment named “pg” is listed. Exit out of this list to activate the environment.

2. Activate the environment in the terminal by typing: 

```
conda activate pg
```
After that you can use pygimli with your text editor of choice and a terminal.


### Step 2

**Testing:**

To test if everything works correctly you can do the following:

```
python -c "import pygimli; pygimli.test(show=False, onlydoctests=True)"
```

If none of these commands gives an error, then your installation should be working.
If you get any errors or the outputs look significantly different, please let us know on Slack at `#t21-mon-pygimli`.

### Step 3

**Start Jupyter notebook:**

1. Activate the conda environment: `conda activate pg` if you haven't done so already.
2. Start the Jupyter notebook server: type `jupyter notebook`
3. Jupyter should open in your default web browser. *start new noteboook or give them the notebook* 


# Tutorial on geophysical modeling & inversion with pyGIMLi

<div width="50%">
<img src="https://www.pygimli.org/_images/pg_logo.png" width=40%>
</div>

The [pyGIMLi tutorial at Transform 21](http://schedule.softwareunderground.org/)

Instructors:
[Florian Wagner](https://github.com/florian-wagner) <sup>1</sup>, [Carsten Rücker](https://github.com/carsten-forty2) <sup>2</sup>, [Thomas Günther](https://github.com/halbmy)<sup>3</sup>, [Andrea Balza](https://github.com/andieie)<sup>1</sup>

> <sup>1</sup> RWTH Aachen University, Applied Geophysics and Geothermal Energy, Aachen, Germany
> <sup>2</sup> Berlin University of Technology, Department of Applied Geophysics, Berlin, Germany
> <sup>3</sup> Leibniz Institute for Applied Geophysics, Hannover, Germany

|                       | Info                                                                                                                              |
| --------------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
|                  When | Monday, April 19 • 8:00 - 9:00 UTC (starts at 10.00 a.m. CET)                                                                     |
|           Slack (Q&A) | [Software Underground](https://softwareunderground.org/) channel [#t21-mon-pygimli](https://swung.slack.com/archives/C01T5V5S9EV) |
|           Live stream | https://youtu.be/w3pu0H3dXe8                                                                                                      |
| pyGIMLi documentation | https://www.pygimli.org/documentation.html                                                                                        |

## BEFORE THE TUTORIAL

Make sure you've done these things **before the tutorial on Monday**:

1. Sign up for the [Software Underground Slack](https://softwareunderground.org/slack)
1. Join the channel [#t21-mon-pygimli](https://swung.slack.com/archives/C01T5V5S9EV) channel. This is where **all communication will
   happen** and where we will answer any question about installation and the tutorial

## About

pyGIMLi is an open-souce librabry for modeling and inversion in geophysics. This tutorial is particularly suited for new users. We will start from scratch and:

- Create a subsurface geometry and explore the pyGIMLi meshtools
- Simulate the stationary 2D heat equation
- Simulate synthetic crosshole traveltime measurements
- Invert seismic traveltime and field ERT data
- Show how to build inversions with own forward operators (e.g., from other packages)

## Schedule

| Notebook # | Topic                                                    | Start Time (UTC) |
| ---------: | :------------------------------------------------------- | :--------------- |
|            | Intro (main features, conda installer, API doc)          | 8:00             |
|          1 | 2D meshtools demonstration                               | 8:10             |
|          2 | Equation level: 2D heat equation                         | 8:30             |
|          3 | Crosshole traveltime forward modeling                    | 8:40             |
|         \* | 10-MINUTE BREAK                                          | 8:55             |
|          4 | Method Manager: Traveltime inversion                     | 9:05             |
|          5 | Inversion settings: Geoelectric field data set with topo | 9:20             |
|          6 | Inversion with own forward operator                      | 9:40             |
|            | Homepage with examples, papers, contribution guide       | 9:50             |

## Setup

There are a few things you'll need to follow the tutorial:

1. A working Python installation (Anaconda or Miniconda). For details on how to install Anaconda, we refer to: https://docs.anaconda.com/anaconda/install/
2. pyGIMLi installation
3. A modern web browser that works with JupyterLab or Jupyter Notebook (Internet explorer will not work)
4. Tutorial material provided in this git repository

> ### Quick setup
>
> If you are working on Mac or Linux and have worked with conda before, you can copy & paste these lines. For all others, we recommend to carefully read the descriptions of individual steps below.
>
> ```bash
> conda create -n pg -c gimli -c conda-forge pygimli=1.2.0 notebook
> conda activate pg
> python -c "import pygimli; pygimli.test(show=False, onlydoctests=True)"
> git clone https://github.com/gimli-org/transform2021
> cd transform2021
> jupyter notebook
> ```

To start the tutorial setup, please follow the next steps:

### Step 1

**Install the tutorial environment:**

1. Open a terminal (Linux & Mac) or the Anaconda Prompt (Windows) and type:

```
conda create -n pg -c gimli -c conda-forge pygimli=1.2.0
```

Type `conda env list ` in the same terminal to check if a new environment named “pg” is listed. Exit out of this list to activate the environment. If you have miniconda, you might also need to `conda install -c conda-forge notebook`.

2. Activate the environment in the terminal by typing:

```
conda activate pg
```

After that you can use pyGIMLi with your text editor of choice and a terminal.

### Step 2

**Testing:**

To test if everything works correctly you can do the following:

```
python -c "import pygimli; pygimli.test(show=False, onlydoctests=True)"
```

If none of these commands gives an error, then your installation is working fine.
If you get any errors, please let us know on Slack at [#t21-mon-pygimli](https://swung.slack.com/archives/C01T5V5S9EV).

### Step 3

**Start Jupyter notebook:**

1. Activate the conda environment: `conda activate pg` if you haven't done so already.
2. Start the Jupyter notebook server: type `jupyter notebook`
3. Jupyter should open in your default web browser.
4. Download the notebooks provided in this git repository (if you are on Mac or Linux, you can do `git clone https://github.com/gimli-org/transform2021`)

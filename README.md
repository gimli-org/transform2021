# Geophysical modeling & inversion with pyGIMLi

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
|                  When | Monday, April 19 • 8:00 - 10:00 UTC                                                                                               |
|           Slack (Q&A) | [Software Underground](https://softwareunderground.org/) channel [#t21-mon-pygimli](https://swung.slack.com/archives/C01T5V5S9EV) |
|           Live stream | https://youtu.be/w3pu0H3dXe8                                                                                                      |
| pyGIMLi documentation | https://www.pygimli.org/documentation.html                                                                                        |

## About

pyGIMLi is an open-source library for modeling and inversion in geophysics. This tutorial is particularly suited for new users. We will start from scratch and:

- Create a subsurface geometry and explore the pyGIMLi meshtools
- Simulate the stationary 2D heat equation
- Simulate synthetic crosshole traveltime measurements
- Invert seismic traveltime and field ERT data
- Show how to build inversions with own forward operators (e.g., from other packages)

## Table of contents

- [Tutorial on geophysical modeling & inversion with pyGIMLi](#tutorial-on-geophysical-modeling--inversion-with-pygimli)
  - [About](#about)
  - [Table of contents](#table-of-contents)
  - [BEFORE THE TUTORIAL](#before-the-tutorial)
  - [Setup instructions](#setup-instructions)
    - [Step 1: Prerequisites](#step-1-prerequisites)
    - [Step 2: Download material for the tutorial](#step-2-download-material-for-the-tutorial)
    - [Step 3: Install the tutorial environment](#step-3-install-the-tutorial-environment)
    - [Step 4: Start JupyterLab](#step-4-start-jupyterlab)
  - [Schedule](#schedule)

## Foreword

This tutorial was presented on April 19, 2021 at Transform, but you can still follow it on YouTube and ask questions. To do so please:

1. Sign up for the [Software Underground Slack](https://softwareunderground.org/slack)
2. Join the channel [#pygimli](https://swung.slack.com/archives/C01US4T522X) channel to interact with other users and developers and ask questions with regard to the tutorial/software.
3. **Install the pyGIMLi conda environment** as described below.

## Setup instructions

> ### Quick setup for experienced users
>
> If you are working on Mac or Linux and have worked with conda and have git installed, you can copy & paste these lines separately. For all others, we recommend to carefully read the descriptions of individual steps below.
>
> ```bash
> git clone https://github.com/gimli-org/transform2021
> cd transform2021
> conda env create
> conda activate pg-transform
> python -c "import pygimli; pygimli.test(show=False, onlydoctests=True)"
> jupyter lab
> ```

To start the tutorial setup, please follow the next steps:

### Step 1: Prerequisites

There are a few things you'll need to follow the tutorial:

1. A working Python installation (Anaconda or Miniconda). For details on how to install Anaconda, we refer to: https://docs.anaconda.com/anaconda/install/
2. A modern web browser that works with JupyterLab or Jupyter Notebook (Internet explorer will not work)
3. Intermediate experience in Python programming (Python, numpy, matplotlib, jupyter)
4. Background on geophysical modeling and inversion

### Step 2: Download material for the tutorial

- Windows: [Download the course material](https://github.com/gimli-org/transform2021/archive/refs/heads/main.zip) and unzip it a folder of your choice.
- Mac/Linux: You can do the same as above, or alternatively open a terminal, navigate to a folder of your choice, and execute `git clone https://github.com/gimli-org/transform2021`.

### Step 3: Install the tutorial environment

1. Open a terminal (Linux & Mac) or the Anaconda Powershell Prompt (Windows). Navigate to the folder from step 2 (using the `cd` command) and type:

```
conda env create
```

2. Activate the environment in the terminal by typing:

```
conda activate pg-transform
```

3. To test if everything works correctly you can do the following:

```
python -c "import pygimli; pygimli.test(show=False, onlydoctests=True)"
```

If none of these commands gives an error, then your installation is working fine.
If you get any errors, please let us know on Slack at [#t21-mon-pygimli](https://swung.slack.com/archives/C01T5V5S9EV).

### Step 4: Start JupyterLab

1. **Windows users:** Make sure you set a default browser that is **not Internet Explorer**.
2. Activate the conda environment: `conda activate pg-transform`
3. Start JupyterLab: `jupyter lab`
4. Jupyter should open in your default web browser. We'll start from here in the
   tutorial and create a new notebook together.

## Schedule

> **Note**: Click on the notebook number to get to the respective notebook and the minutes to get to the respective position in the tutorial video.

| Notebook                                                                                                       | Topic                                                           | Time                                                           |
| -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------- |
|                                                                                                                | Intro (main features, conda installer, API documentation)       | [9 min.](https://youtu.be/w3pu0H3dXe8?t=10)                    |
| [1](https://github.com/gimli-org/transform2021/blob/main/1_Creating_a_subsurface_model.ipynb)                  | Creating a subsurface model (_2D meshtools_)                    | [22 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=570s)  |
| [2](https://github.com/gimli-org/transform2021/blob/main/2_Modeling_the_2D_heat_equation.ipynb)                | Modeling the 2D heat equation (_equation level_)                | [17 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=1870s) |
| [3](https://github.com/gimli-org/transform2021/blob/main/3_Simulating_a_crosshole_traveltime_experiment.ipynb) | Simulating a crosshole traveltime experiment (_modeling level_) | [15 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=2899s) |
|                                                                                                                | 10-MINUTE BREAK                                                 | 7 min.                                                         |
| [4](https://github.com/gimli-org/transform2021/blob/main/4_Traveltime_inversion.ipynb)                         | Traveltime inversion (_Traveltime method manager_)              | [10 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=4210s) |
| [5](https://github.com/gimli-org/transform2021/blob/main/5_ERT_field_data_inversion.ipynb)                     | ERT field data inversion (_ERTManager_)                         | [17 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=5447s) |
| [6](https://github.com/gimli-org/transform2021/blob/main/6_Inversion_with_any_forward_operator.ipynb)          | Inversion with any forward operator                             | [17 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=6438s) |
|                                                                                                                | Homepage with examples, papers, contribution guide              | [5 min.](https://www.youtube.com/watch?v=w3pu0H3dXe8&t=6950s)  |

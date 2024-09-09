---
title: "Python"
---

The most reliable way of installing Python is by using a package manager. First, follow the instructions on the [mamba installation page](mamba.md). Then return to this page.

After installing, run the following:

::: {.panel-tabset group="os"}
#### Windows 10/11

#### MacOS

* create and activate a new environment

```bash
mamba create --name jupyterlab
mamba activate jupyterlab
```

* install Jupyter lab

```bash
mamba install -c conda-forge jupyterlab
```

* start Jupyter lab

```bash
jupyter lab
```

#### Linux


* create and activate a new environment

```bash
mamba create --name jupyterlab
mamba activate jupyterlab
```

* install Jupyter lab

```bash
mamba install -c conda-forge jupyterlab
```

* start Jupyter lab

```bash
jupyter lab
```

:::

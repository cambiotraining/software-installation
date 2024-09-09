---
title: "Python"
---

The most reliable way of installing Python is by using a package manager. For all our courses we use *Mamba*. Run the following commands (which will install *miniforge*, which also includes a default Python installation):

::: {.panel-tabset group="os"}
#### Windows 10/11

#### Mac OS X

#### Linux

```bash
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3-$(uname)-$(uname -m).sh -b -p $HOME/miniforge3
rm Miniforge3-$(uname)-$(uname -m).sh
$HOME/miniforge3/bin/mamba init
```

:::

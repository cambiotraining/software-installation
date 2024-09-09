---
title: "conda/mamba"
---

For all our courses we use *Mamba*.

::: {.panel-tabset group="os"}
#### Windows 10/11

#### MacOS

Before we can install mamba, we need to install two other things:

1. Apple's Command Line Developers Tools

```bash
 xcode-select --install
 ```
 
2. Bash

Install [MacPorts](https://www.macports.org/install.php), then run the following, saying yes to any dependencies it suggests:

```bash
sudo port install bash
```

**Installing mamba**

Run the following commands from the terminal (this will install it in its default location in the home directory): 

```bash
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3-$(uname)-$(uname -m).sh -b -p $HOME/miniforge3
rm Miniforge3-$(uname)-$(uname -m).sh
$HOME/miniforge3/bin/mamba init
```

Restart your terminal.

Your shell should now start with the word `(base)`.

Then run the following commands: 

```bash
conda config --add channels defaults; conda config --add channels bioconda; conda config --add channels conda-forge
conda config --set remote_read_timeout_secs 1000
```

#### Linux

To install _Mamba_, run the following commands from the terminal (this will install it in its default location in the home directory): 

```bash
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3-$(uname)-$(uname -m).sh -b -p $HOME/miniforge3
rm Miniforge3-$(uname)-$(uname -m).sh
$HOME/miniforge3/bin/mamba init
```

Restart your terminal.

Your shell should now start with the word `(base)`.

Then run the following commands: 

```bash
conda config --add channels defaults; conda config --add channels bioconda; conda config --add channels conda-forge
conda config --set remote_read_timeout_secs 1000
```
:::
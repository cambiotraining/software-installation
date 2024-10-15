---
pagetitle: "Software installation"
---

# macOS

## Xcode Command Line Tools

We recommend installing the Xcode Command Line Tools, which makes several useful software utilities available.

Open a terminal and run:

```bash
xcode-select --install
```

## Homebrew

On macOS the `brew` package manager is a popular choice for installing packages as a user. 
Note that for research work we recommend [using Mamba](mamba.md) for managing software environments, but for general utilities `brew` is a good solution. 

First, make sure to install Xcode as instructed in the previous section.
Then, open a terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Test your `brew` installation by installing the `wget` utility, which is used to download files from the web:

```bash
brew install wget
```
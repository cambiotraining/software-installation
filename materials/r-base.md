---
pagetitle: "Software installation"
---

# R

To run R, we need to install R (the programming language). We also install RStudio, which acts as a graphical interface for R.

::: {.panel-tabset group="os"}

#### Windows 10/11

You can install R and RStudio using `winget`. 
Click the Windows key and search for  _Windows PowerShell_, right-click on the app and choose **Run as administrator**. 
Then run the following commands: 

```powershell
winget install --id=RProject.R -e
winget install --id=RProject.Rtools -e
winget install --id=Posit.RStudio -e
```

Alternatively, you can manually download and install these programs using default options:

- [R](https://cran.r-project.org/bin/windows/base/release.html)
- [RTools](https://cran.r-project.org/bin/windows/Rtools/)
- [RStudio](https://www.rstudio.com/products/rstudio/download/#download)

#### macOS

If you followed our [macOS system setup instructions](macos.md), you can install R and RStudio using `brew`. 
Open a terminal and run:

```bash
brew install --cask r
brew install --cask rstudio
```

Alternatively, you can manually download and install these programs using default options:

- [R](https://cran.r-project.org/bin/macosx/)
- [RStudio](https://www.rstudio.com/products/rstudio/download/#download)

#### Linux

- Go to the [R installation](https://cran.r-project.org/bin/linux/) folder and look at the instructions for your distribution.
- Download the [RStudio](https://www.rstudio.com/products/rstudio/download/#download) installer for your distribution and install it using your package manager.

:::
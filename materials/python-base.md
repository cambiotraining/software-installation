---
pagetitle: "Software installation"
---

# Python

We recommend using the package manager Mamba to manage your Python installation and environments. 
Our recommendation is to create separate environments for each project or type of analysis, to avoid package version conflicts. 
In this page we give an example of creating an environment for our Python introduction course, which includes JupyterLab. 

:::{.callout-important}
#### First install Mamba

Follow the instructions on the [mamba installation page](mamba.md). 
Then return to this page.
:::

* Open a terminal:
  * macOS and Linux - open your regular terminal
  * Windows - open the Miniforge prompt or WSL terminal (if you followed the [WSL setup instructions](wsl.md))
* Ensure that the prompt starts with the word `(base)`, indicating Mamba is correctly installed.
* Create a new environment, which we will call `pycourse` (you may give your environment a name of your choice):

    ```bash
    mamba create -n pycourse
    ```

* Install JupyterLab (for notebook interface):

    ```bash
    mamba install -y -n pycourse jupyterlab
    ```

* The installation should complete with the following message: 

    ```
    Downloading and Extracting Packages

    Preparing transaction: done
    Verifying transaction: done
    Executing transaction: done
    ```

## Initiate JupyterLab

Once installed, you can start JupyterLab by activating your environment and running the command to launch it:

```bash
mamba activate pycourse
jupyter lab
```

JupyterLab should open in your browser automatically. 
If it doesn't, you can click the link that appears on the message printed on the screen:

![](images/jupyterlab_launch.png)

By default, JupyterLab will open in the directory where you launch it from. 
If the files you are interested in working with are in a different directory, you need to change to that directory first. 

For example, let's say you had a folder in your Desktop called `intro-python`. 
To open JupyterLab in that folder, you would first `cd` into it, and then run the `jupyter lab` command.
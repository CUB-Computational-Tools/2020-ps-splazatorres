# Binder

[This repo](https://github.com/CUB-Computational-Tools/assignment_problem_set) contains a set of [binder](https://mybinder.readthedocs.io) settings to run R and python in RStudio and Jupyter Lab. The R / python environments are configured in the `binder-R`, `binder-python`, and `binder-R+python` branches, respectively (instructions below). The notebooks and data that provide content can be stored in any branch. To launch a problem set in RStudio/Jupyter, the relevant link can be constructed using the short R script below and provided to students in any LMS, HTML or markdown file.

## Binder Setup

Binder will create a virtual server setup (a docker image) based on the `binder-R`, `binder-python`, or `binder-R+python` branch the first time you launch a binder and after every time the configuration in these branches changes. If nothing in the config branches changes, binder will simply re-use the docker image. This means that the first time you launch a problem set, it may take some time but will be fast for everyone else afterwards. For this reason you should always test-run a problem set on binder before giving out the link.

**Important**: binder will *only* work for public repositories. If a repository is private, you will have to make it public in the repository settings before you can launch it in binder. If you need to, you can turn a repository public just before students use it (leave enough time to start the binder environment for the first time), and then make it private again after use.

### R setup

The default R version is from a specific date and snapshot available on the [MRAN](https://mran.microsoft.com/documents/rro/reproducibility) network (keeps daily snapshots of CRAN). To use a different R version, simply change the date listed in the `binder/runtime.txt` file of the `binder-R` branch. The default R setup includes `rmarkdown` and the `tidyverse` but it is easy to install additional packages: in the `binder-R` branch, modify the `binder/install.R` file to make sure all dependencies are specified. Dependencies can be from CRAN, bioconductor or GitHub. Since GitHub hosted libraries can change without notice, it is best to specify a commit or release tag to ensure that a compatible version of the package is installed in the binder. 

Alternatively to modifying `binder-R`, you can make a new `binder-R-xxx` branch off of the `binder-R` branch to create a completely separate configuration thus keeping the original intact. Both can be used as needed simply by specifying the correct branch in the problem set link.

### Python setup

The default python setup includes the latest stable python release and the `matplolib`, `numpy` and `pandas` libraries but it is easy to install additional ones: in the `binder-python` branch, modify the `binder/environment.yml` file to specify the dependencies. The file is a standard [conda environment config file](https://conda.io/docs/user-guide/tasks/manage-environments.html#create-env-file-manually) and thus supports conda packages, version definitions, multiple source channels as well as pip installations. Additionally you can modify the `binder/postBuild` file for any JupyterLab extensions or other direct install commands.

Alternatively to modifying `binder-python`, you can make a new `binder-python-xxx` branch off of the `binder-python` branch to create a completely separate configuration thus keeping the original intact. Both can be used as needed simply by specifying the correct branch in the problem set link.

### R + Python setup

To use both languages in the same problem set or to use python in RStudio, use the `binder-R+python` branch. The configuration instructions to change libraries and packages are the same as described above. Note that the R configuration in this setup is fairly minimal since this branch is more commonly used for python in RStudio. However, additional R libraries can be easily added (as always, the more is included, the longer the binder will take to generate the first time).

## Content Setup

The notebooks and any data files a problem itself can be stored in any branch. The `master` branch has a few example files (both ipython notebooks and RMarkdown notebooks) and is used in the example links below. You can add your own notebooks to the master branchor create an entirely new branch. If you require specialized python libraries or R packages, make sure to update your binder setup in the configuration branch you are using (`binder-R`, `binder-python`, or `binder-R+python`) so all the necessary functionality is available to use in your notebooks. Once your binder setup is finalized, you can still change the content branch(es) as much as you need and simply relaunch the Jupyter or RStudio platforms to get the latest notebooks from the content branch(es).

Important note: the output of Jupyter notebooks is usually saved in the notebook itself and becomes part of the repository on GitHub if committed. For a problem set you usually do not want any output already in the notebooks when students open them. To avoid this, you can run `jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace *.ipynb` in the terminal in your repository folder or simply open the `cleanup.ipynb` notebook in the master branch and run the code chunk in it (same command). This will remove the output in all Jupyter notebooks that are in the folder. Make sure to re-commit the cleared notebooks to your repository content branch. This is not an issue with RMarkdown files (they do not store output).

## Launch Links

The below R fuctions are intended to simplify construction of the launch links for your problem set. Simply copy the functions into an R console to create them and then call them as shown in the examples below to create launch links for your desired binder configuration, IDE, content branch, and link text.

```r
# functions
create_badge_url <- function(left = "launch", right = "binder", color = "red") {
  sprintf("https://img.shields.io/badge/%s-%s-%s.svg", URLencode(left), URLencode(right), color)
}
create_binder_url <- function(org, repo, binder_branch, content_branch, ide = c("nb", "lab", "rstudio"), file = NULL) {
  ide <- match.arg(ide)
  if (!is.null(file)) 
    ide_url <- if(ide == "nb") sprintf("tree/%s/%s", repo, file) 
      else if (ide == "lab") sprintf("lab/tree/%s/%s", repo, file) else ide
  else
    ide_url <- if(ide == "nb") "" else ide
  repo_url <- sprintf("https://github.com/%s/%s&branch=%s&urlpath=%s", 
                      org, repo, content_branch, ide_url)
  sprintf("https://mybinder.org/v2/gh/%s/%s/%s?urlpath=git-pull?repo=%s", 
          org, repo, binder_branch, URLencode(repo_url, reserved = TRUE))
}
create_binder_link <- function(binder_url, badge_url) {
  sprintf("<a href='%s'><img src='%s'/></a>", binder_url, badge_url)
}
```

### Python in Jupyter Lab

Running the following code creates this link for the template repository. Click on it to launch the template repository master branch in Jupyter Lab with a python configuration:

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch-Py+Jupyter%20Lab-red.svg'/></a>

```r
create_binder_link(
  create_binder_url(
    org = "CUB-Computational-Tools", # change if your repo lives elsewhere
    repo = "assignment_problem_set", # change to the name of your repository
    binder_branch = "binder-python", # use the python binder configuration
    content_branch = "master", # change to content branch you want to use
    ide = "lab" # use the Jupyter Lab IDE
  ),
  create_badge_url(
    left = "launch", # change to adjust link text
    right = "Py+Jupyter Lab", # change to adjust link text
    color = "red" # change to adjust link color
  )
)
```

### R in RStudio

Running the following code creates this link for the template repository. Click on it to launch the template repository master branch in RStudio with an R configuration:

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch-R+RStudio-blue.svg'/></a>

```r
create_binder_link(
  create_binder_url(
    org = "CUB-Computational-Tools", # change if your repo lives elsewhere
    repo = "assignment_problem_set", # change to the name of your repository
    binder_branch = "binder-R", # use the R binder configuration
    content_branch = "master", # change to content branch you want to use
    ide = "rstudio" # use the RStudio IDE
  ),
  create_badge_url(
    left = "launch", # change to adjust link text
    right = "R+RStudio", # change to adjust link text
    color = "blue" # change to adjust link color
  )
)
```

### R in Jupyter Lab

Running the following code creates this link for the template repository. Click on it to launch the template repository master branch in Jupyter Lab with both python and R configuration (you could also run this with the `binder-R` configuration only but it's usually helpful, though not necessary, to have a few basic python libraries when running in Jupyter):

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch-R+Jupyter%20Lab-orange.svg'/></a>

```r
# binder link example
create_binder_link(
  create_binder_url(
    org = "CUB-Computational-Tools", # change if your repo lives elsewhere
    repo = "assignment_problem_set", # change to the name of your repository
    binder_branch = "binder-R", # use the R+python binder configuration
    content_branch = "master", # change to content branch you want to use
    ide = "lab" # use the Jupyter Lab IDE
  ),
  create_badge_url(
    left = "launch", # change to adjust link text
    right = "R+Jupyter Lab", # change to adjust link text
    color = "orange" # change to adjust link color
  )
)
```

### Python in RStudio

Running the following code creates this link for the template repository. Click on it to launch the template repository master branch in RStudio with both python and R configuration.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch-Py+RStudio-purple.svg'/></a>

```r
create_binder_link(
  create_binder_url(
    org = "CUB-Computational-Tools", # change if your repo lives elsewhere
    repo = "assignment_problem_set", # change to the name of your repository
    binder_branch = "binder-R+python", # use the R+python binder configuration
    content_branch = "master", # change to content branch you want to use
    ide = "rstudio" # use the RStudio IDE
  ),
  create_badge_url(
    left = "launch", # change to adjust link text
    right = "Py+RStudio", # change to adjust link text
    color = "purple" # change to adjust link color
  )
)
```

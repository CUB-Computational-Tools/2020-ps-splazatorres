# Problem Sets

This is the repository for designing your weekly problem sets. Clone it to your desktop and keep it synchronized with GitHub for peer feedback and submissions.

## Before you Start

Before you start using this repository, please edit the README.md file of your repository in the text editor of your choice and replace all instances of the word `assignment_problem_set` (the name of the template repo) with the name of your own repository.

# Instructions

To design a new problem set, follow the instructions below:

## Setup the problem set

Before you start designing your problem set for any given week, please complete the following steps. Make sure to do this every week with the appropriate branch name for the week (`week1`, `week2`, etc.):

1. Create a new branch called `weekX` (X=1,2,3,..., e.g. `week1`).
1. Create a new pull request from `weekX` back to the `master` branch. This is the pull request for peer feedback and it will stay open until you finalize your work, only merge once you are certain you want to submit your final version for grading.
1. Synchronize the repository with your desktop and make sure to switch to the new `weekX` branch for the new problem set (NOT `master` or a previous week's branch).
1. Copy one of the `blank_` template files to create a new notebook for this week's problem set (name it `weekX.Rmd` or `weekX.ipynb`).
1. In README.md, remove all but one of the links from the `Binder link for peer reviewers` and `Binder link for final version` sections for the relevant week [below](#week-1) (i.e. decide whether you want to work in R or python and whether to work in RStudio or Jupyter this week).
1. Test-launch your binder for peer reviewers by clicking on the remaining binder link for this section (leave the tab open in the background, this may take quite a while because your binder server is built from scratch the first time - note: you can reload the page after ~1 hour if it's stuck).

## Draft the problem set

1. Design your problem set draft by editing the problem set file (`weekX.Rmd` or `weekX.ipynb`). If you are working in Jupyter, make sure to always clear the output in the notebook **before** committing changes to git. There are two ways to do this: you can run the code block in the `cleanup.ipynb` notebook, or you can do this in your problem-set notebook by selecting Cell => All Output => Clear.
1. Make sure the binder link for peer reviewers below works for interacting with your draft problem set. Note that if you are using functionality from non-standard libraries other than `numpy`, `matplotlib`, and `pandas` in python or the [`tidyverse`](https://www.tidyverse.org/) packages in R, you may have to modify the binder configuration in the relevant `binder-` branch for your problem set to work on binder. If this is case, take a look at the [`BINDER.md`](BINDER.md) file and ask an instructor for help if you get stuck.
1. During next class, your peer reviewers will use the binder link below to interact with your draft problem set and will use the pull request to provide feedback.

## Complete problem set

1. Update your problem set based on peer feedback. If you are working in Jupyter, make sure to always run the code block in the `cleanup.ipynb` notebook, or clear output in your problem set notebook directly, **before** committing changes to git.
1. Create an answer key named `weekX_answers.Rmd` or `weekX_answers.ipynb` that provides example answers for all questions you pose in your problem set. If you are working in Jupyter, again make sure to clear all output **before** committing changes to git.
1. Make sure the answer key runs completely without error in the binder for the peer reviewers (that means it will also work in the final version).
1. Optional: ask a peer reviewer to take another look before merging the pull request.
1. Once ready, merge the pull request into the master branch. Double check that the binder link for the final version works as well.

# Week 1

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week1` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek1%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek1%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek1%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek1%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# Week 2

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week2` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek2%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek2%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek2%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek2%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# Week 3

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week3` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek3%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek3%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek3%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek3%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# Week 4

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week4` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek4%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek4%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek4%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek4%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# Week 5

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week5` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek5%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek5%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek5%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek5%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# Week 6

#### Binder link for peer reviewers

> Only keep the one link you want your peer reviewers to use. Note that these will only work once the `week6` branch exists.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek6%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek6%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek6%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20draft-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dweek6%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20draft-Py+RStudio-purple.svg'/></a>

#### Binder link for final version

> Instructions: Only keep the one link you want your instructor(s) to use. This uses the `master` branch so will only have your newest notebook once you have merged your pull request for the week.

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-Py+Jupyter%20Lab-red.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-R+RStudio-blue.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Dlab'><img src='https://img.shields.io/badge/launch%20final-R+Jupyter%20Lab-orange.svg'/></a>

<a href='https://mybinder.org/v2/gh/CUB-Computational-Tools/assignment_problem_set/binder-R+python?urlpath=git-pull?repo=https%3A%2F%2Fgithub.com%2FCUB-Computational-Tools%2Fassignment_problem_set%26branch%3Dmaster%26urlpath%3Drstudio'><img src='https://img.shields.io/badge/launch%20final-Py+RStudio-purple.svg'/></a>

# ekvip Coding Ninjas Standard - Recipe Handling Library for TwinCAT Build 4026

<a name="toc"></a>
## Table-Of-Contents

1. [Table Of Contents](#toc)
2. [Summary](#summary)
3. [Folder Structure](#structure)
4. [Branches](#branches)
5. [Version Number Format](#versioform)
6. [Contribution](#contribution)
7. [Version Log](#version)

<a name="summary"></a>
## Summary

* project description: This is a TwinCAT 3 library project for recipe handling and machine settings. It is intended to be used with CNM HMI framework to store and load parameters. 
* For required software and tools, visit the confluence page:
* [confluence page](https://ekvip.atlassian.net/wiki/spaces/CNM/pages/2498002983/CNM_RecipeHandling)
* [gitlab project page](https://ekv-app-git-p01.ekvip.de/CNMTC3/cnm4026/cnm4026-recipehandling)


<a name="structure"></a>
## Folder-Structure

*   **.\\**
*   **build\\** _contains the actual library files_
*   **src\\** _root folder for all project sources_
*   **test\\** _contains project sources for all test libraries_
*   **.gitignore**  _the git ignore file for this project_
*   **.gitattributes** _the git attribute file for the LFS support_
*   **README.md** _the file you read right now_

<a name="branches"></a>
## Branches

The repository has some branches to allow collaboration on a centralized repository, and give everybody the possibility to orient onself. We've two main branches, we use this two to branch from and merge to.

> **The Main Branches Are:**
> -   **master**  _here are  **only**  our well tested releases_
> -   **develop**  _this is the choice for new features during the normal project work_

### creating Branches

The initial master commit contains the reworked readme.md, .gitignore and .gitattributes files.
We **only** use the Jira project-tasks (only sub tasks) to create branches. You can choose between **feature** and **hotfix** branches in the Jira menu. To create a branch in Jira, choose the task you want to create a branch for and click on **"Create branch"** at the tab **"Development"** in the task view.

Here are two examples:  **feature/FRINST-14-analogvalueprocessing/efro**  (here is Elias Froschauer working on feature analogvalueprocessing in project FRINST) and  **_hotfix/FRINST-15-analogvalueprocessingbug/toel_**  (here is Tino working on a hotfix for the bug in analog value processing after production release). 

### creating Tags
Every time you finish a task and merge a branch back to the develop or master, then you have to fill out the version log here and you've to tag this commit with the prefix ***"version_"*** and the version number.
If you work in a group and the current online version is not the latest master or develop commit, you will need to tag the currently used branch with **"online"**.

<a name="versionform"></a>
## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

## Version-Number-Format

The version number format for this project has following pattern: ***{major release}.{minor release}.{development state}{maintenance}***. Before the software is deployed to the machine, the major number is zero, if the software is deployed and tested 1st time the major number increase to one.

> **Version Number Format Description:**

> -   **major release**  _marks api changes_
> -   **minor release**  _marks functional extensions or changes but api is still compatible_
> -   **build**  _**odd** number is beta state,  **even**  is stable release
> -   **revision**  _shows the number of patches and hotfixes_

Some examples:

-   **0.0.0.0**  _initial commit_
-   **0.3.0.7**  _add some features and some bug fixes, software is still in alpha state_
-   **0.3.2.9**  _two more bug fixes and the software is now in release state_
-   **1.0.4.15**  _the api has been changed, this needs changes in the used software as well_

<a name="contribution"></a>
## Contribution

-   The language of software and software comments is **English** and software documentation is **English**
-   Use **branch** and **tag** **rules** as defined earlier
-   If you extend or change the folder structure, then you have to **update this file**
-   You have to provide a **version description** with a small change log for every version tag within this file in the version log section
-   If you want to merge you software to the master branch, then you have to take care that your software is compiling  **without warnings and errors**.
-   If you edit this file you've to do it in **English** and to use the **markdown** format
-	It is **not** allowed to work in one of the main branches directly
-	It is **only** allowed to work in your own branches (with your ekvip name acronym)
-	Every commit to feature or hotfix branch needs to contain the **Jira task id** before the commit description

<a name="version"></a>
## Version-Log

### Versions 
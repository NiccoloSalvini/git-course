---
description: "Workflow Collaborativo per Git e Rstudio"
title: Workflow di Git e Rstudio
output:
  html_document:
    toc: true
    toc_depth: 2
    toc_float: true
---

------------------------

# Prima di cominciare a Lavorare/collaborare

------------------------

## STEP 1: Aggiorna il tuo codice

**Scegli l'opzione:**

### OPZIONE 1A: *Farò un nuovo branch su cui lavoro*  
Crea un nuovo _branch_ con un nome evocativo della funzione che vuoi aggiungere o modificare.

Make sure you are working on the master branch:
![](./static/images/workflow_rstudio_1.png)

Update the master branch to make sure it is aligned with the remote master: Click `Pull`:
![](./static/images/workflow_rstudio_2.png)

Create a new branch: click on `New branch` and fill in a branch name:
![](./static/images/workflow_rstudio_2b.png)

### OPTION 1B:  *I already have a branch I want to continue working on*:  

Switch to existing topic branch:
![](./static/images/workflow_rstudio_3.png)

Update the topic branch to make sure is is aligned with the remote master: 
In the Git shell, type:
```
git pull origin master
```
![](./static/images/workflow_rstudio_4.png)


------------------------

# WHILE EDITING

------------------------

## STEP 2.x: adapt in md, R-code,... (multiple times!)

### Add new files

Stage the new file with checkbox and click `Commit`
![](./static/images/workflow_rstudio_5.png)

Provide clear and understandable message about adaptations
![](./static/images/workflow_rstudio_6.png)

### Change files:

Stage the adaptations with checkbox and click `Commit`
![](./static/images/workflow_rstudio_7.png)

Provide clear and understandable message about adaptations
![](./static/images/workflow_rstudio_8.png)


## STEP 3: Push your changes to GitHub.

Update the remote version of the topic branch. Click `Push`:
![](./static/images/workflow_rstudio_9.png) 

------------------------

# EDITS ON BRANCH ARE READY

------------------------

## STEP 4: Pull request to add your changes to the current master. 

Update the remote version of the topic branch. Click `Push`:
![](./static/images/workflow_rstudio_9.png)

Go to your repo on Github.com and click the `Compare & pull request` button. 

![](./static/images/workflow_rstudio_github_1.png)

Add information about the Pull request, add reviewers, labels,... Finally, `Create pull request`:
![](./static/images/workflow_rstudio_github_2.png)

## STEP 5: Code review!

You and collaborators can make comments about the edits, review the code and adapt if required (create additional commits and `Push` them to GitHub) .

If everything is ok, click the  `Merge pull request`:

![](./static/images/workflow_rstudio_github_3.png)

followed by `Confirm merge`:

![](./static/images/workflow_rstudio_github_4.png)

Delete the online branch after merge, since obsolete, click `Delete branch`

![](./static/images/workflow_rstudio_github_5.png)

## STEP 6: Update the master branch on my PC

Make sure you are working on the master branch:
![](./static/images/workflow_rstudio_1.png)

Remove the local branch, since obsolete. In the Git shell, type:
```
git branch -d analysis-script
```
![](./static/images/workflow_rstudio_4.png)

Update the local master branch: Click `Pull`:
![](./static/images/workflow_rstudio_2.png)

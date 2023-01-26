# Git_Assignment
This is my Git Assignment
In 3rd step,Making some changes from Feature_2 Branch-rebase step

Step 6:Making some more changes From Feature_1_

Step 7:Making some changes From HotFix Branch


# Assignment Description:
### Step 1:
* First I created the empty folder name Git_Assignment in my local environment and then initialized the empty git repository.
* Then I created the repository on remote environment name ***Git_Assignment*** with README.md file and then linked my local repository with the remote repository using Git command (**git remote add origin https://github.com/Karan2291/Git_Assignment.git**) and pulled the README.md to our local repository.
* Now,I set the tracking of my local main branch to remote origin main branch using git command **(git push -u origin main)**,here -u flag helps in tracking.
### Step 2:
* Now in the local environment, in the Production Branch .i.e,**main branch** I created two more brances **HotFix Branch** and **Integration Branch** which is branching out from the **main branch** using git command (**git checkout -b HotFix** and **git checkout -b Integration**) which will create the branches and switch to that branch automatically.
* Then I push the branches to the origin in the remote repository using git command **(git push -u origin HotFix)** and **(git push -u origin Integration)** ,now again -u for setting the tracking of local branch to the origin remote branch
### Step3:
* Now,in my local environment,in the Integration Branch I created two sub branches name **Feature_1** and **Feature_2** branching out from **Integration** Branch.
### Step4:
* Now again in my local environment,switching to **Feature_2** Branch and commiting some changes in the **README.md** file.
* Now pushing the changes in the remote origin using git command **(git push -u origin Feature_2)** and creating the pull request and adding two reviewers, Mahesh and Ratinder and got my PR reviewed and merged it into **Integration branch**.
* Now as **Feature_2** is merged into the **Integration Branch**,we delete the Feature_2 Branch locally using git command (**git branch -d Feature_2**).Now remotely our Feature_2 is still present,so for deleting the remote Feature_2 branch through local environment we use git command (**git push origin :Feature_2**),This will delete the Feature_2 branch from the remote.
### Step5:
* Now in local environment,switching to **Feature_1** branch,we commit some changes in the README.md file in the Feature_1 branch and did a ***rebase*** of Feature_1 branch to the Integration Branch using **git rebase** command which will put forward our local commits ahead of previous commits.
* While rebasing,a conflict arised in the README.md file which I solved using **git mergetool** which open up a default **P4Merge tool** which gives us the flexibility to resolve conflicts.
* And to continue with rebasing step, I used the command (**git rebase --continue**)
### Step6:
Now in remote/origin,I created two pull request to merge **Integration branch** to **HotFix Branch and Production Branch(Main Branch)**
* To merge **Integration** branch to **HotFix** Branch, I set the **base** to **HotFix** branch and **compare** to **Integration** branch, then added two reviewers and created a pull request,then got my PR reviewed and merged it into HotFix Branch.
* Now Similarly, to merge **Integration** branch to **Production(main)** branch I created a pull request with **base** as **main** branch and **compare** as **Integration** branch,then again added two reviewers and got my PR reviewed and merged it into **main Branch**.
* Now changes is reflected on both my **HotFix** and **main** branch remotely.
* Now the changes is done in **remote repositories** main and HotFix Branch but its not relecting in **local repositories** main and HotFix Branch.To update the local repository to get upto date with origin/main and origin/HotFix, we pull the changes using git command (**git pull origin HotFix**) and (**git pull origin main**) in the respective banches.
### Step7:
Now in our local environment,switching to **Feature_1** branch we again commit some changes in README.md file of Feature_1 Branch and push the changes in the remote origin using git command **(git push -u origin Feature_1)**
Now I created 3 pull request to merge **Feature_1** to (**HotFix**, **Integration** and **main**) branch, one pull request for each merge to different branch
* To merge **Feature_1** branch to **HotFix** Branch, I set the **base** to **HotFix** branch and **compare** to **Feature_1** branch, then added two reviewers and created a pull request,then got my PR reviewed and merged it into HotFix Branch.
* To merge **Feature_1** branch to **Integration** Branch, I set the **base** to **Integration** branch and **compare** to **Feature_1** branch, then added two reviewers and created a pull request,then got my PR reviewed and merged it into Integration Branch.
* Now Similarly, to merge **Feature_1** branch to **Production(main)** branch I created a pull request with **base** as **main** branch and **compare** as   **Feature_1** branch,then again added two reviewers and got my PR reviewed and merged it into **main Branch**.
* Now changes is reflected on all **HotFix** ,**Integration** and **main** branch remotely.
* Now the changes is done in **remote repositories** HotFix,Integration and main Branch but its not relecting in **local repositories** HotFix,Integration and main Branch.To update the local repository to get upto date with origin/HotFix, origin/Integration ans origin/main, we pull the changes using git command (**git pull origin HotFix**),(**git pull origin Integration**) and (**git pull origin main**) in the respective banches.
### Step8:
* Now as **Feature_1** is merged into the **HotFix Branch**,**Integration Branch** and **main Branch**,we delete the Feature_1 Branch locally using git command (**git branch -d Feature_1**).Now remotely our Feature_1 is still present,so for deleting the remote Feature_1 branch through local environment we use git command (**git push origin :Feature_1**),This will delete the Feature_1 branch from the remote.
### Step9:
Now in our local environment,switching to **HotFix branch** we again commit some changes in README.md file of HotFix Branch and push the changes in the remote origin/HotFix.
Now I created 2 pull request to merge **HotFix** to (**Integration** and **main**) branch, one pull request for each merge to different branch
* To merge **HotFix** branch to **Integration** Branch, I set the **base** to **Integration** branch and **compare** to **HotFix** branch, then added two reviewers and created a pull request,then got my PR reviewed and merged it into **Integration** Branch.
* Now Similarly, to merge **HotFix** branch to **Production(main)** branch I created a pull request with **base** as **main** branch and **compare** as   **HotFix** branch,then again added two reviewers and got my PR reviewed and merged it into **main** Branch.
* Now changes is reflected on both **Integration** and **main** branch remotely.
* Now the changes is done in **remote repositories** Integration and main Branch but its not relecting in **local repositories** Integration and main Branch.To update the local repository to get upto date with origin/Integration ans origin/main, we pull the changes using git command (**git pull origin Integration**) and (**git pull origin main**) in the respective banches.

## Screenshot of Graph for the entire commit History
<img width="794" alt="Screenshot 2023-01-26 at 11 48 51 AM" src="https://user-images.githubusercontent.com/122456892/214770418-6ea61234-2587-4d9d-bc1b-224ef95fb3a9.png">

## Diagramatic Representation
<img width="850" alt="Screenshot 2023-01-26 at 11 53 05 AM" src="https://user-images.githubusercontent.com/122456892/214771159-8c3f7d3e-e18a-4c06-b714-19314d943a76.png">





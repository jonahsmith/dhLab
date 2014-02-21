##Digital Humanities Lab, 2.18.2014
#Git Basics

Git: a model of versioning syncronization

GitHub: a centralized server running Git. Also has a wiki feature and a bug tracker

##The General Workflow
Command		| Description
----------------|-------------
git init 	| initiate a repository
git add 	| adds to staging area
git commit 	| commit to ledger of changes
		|
git push 	| synchronize to the cloud
		|
git clone	| clones repository into new directory
git pull 	| gets the timeline from the cloud

##Some Terminology
"He advanced the head": changed the file, staged it, committed it, and pushed it to common ledger

##Initializing and connecting to GitHub
```
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/[]
git push -u origin master
```

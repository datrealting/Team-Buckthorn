# Team Buckthorn

Hello! It's only taken me an agonising 6 failed repositories but we finally have UE5 working with Git.
Below, I'm gonna give a quick 'n' simple guide on what Git and Github is, starting with the important bits then going into a bit of the further reading.

Just a quick note - I don't claim to know everything there is to know about Git + Github, so if there are gaps in this, ask me (I might have just missed it out for brevity) or look it up online.

### Necessary Software
There is only **1** bit of software you'll need before we go on, and that is Github Desktop, so I'd get that installing as you read. This is an interface that lets you turn local changes
in the project into server-side changes on the repository. It is the alternative to using a kernel like Git Bash. If that's confusing, don't worry, I'll explain what that all means later.

https://desktop.github.com/

**TL;DR Install Github Desktop with the link above**

## Github & SCM
What is Github?
Github is a web-based application that will let us work on our project collaboratively (hopefully) without interfering with each-other's work. Our entire project is essentially
uploaded onto the cloud here on **github.com** as a repository, and if you ever want to work on it and make your changes you would simply *pull* from the repository, make your changes and then
*commit* it back onto Github. This will make more sense later, but for now just understand:
- There are versions of the project on the cloud (global repository)
- There is a version of the project on your device (local repository)
  
Have a gander at **The General Workflow** for more info.

Source Control Management (SCM (you may have also heard of the term Version Control which is the same thing) is what Github achieves - a way to manage our source. One of Github's many achievements is that it lets us track changes we've made to the project, and revert
to a previous state of the project at any time! So if you seriously mess up, we're not screwed - we can revert to a time when the project worked, and very easily. This saves us from making hundreds of
duplicate projects in case one breaks.

![image](https://github.com/datrealting/Team-Buckthorn/assets/150270914/6477b784-d932-487e-9e3d-1646ee9ec527)


**TL;DR Github is our way of sharing the project**

## Pull, Commit, Push
I brought up these terms earlier, but what do each of them actually mean?
### Pull
**'Pull'** is the action of taking the repository that is online and merging it with whatever you have on your local disk. It's the equivalent of reinstalling software on your PC, it will only pull what changes it needs, and if its not changed it won't pull.
This section is done on the **Github website**.

### Commit
**'Commit'** is the equivalent of "saving" your work, locally that is. You can make a title (which is a short summary of the changes made, written in imperative present tense (e.g. instead of "Fixed character jumping" it would be "Fix character jumping")), and a description.
This section is done on the **Github desktop app**.

### Push
**'Push'** is the equivalent of "uploading" or "saving" your work onto the cloud. Pushing will push whatever is in your local repository to the target branch. This is also known as pushing the origin. 
This section is done on the **Github desktop app**.

## Branches
The Github repository stores the many versions of the project we may have. There is one **crucial** version of the project, however, and that is stored in the **master** branch (also known as the **main**). 
Branches are Githubs way of having many different versions of the project. We can make our own branches, give them names and descriptions, and edit them without the other branches being affected. More importantly, the master branch is preserved and unchanged! For now...

Branches are generally meant to be "lightweight", and that is they are not made to have entire versions of games on them. Each branch should only be used for individual additions/fixes to the game, before being deleted/removed.

### Branch, or Fork?
You may hear the term **'fork'**. I only understand forks in principle - I have no practise with them. From my understanding, forks are very similar to branches, but each has their specific use cases.
- Branches
  - Not meant to last long, attached to a repository only temporarily to attempt a fix/add a feature.
- Forks
  - Whole new repository, which can then have its own branches on it.
  - Meant to be permanent **but** can also be merged with the main branch.
  - Adds another layer of safety to the project i.e. if you mess up very badly on this fork, you can always just fork off of the old one again.

Again, this isn't my area of expertise. Here's a diagram in place of an apology:

![image](https://github.com/datrealting/Team-Buckthorn/assets/150270914/53a9eaf3-a627-4bfa-a520-4f63df72d10d)


**TL;DR Work in branches first, then commit to the master later. For the most part, stick with branches**

## Final Changes, and Pull Requests/Merges
So you've made your changes in your branch, and you're ready to merge with the master branch. How do you do that?

**Merging** is the process of taking two builds of a game (in this case, your development branch and a test branch) and squishing them together. This is usually followed by praying it works. 

A **pull request** is basically a merge that we can all review before it goes through. To my knowledge, there is no way to merge without making a pull request first. If you're confident that the thing you're adding won't break the game, then don't bother waiting for your peers to review the pull request - just bloody merge it!

## The General Workflow
Now you know the basics, here are some scenarios to help better explain how to use Github!

### Scenario: I want to have my own version of the game!
1. Open the repository on github.com
2. Navigate to the green "<> Code" button, and hit 'Open with GitHub Desktop'. This will 'clone' the repository to your local drive - the equivalent to downloading a project from the Google Drive for example.

![image](https://github.com/datrealting/Team-Buckthorn/assets/150270914/d5c12b14-eca7-46f7-a7f5-62bf43064f1f)

3. From here, you should have a version on your computer now of the project that you can play with! This whole process at first may take a while. This is only because you are effectively installing the entire project.
Once you have the project, further pulling from the repository will be quicker as you won't need to reinstall parts of the project you already have.

### Scenario: I want to add something to the game!
1. For best practise, make a new branch in GitHub Desktop. Navigate to the top bar where it says which branch you are currently working in, click it and press 'New branch'. Give it a short, descriptive name, usually the change you intend to make.

![image](https://github.com/datrealting/Team-Buckthorn/assets/150270914/e9a72d45-1d5d-41f8-b949-9a74e85258e7)

2. Open the UE5 project from the local repository. Don't know where that is? Hit **Ctrl-Shift-F** in GitHub Desktop!
3. Make your changes/fix Alfie's bugs/add your features!
4. Save the Unreal project, then open up GitHub Desktop. You will see that all the changes you've just made should be on the left-hand side like in the picture, with a detailed breakdown (largely in gibberish as it's Unreal and not actual readable code). For example, here I simply added a cube.

![image](https://github.com/datrealting/Team-Buckthorn/assets/150270914/d53a933b-d7f6-4b25-8440-146aac17b852)

5. When ready, make a nice commit title, and a good description, and hit the big blue Commit button. Again, this saves it to your local repository, but to send it to the cloud that is when you must Push. This pushes it into whichever branch you are working on.
6. Your branch is now saved safely on the cloud. You could turn your PC off and come back to it later if you want. Alternatively, if you're ready, you can make a pull request. This must then be reviewed on the GitHub website, where it will check for any issues and incompatibilities should it be merged. If there are no issues to resolve, feel free to hit merge!
7. For organisation, be sure to delete the branch after you're done in it. All changes made to the main branch are automatically tracked and stored, so don't worry about messing up!

## Large File Storage (LFS)
This section is entirely an optional read. Don't bother if you're not interested.s

LFS is effectively a plugin in GitHub that is crucial for UE5 projects and anything sizeable. Baseline, our project is around 4GB, which is huge for a GitHub project (note: GitHub usually only deals with source code).

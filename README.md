# gitRecap
this repo is intended just to try and recap on git commands

## This file will list some util commands with it sintax for easy recap 

# What is Staging 
Staging is the area that we have between our Directory and the Repository. So we can say that staging is a temporal preparation area, where our changes can go when we execute teh 'add' command.
From here when we run the command 'commit -m ""' at this point all those changes that are in the staging, "Preparation area" are move to be tracked to the repository, is at this point where the change ID is added "commit ID"
There is also one more command that is handy for us 'checkout'; This command allow us to bring a bounch of changes or some changes into our local based on the flags we use for this command.

## Graphical view
                         [working directory]                        [Staging area]                      [Git repository]
-----------------------> [.................]                        [............]                      [..............]
cp, mv, touch, create    [.................]                        [............]                      [..............]
                         [.................] git add <file>         [............]                      [..............]
cp, mv, rm, delete       [.................] -------------------->  [............]                      [..............]
                         [.................] git rm --cached <file> [............]                      [..............]
                         [.................] <--------------------  [............]                      [..............] 
                         [.................]  git rm --force        [............]                      [..............]
<-----------------------------------------------------------------  [............]                      [..............]
                         [.................]                        [............] git commit           [..............]
                         [.................]                        [............]--------------------> [..............]
                         [.................]                        [............] git commit -ammend   [..............]
                         [.................]                        [............]--------------------> [..............]
                         [.................]                        [............] git reset --soft     [..............]
                         [.................]                        [............]<-------------------- [..............]
                         [.................]                        [............] git reset --mixed    [..............]
                         [.................]<---------------------------------------------------------- [..............]
                         [.................]                        [............] git reset --hard     [..............]
<------------------------------------------------------------------------------------------------------ [..............]
                         [.................]                        [............]                      [..............]

## How to See all the commits our repo has 
If we want to look out on the commits that has been done to the repo we can use the 'git log' command
probably you may be wondering why you may want to take a look on the various commits that has been executed, the reason is that we can go back in time to a sertain commit using the 'git reset [commitid]' -- soft or -- hard command.
if we use the soft all goes back to the prev state but what is in stageing remains there.
if we use the hard all goes back.
## Git log
How to use git log command 
git log shows the list of commits that has been done already 
git log --stat shows what has beenn added and or removed
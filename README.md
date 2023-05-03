# my_learnings_mac_linux_git_etc

# To install binaries of c++ files like opencv

https://rvarago.medium.com/introduction-to-cmake-for-cpp-4c464272a239#:~:text=CMake%20is%20a%20cross%2Dplatform,other%20resources%20inside%20the%20project.

Easiest way seems to be downloading an older opencv version source code like https://github.com/opencv/opencv/archive/2.4.13.6.zip and extract it to any location. In that folder perform

mkdir build

cd build

cmake ..

make

cd bin

ls

there you will find the binaries of opencv_createsamples, opencv_traincascade etc.


# My Git commands

Personal Token (PAT)----> 412cf75d0e34759fe599c8592756b414b035743b , for eg

https://git.<organization>.com/<path to repo>

https://git.<organization>.com/<path to repo>.git

git push https://<username>:<PAT>@git.<organization>.com/<path to repo>.git --all

git fetch --all

git checkout --track origin/dev

git init

git add .

git status

git branch

git commit -m 'your message'

git remote add origin 'your_url_name'
 
git push -u origin master

git branch -d localBranchName // delete branch locally

git push origin --delete remoteBranchName // delete branch remotely

git checkout -b <branch-name>
 
git checkout -b new-branch dev-branch
 
git pull <remote>
 
git reset --hard HEAD
 
git reset --hard <old_commit_id>
 
git push -f origin master
 
git stash
 
git stash list
 
git stash apply --index 1
 
git stash clear
 
git commit --amend --no-edit ( new changes wont need new commit)
 
git push -f origin testbranch
 
git branch -m renamed_branch ( rename the current branch )
 




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
 

# Add to path on mac os:
 
 Basically, what this means is that instead of running your command like this:

/path/to/program/script.sh

you can simply use the following:

script.sh

inside any directory on the file system.
 

In the process of setting up a new Mac, I installed node.js.  After the node.js installer finished, it recommended to add /usr/local/share/npm/bin to my path.  It turns out there is a very neat way to do this in OS X, the /etc/paths file!  The file contains a list (one per line) of paths that are added to the $PATH variable in the shell. Here are some quick directions to add to the path:

Open up Terminal.
 
Run the following command:

sudo nano /etc/paths

Enter your password, when prompted.
 
Go to the bottom of the file, and enter the path you wish to add.
 
Hit control-x to quit.
 
Enter “Y” to save the modified buffer.
 
That’s it!  To test it, in new terminal window, type:
 
echo $PATH

https://www.architectryan.com/2012/10/02/add-to-the-path-on-mac-os-x-mountain-lion/
 
 
#### Setting the PATH Variable Temporarily
 
Once you’ve identified the current PATH entries, you can now set the PATH for any program. If you want to use/execute a program via terminal only in your current session, you can set its path temporarily using the following command:

export PATH=$PATH:absolute/path/to/program/

For example, if you want to set PATH for Python 3.6, you’d run:

>export PATH=$PATH:/Users/shivaniagrawal/Downloads/opencv-3.4/build/bin/
 
>opencv_createsamples
 
 Usage: opencv_createsamples
 
  [-info <collection_file_name>]
 
  [-img <image_file_name>]
 
  [-vec <vec_file_name>]
 
  [-bg <background_file_name>]
 
   ....................
 
>echo $PATH 
 /opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/shivaniagrawal/Library/Python/3.8/bin/
 
 
https://techpp.com/2021/09/08/set-path-variable-in-macos-guide/
 
 

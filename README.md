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

# Got segmentation fault after creating binaries/object files/executables for opencv_createsamples

https://answers.opencv.org/question/186134/segmentation-fault-using-opencv_createsamples/

in apps/createsamples/utility.cpp commenting out this line (line 552 in opencv 3.4.4) worked for me

after commenting out that line then "make" opencv again it should scan past everything else and just make createsamples

static int icvStartSampleDistortion( const char* imgfilename, int bgcolor, int bgthreshold,
                              CvSampleDistortionData* data )
{
//    memset( data, 0, sizeof( *data ) );
Can't take credit, my son saw it right off the bat looking at the code. Best thing ever for a dad, seeing you kids becoming better than you are.

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

git clone --single-branch --branch 3.4 https://github.com/opencv/opencv.git
  
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

>Usage: opencv_createsamples
  [-info <collection_file_name>]
  [-img <image_file_name>]
  [-vec <vec_file_name>]
  [-bg <background_file_name>]
  [-num <number_of_samples = 1000>]
  [-bgcolor <background_color = 0>]
  [-inv] [-randinv] [-bgthresh <background_color_threshold = 80>]
  [-maxidev <max_intensity_deviation = 40>]
  [-maxxangle <max_x_rotation_angle = 1.100000>]
  [-maxyangle <max_y_rotation_angle = 1.100000>]
  [-maxzangle <max_z_rotation_angle = 0.500000>]
  [-show [<scale = 4.000000>]]
  [-w <sample_width = 24>]
  [-h <sample_height = 24>]
  [-maxscale <max sample scale = -1.000000>]
  [-rngseed <rng seed = 12345>]
 
   ....................
 
>echo $PATH 
 /opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/shivaniagrawal/Library/Python/3.8/bin/
 
 
https://techpp.com/2021/09/08/set-path-variable-in-macos-guide/
 
 

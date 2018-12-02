# jupyter_with_PY_R_MATLAB
I have created an envirnment for centos6.9 which contains jupyter with python, R and Matlab.

Firstly, I used the code here: http://www.edu-ing.cn/?p=1176(vagex) to get the desktop for remote vps.

Secondly, install anaconda: http://www.edu-ing.cn/?p=2671 which contains the details for config the jupyter and run it by screen.(also how to install R)


Then, it comes to matlab installing and activation
as I have the desktop for linux, so I run it by ./install the matlab zip file is download from matlab website.
we need to get the licence if use the silent install and activation
Execute the installer when you get the zip file and unzip it.
./install -inputFile ~/installer_input.txt

(To avoid problems, is better install them: apt-get install gcc build-essential openjdk-7-jdk)

Activating
./usr/local/MATLAB/R2018b/bin/activate_matlab.sh -propertiesFile ~/activate.ini 

After activating, cd matlabroot\extern\engines\python
run python setup.py install
to get matlab engine package(2018b works for python 3.6 so we need this code to install python3.6 conda install python=3.6)

For image recoverying, matlab should be reactivated by login the mathwork page and create a new computer download the "licence.lic" file.
see: http://installfights.blogspot.com/2016/11/how-to-install-matlab-without-gui.html


More details about no GUI for matlab
(To run matlab, now you need run it wihout interface:

matlab -nodesktop -nojvm -nosplash
#or matlab -nodisplay

If you want run matlab easily, you can add to your ~/.bashrc file the following lines:

alias matlab='matlab -nodisplay'
MATLAB='/usr/local/R2016a/bin'
PATH=$MATLAB:$PATH)

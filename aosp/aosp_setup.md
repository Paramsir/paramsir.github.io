### AOSP setup on ubuntu machine 

---------------------------------------------------------------------
1. Installing essential packages
---------------------------------------------------------------------
- iMX Android AOSP Required ~ 200GB hence make sure you have this much space
  in your laptop. 

$: sudo apt-get install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip gtkterm adb uuid uuid-dev zlib1g-dev liblz-dev liblzo2-2 liblzo2-dev lzop git-core curl u-boot-tools mtd-utils android-tools-fsutils openjdk-8-jdk device-tree-compiler gdisk m4 libz-dev 

# Install python mako module
sudo apt-get install python-mako

# Install OpenJDK8
-------------------
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk
sudo update-alternatives --config java   # set to correct version
sudo update-alternatives --config javac # set to correct version

# installing git and repo
--------------------------
sudo apt-get install git
sudo apt-get install repo

#configure git
---------------
git config --global user.email "user@email.com" # provide your email-id here
git config --global user.name "Test"         # Provide your username

for e.g. -
git config --global user.email "abc@gmail.com"
git config --global user.name "Testing"  


---------------------------------------------------------------------
2. To use this manifest repo, the 'repo' tool must be installed first.
---------------------------------------------------------------------
$: mkdir ~/bin
$: curl https://storage.googleapis.com/git-repo-downloads/repo  > ~/bin/repo
$: chmod a+x ~/bin/repo
$: export PATH=${PATH}:~/bin
# AOSP setup on ubuntu machine 

## AOSP recomended computer configuration

- Android AOSP is approximately 100GB code in today (2020) but after compilation and build it grows around 250GB.
1. Processor - i5 /i7 latest generation
2. Ram - 16Gb minimum (for less ram it will take lot of time to compile full OS )
2. OS - prefer Ubuntu latest version because android team itself tests on ubuntu and Mac Pc's.

- NOTE - Here onwards we have used ($:) symbol for showing ubuntu terminal. Commands starts after that sysmbol. 

## Installing essential packages
- For Ubuntu to compile it needs few packages with should be installed so just put following command in terminal and it will setup all the environment needed. 

`$: sudo apt-get install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip gtkterm adb uuid uuid-dev zlib1g-dev liblz-dev liblzo2-2 liblzo2-dev lzop git-core curl u-boot-tools mtd-utils android-tools-fsutils openjdk-8-jdk device-tree-compiler gdisk m4 libz-dev `

## Install python mako module
`$: sudo apt-get install python-mako`

## Install OpenJDK8
`$: sudo add-apt-repository ppa:openjdk-r/ppa`  <br/>
`$: sudo apt-get update ` <br/>
`$: sudo apt-get install openjdk-8-jdk`  <br/>
`$: sudo update-alternatives --config java`    <br/>
`$: sudo update-alternatives --config javac` 

## installing git and repo
`$: sudo apt-get install git`  <br/>
`$: sudo apt-get install repo`

## configure git

`$: git config --global user.email "myemail@email.com"`  <br/>
`$: git config --global user.name "username" `      

### for e.g. - <br/>
git config --global user.email "paramsir@gmail.com"  <br/>
git config --global user.name "paramsir"  

### To use this manifest repo, the 'repo' tool must be installed first.
`$: mkdir ~/bin  ` <br/>
`$: curl https://storage.googleapis.com/git-repo-downloads/repo  > ~/bin/repo `  <br/>
`$: chmod a+x ~/bin/repo`   <br/>
`$: export PATH=${PATH}:~/bin`   <br/>

### Actual downloading AOSP Code
`$: repo init -u https://android.googlesource.com/platform/manifest -b android-9.0.0_r45` <br/>
`$: repo sync`

- NOTE -Downloading will take ~6-7 Hours based on Internet Speed and compilation will take ~6-7 Hours based on coputers ram and processor speed.

### Next Reading
- Before going to compilation and building the aosp lets understand the repo commands to handle the surce code.
if you already aware of commands then direclty go for compilation and building.

1. [ AOSP important terminal commands ](aosp_imp_commands.md)
2. [ AOSP compilation and build](aosp_compile_build.md)


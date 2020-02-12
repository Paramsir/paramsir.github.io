### Compile and build AOSP code

## Compile full source code after downloading
`$: source build/envsetup.sh`<br/>
`$: lunch`<br/>
`$: make -j8` <br/>

- After preparing the compilation environment, the first step in compiling the Android source code is source build/envsetup.shthat the source command is used to run shell script commands. The function is equivalent to ".", So this command is also equivalent . build/envsetup.sh. Every time you open new terminal all above 3 commands are needed to apply.
- Lunch command is for board confuguration selection where you get a choice. 
- make will start build process from root. Here we have added **-j8** which indicates threads to be run in parallel. We can use j2, j4, j8, j12, j16... 

## Commands to compile individual module
1. **m    :**	Compile at the root of the source tree
2. **mm	  :** Compile all modules in the current path, but do not include dependencies
3. **mmm  :** Compile all modules in the specified path, but do not include dependencies
4. **mma	:** Compile all modules in the current path and include dependencies
5. **mmma :** Compile all modules in the specified path, and include dependencies
6. **make :** Without parameters, it means that the entire Android code is compiled

## Compilation instructions of some modules using make
1. **init :** make init
2. **zygot:** make app_process
3. **system_server :** make services
4. **java framework :** make framework
5. **framework resources :** make framework-res
6. **jni framework :** make libandroid_runtime
7. **binder :** make libbinder

## Compilation using mmm or other commands
1. **init :** mmm system / core / init
2. **zygot :** mmm frameworks / base / cmds / app_process
3. **system_server :** mmm frameworks / base / services
4. **java framework :** mmm frameworks / base
5. **framework resources :** mmm frameworks / base / core / res
6. **jni framework :** mmm frameworks / base / core / jni
7. **binder :** mmm frameworks / native / libs / binder

## Code Search
1. **cgrep :** Search operations on all C / C ++ files
2. **jgrep :** Perform a search operation on all Java files
3. **ggrep :** Perform a search operation on all Gradle files
4. **mangrep :** Perform a search operation on all AndroidManifest.xml files
5. **mgrep :** Perform a search operation on all Android.mk files
6. **sepgrep :** Search for all sepolicy files
7. **resgrep :** Perform search operations on all local res / *. Xml files
8. **sgrep :** Perform a search operation on all resource files

## Other commonly used commands are
1. **make clean :** perform a clean operation, equivalent to rm -rf out/
2. **make update-api :** Update the API. This instruction needs to be executed after the framework API is changed. Api is recorded in the directory frameworks/base/api.

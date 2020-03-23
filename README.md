# ArtStarOS - ASOP #

<img src="https://raw.githubusercontent.com/ArtStarOS/android_manifest/Q/ArtStarOS.jpg">

## Getting Started
To get started with the building process, you'll need to get familiar with Git and Repo.

To initialize your local repository, use a command like this:

```bash
      repo init -u git://github.com/ArtStarOS-Development/android_manifest.git -b Q-Dev
```

Then to sync up:

```bash
      repo sync -vc -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Additionally, you can define the number of parallel download repo should do:

```bash
      repo sync -vf -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## Compilation of ArtStarOS

From root directory of Project, perform following commands in terminal :

```bash
      source build/envsetup.sh
      or
      . build/envsetup.sh
```

```bash 
      export ALLOW_MISSING_DEPENDENCIES=true
```

```bash
      lunch artstar_<devicecodename>-userdebug
```

```bash
      mka bacon -j$(nproc --all)
```

## Notes
Install And Set Default Python 3.6 vs Python 3.7
```bash
      sudo apt-get install python3.6
```
```bash
      sudo apt-get install python3.7
```
```bash
      sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
      sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
```
```bash
      sudo update-alternatives --config python3
```
      

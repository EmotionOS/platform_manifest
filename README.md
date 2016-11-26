[Emotion Rom](http://emotroid.com/)
====================================

![Emotroid Team](http://i.imgur.com/4XAXvMq.png)

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    $ repo init -u https://github.com/Emotroid-Rom/platform_manifest.git -b mm

    $ git clone local_manifest into ./repo

Sync the repository:

    $ repo sync -c -f -j4 --force-sync --no-clone-bundle

***
###Set CCache

$  export USE_CCACHE=1
 
$  prebuilts/misc/linux-x86/ccache/ccache -M 100G
 

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    $ ./build-emotion.sh <device_codename>

Example for Note 4:

    $ ./build-emotion.sh trltexx

For a list of supported options, run the script on it's own:

    $ ./build-emotion.sh


Remember to `make clobber && make clean` every now and then!

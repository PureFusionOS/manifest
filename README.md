The PureNexus Project
=====================

Getting Started
---------------

To build PureNexus from source, you'll need to be familiar with
[Git and Repo](http://source.android.com/download/using-repo).


To initialize your local repository, use this command:

	repo init -u https://github.com/PureNexusProjectMod/manifest.git -b n-mr2

Then to sync up:

    repo sync -c -f -j8 --force-sync --no-clone-bundle --no-tags
    
##### Setting Up CCache
- CCache is a method of utilizing a specified storage space to speed up building. It can be referred to as the same caching your android device does to speed up application and system boot times. In this case, CCache will help build Resurrection Remix faster than standard build times (Able to cut-down 50% of time taken to build).
- To set up CCache, follow the following:


        $ echo "export USE_CCACHE=1" >> ~/.bashrc
      
        $ prebuilts/misc/linux-x86/ccache/ccache -M 50G

     -M 50G
The number before the letter G at the end specifies the amount of space CCache can use in your storage unit. As such, ensure that not too much of space is specified as this might result in unexpected errors although, the more storage you have, its recommended to have more CCache as it will increase the build times. Most efficient build systems are able to utilize CCache to about 120G or more.    
   

After syncing is done, do one of the following to build:

    bash build.sh --help

OR

    1.) . build/envsetup.sh
    2.) brunch device-user/userdebug/eng

Enjoy, Stick around for a while AOSP Building is Fun!!!

[PureNexus Community](https://plus.google.com/u/0/communities/103055954354785266764) on Google+

[PureNexusProject-Legacy](https://github.com/PureNexusProject-Legacy) Old Source and Reference code

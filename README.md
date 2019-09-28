## Getting Started ##
---------------

To get started with OMNI sources to build TWRP, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0

Then to sync up:

    repo sync

Then to build for a device with recovery partition:

     cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_<device>-eng; mka recoveryimage

Then to build for a device without recovery partition:

     cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_<device>-eng; mka bootimage

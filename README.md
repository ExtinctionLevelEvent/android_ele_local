android_ele_local
Local Manifest for Project E.L.E

Getting Started
To get started with Android, you'll need to get familiar with Git and Repo.

Make a build directory:

mkdir projectele (or whatever)
cd projectele (or the name  you chose)
To initialize your local repository using the AOSP manifest, use commands like these:

repo init -u https://android.googlesource.com/platform/manifest -b android-4.2.2_r1

curl -L -o .repo/local_manifest.xml -O -L https://raw.github.com/ExtinctionLevelEvent/android_ele_local/master/local_manifest.xml

    ( or Download: https://github.com/ExtinctionLevelEvent/android_ele_local/master/local_manifest.xml
    and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)
Then sync the source:

repo sync
Then build the source:

. build/envsetup.sh
lunch
(choose build)
make -j8 bacon

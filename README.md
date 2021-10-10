![LegionOS](https://i.imgur.com/6qCMrc2.png[/img])

---------------------------------------------------------------------------------------
 Getting Started:
 ==============

To get started with manifest/legionos, you'll need to get familiar with [Repo](https://source.android.com/source/using-repo.html) and Version Control with [Git](https://source.android.com/source/version-control.html).

To initialize your local repository, use a command like this:

```bash
repo init -u https://github.com/Project-LegionOS/manifest.git -b 12

```
You can alternatively use this command to save some space and time :

```bash
repo init --depth=1 -u https://github.com/Project-LegionOS/platform_manifest.git -b 12

```

Then to sync up:

```
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
You can just use `repo sync` or above command, but this will save you from lot of terminal spam, data and time.
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```
---------------------------------------------------------------------------------------
 Compilation of  LegionOS:
 ==================

From root directory of project, perform following commands in terminal

```bash
$ . build/envsetup.sh
$ lunch legion_<device_codename>-buildtype
$ make legion
```

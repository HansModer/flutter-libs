# flutter-libs

This repo is just for some testers. It is written in as easy language as possible so anyone can understand and work with this. 

# How to use this repo?
## 1. Adding Secret Token
1. Fork it.
2. Generate your **Github Token (Classic)** with required permissions and expiration time as needed.
3. Copy and save it in safe place.
4. Open the forked repo, goto **Settings**.
5. Then head to **Secret and variables** on left side pane.
6. Then select **Actions** option.
7. Under **Repository secrets**, there is a button **New repository secret**.
8. Click on it, enter *Secret name* as *MY_TOKEN* and your github token starting from ghxxxxxxxxxxxxxxxxxxx in *Secret* section.
9. Press **Add Secret**.

## 2. Enabling workflows if disabled
1. Open the forked repo, goto **Settings**.
2. Then head to **Actions** on left side pane.
3. Then select **General** option.
4. Click on first radio button and press *Save* button.

## 3. Generating Flutter libs
1. Open your forked repo, goto .github/workflows/*flutter-build.yml*.
2. Edit it and speicfy the **Flutter version in line 20**.
3. Commit the change.
4. Goto **Actions** Tab, select **Flutter Build** workflow and Run it.
5. It will run for some minutes and you will get the libs in Releases section of your repo.

# Finding the correct flutter version from dart version
1. To find the correct version needed for our build we can head the [Flutter Release Archive](https://docs.flutter.dev/release/archive). 
2. Find the **Dart version** for which you are desiring to build flutter libs.
3. Once you find it, see the **Flutter version** in the same row.
4. Rest you know.

**Notes**: 
1. There are 2 workflows present in this repo. One creates flutter libs and the other workflow clears the actions and releases section after every 6 hours.
2. This doesn't clutter the repo.

The initial workflow file was given by *Rajesh khurana*. It was pushing the builds to artifacts. The workflow here is the upgraded version, needs 1 env but it pushes the libs along with flutter version to the **Releases section** of repo making it easier to locate and download files.

# How to install VS Code in an Android Phone? | CodeWithHarry
In this post, we will see how you can install VS Code on an Android device. We will use one of the most popular Android terminal applications called Termux.

**Updated August 2023:** _There have been some changes with Termux due to which the official play store app of Termux doesn't work but don't worry I will guide you on using VS Code on your Phone._

If you are a student who wants to code on your Android device using VS Code, this might be the best setup for you.

Follow the steps below:

Step 1 - Install termux
-----------------------

In order to install VS code, you will have to install the Termux app by scrolling down and downloading apk using [this link from f-droid](https://f-droid.org/en/packages/com.termux/).

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/1.jpg)

The official release available on the play store doesn't seem to get the packages updated for some reason. 

Termux from Play Store won't work. This is what the [official Termux Github repository](https://github.com/termux/termux-app#google-play-store-deprecated) has to say:

_"Termux and its plugins are no longer updated on [Google Play Store](https://play.google.com/store/apps/details?id=com.termux) due to [Android 10 issues](https://github.com/termux/termux-packages/wiki/Termux-and-Android-10) and have been deprecated. The last version released for Android >= 7 was v0.101. It is highly recommended to not install Termux apps from Play Store anymore."_

Open the downloaded apk by clicking "Open"

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/2.jpg)

Now Install the apk file. If you are prompted to go to settings and enable installation of Apps from unknown sources, do that!

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/3.jpg)

Open the Termux app and you will see a screen like this:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/4.jpg)

Step 2 - Install Ubuntu using Termux
------------------------------------

Enter the following command on Termux to update the package repository

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/5.jpg)

When prompted, press 'y' and then press enter. You will have to press y followed by enter every time you are prompted for it.

Now let's upgrade the packages using the below command in Termux

Now let's install proot-distro using the following command:

Now let's list all the distros we can install using proot using the following command (This command is optional)

You will see a screen like this: 

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/6.jpg)

Now fire this command and Ubuntu will start to install on your Android phone

Ubuntu will start installing and you will see a screen like this:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/7.jpg)

Now, start Ubuntu by firing the following command:

You will now see a `root@ubuntu` prompt in the terminal like this:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/8.jpg)

Step 3 - Downloading code server
--------------------------------

While on Ubuntu run the following command:

and following command to upgrade the package repository:

Press 'y' and enter whenever prompted.

Now install wget using the following command:

Again press 'y' and enter whenever prompted to confirm the installation. You now have wget installed!

We will now download the latest release of the code server from Github using the following command:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/9.jpg)

Extract the tarball using the following command:

The tarball will start extracting. Wait for the tarball extraction to finish

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/10.jpg)

Enter the /bin folder of your code-server installation on Ubuntu (running on your phone)

Step 4 - Set up a password and start using VS Code
--------------------------------------------------

Setup a password for your VS Code instance using the following command:

**Note:** I am using a very weak password for demonstration purposes as I will use this code-server locally on my phone. Consider using strong passwords for your serious projects

Launch the code server using the following command:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/11.jpg)

Now go to your browser. I am using Google Chrome for Android and go to localhost:8080

You will finally see a screen like this:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/12.jpg)

After entering the password you will see a welcome screen like this:

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/13.jpg)

You can now start coding in VS Code on your Android Devices

![](https://cwh-full-next-space.fra1.cdn.digitaloceanspaces.com/blogpost/install-vs-code-in-android/14.jpg)

Hope that worked for your phone. Please share your experiences, ask questions, or suggest improvements in the comments section. Happy Hacking!

### Caveats:

1\. If the update command doesn't work on your Termux or you get some other network errors, try to change the default repo by using the command below:

Change the repository to Mirror by Grimle and try the `pkg update` command again. It should work!

2\. Whenever prompted, press 'y' and then press enter. You will have to press y followed by enter every time you are prompted for it.
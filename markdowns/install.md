# Installation 

There are two ways to install Road Runner 1.0.

## Method 1: Downloading the Quickstart (highly recommended)

Download the Quickstart repo from [GitHub](https://github.com/acmerobotics/road-runner-quickstart).
This is a modification of the base FIRST SDK with the Road Runner dependencies and tuning files included.
If you don't use Git, you can download it as a zip file,
extract it to somewhere on your system, and open it in Android Studio.

You can also follow the [Cookbook guide](https://cookbook.dairy.foundation/intro_to_programming/intro_to_git.html)
for using Git to download a project.
Use this repository link in place of the FIRST SDK:
https://github.com/acmerobotics/road-runner-quickstart


## Method 2: Installing Road Runner onto an existing FTC project

You can use this to add Road Runner to your own pre-existing project.

Note: it is typically much easier to first download the Quickstart and then copy your existing TeamCode files into it.

This method should only be used in exceptional circumstances,
such as if you have a complex setup with many external libraries or 
if FIRST releases a new SDK version and the Road Runner Quickstart has not yet been updated.

> [!WARNING]  
> Please ensure you have removed all references to prior versions of Road Runner and FTC Dashboard from your  
> Gradle files, as well as any previous Road Runner utilities from your TeamCode folder.

First, open the `build.gradle` file inside your TeamCode module and add the following to the `repositories` section:

```groovy
maven {
     url = 'https://maven.brott.dev/'
}
```


Next, add this snippet to the end of the `dependencies` section:

```groovy
implementation "com.acmerobotics.roadrunner:ftc:0.1.13"
implementation "com.acmerobotics.roadrunner:core:1.0.0"
implementation "com.acmerobotics.roadrunner:actions:1.0.0"
implementation "com.acmerobotics.dashboard:dashboard:0.4.16"
```

Now, perform a Gradle Sync.

Next, download a copy of [the Quickstart](https://github.com/acmerobotics/road-runner-quickstart/)
and copy all the files and folders from the TeamCode folder of the Quickstart into your own project.
Place them in the same spot within your TeamCode folder.
After that, you are ready to begin tuning.

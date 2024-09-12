# Installation 

There are two ways to install Road Runner 1.0.

[Method \#1: (highly recommended)](link to Method 1) Download the Quickstart repo from [GitHub](https://github.com/acmerobotics/road-runner-quickstart).
This is a modification of the base FIRST SDK with the Roadrunner dependencies and tuning files included.
If you don't use Git you can download it as a zip file,
extract it to somewhere on your system, and open it in Android Studio.
You can also follow the [Cookbook guide](https://cookbook.dairy.foundation/intro_to_programming/intro_to_git.html)
for using Git to download a project by using this repository link in place of the FIRST SDK:
https://github.com/acmerobotics/road-runner-quickstart

[Method \#2:](link to Method 2) Manual installation.
You can use this to add Roadrunner to your own pre-existing project.
In many cases, merging your teamcode with the quickstart is easier,
however if you have a complex setup with many external libraries,
this may be easier than adding your code to the quickstart.
Also, in the case FIRST releases a new SDK version and the Quickstart has not been updated,
you can install Roadrunner this way.

## Method 1: Downloading the Quickstart

Download the quickstart guide from [the roadrunner quickstart GitHub repository](https://github.com/acmerobotics/road-runner-quickstart).
Then, open it in and do a Gradle Sync.

If you know how to use git, you can run `git clone https://github.com/acmerobotics/road-runner-quickstart.git`,
then open it with Android Studio.

## Method 2: Installing Roadrunner onto an existing FTC project

> [!TIP]  
> Consider using the Quickstart and copying your code to it.

> [!WARNING]  
> Please remove all references to prior versions of Roadrunner and FTC Dashboard from your  
> Gradle files, as well as any previous Roadrunner utilities from your TeamCode folder.

Open the `build.gradle` file from your TeamCode module. Add the following to your `Repositories` section.

```groovy
maven {
     url = 'https://maven.brott.dev/'
}
```

If `Repositories` does not exist, instead add this snippet between the `android` and `dependencies` sections:

```groovy
repositories {
  maven {
      url = 'https://maven.brott.dev/'
  }
}
```

Also, at the end of the `dependencies` section add this snippet:

```groovy
implementation "com.acmerobotics.roadrunner:ftc:0.1.13"
implementation "com.acmerobotics.roadrunner:core:1.0.0"
implementation "com.acmerobotics.roadrunner:actions:1.0.0"
implementation "com.acmerobotics.dashboard:dashboard:0.4.16"
```

Now, do a Gradle Sync.

Download all the files from [the Quickstart’s teamcode folder](https://github.com/acmerobotics/road-runner-quickstart/tree/master/TeamCode/src/main/java/org/firstinspires/ftc/teamcode) (located at `TeamCode/src/main/java/org/firstinspires/ftc/teamcode` within the quickstart) as well as the `tuning` and `messages` folders. Place them in the same spot within your teamcode folder.	

You're done!

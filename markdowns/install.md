# Installation 

Roadrunner 1.0 has two main ways that you can install it, depending on if you have an existing project or not.

[Method \#1:](link to Method 1) Simply download the Quickstart repo from [it's github repo](https://github.com/acmerobotics/road-runner-quickstart). This is an empty project (almost like you just downloaded the SDK from first), but with the Roadrunner dependencies and tuning files included. All you need to do is open it in Android Studio.

[Method \#2:](link to Method 2) Manual installation. You can use this to add Roadrunner to your own pre-existing project. In many cases, merging your teamcode with the quickstart is easier, however if you have a complex setup with many external libraries, this may be easier than adding your code to the quickstart. Also, in the case FIRST releases a new SDK version and the Quickstart has not been updated, you can install Roadrunner this way.

## Method 1: Downloading the Quickstart

Download the quickstart guide from [the roadrunner quickstart GitHub repository](https://github.com/acmerobotics/road-runner-quickstart).  Then, open it in and do a Gradle Sync.

If you know how to use git, you can run `git clone https://github.com/acmerobotics/road-runner-quickstart.git`, then open it with Android Studio.

## Method 2: Installing Roadrunner onto an existing FTC project

> [!TIP]  
> Consider using the Quickstart and copying your code to it.

> [!WARNING]    
> Please remove all references to prior versions of Roadrunner and FTC Dashboard from your    
> Gradle files, as well as any previous Roadrunner utilities from your TeamCode folder.

Open the `build.gradle` file from your TeamCode module. Add the following to your `Repositories` section.

```java
maven {
     url = 'https://maven.brott.dev/'
}
```

If `Repositories` does not exist, instead add:

```java
repositories {
  maven {
     url = 'https://maven.brott.dev/'
  ]
}
```

between the `android` and `dependencies` sections

Also, at the end of the `dependencies` section add:

```java
implementation "com.acmerobotics.roadrunner:ftc:0.1.13"
implementation "com.acmerobotics.roadrunner:core:1.0.0"
implementation "com.acmerobotics.roadrunner:actions:1.0.0"
implementation "com.acmerobotics.dashboard:dashboard:0.4.16"
```

Now, do a Gradle Sync.

Download all the files from [the Quickstart’s teamcode folder](https://github.com/acmerobotics/road-runner-quickstart/tree/master/TeamCode/src/main/java/org/firstinspires/ftc/teamcode) (located at `TeamCode/src/main/java/org/firstinspires/ftc/teamcode` within the quickstart) as well as the `tuning` and `messages` folders. Place them in the same spot within your teamcode folder.	

You're done!
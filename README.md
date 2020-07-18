Tuinity ![Java CI](https://github.com/Spottedleaf/Tuinity/workflows/Java%20CI/badge.svg)
[![Discord](https://img.shields.io/discord/186794372468178944.svg?color=blue&label=Discord&logo=discord)](https://discord.gg/CgDPu27)
[![IRC](https://img.shields.io/discord/186794372468178944.svg?color=yellow&label=IRC&logo=mlg)](http://irc.spi.gt/iris/?channels=tuinity)
[![Contributors](https://img.shields.io/github/contributors/SpottedLeaf/Tuinity.svg)](https://github.com/SpottedLeaf/Tuinity/graphs/Contributors)
==

Fork of [Paper](https://github.com/PaperMC/Paper) aimed at improving server performance at high playercounts.

## Downloads
[DOWNLOAD LATEST JENKINS BUILD](https://ci.codemc.io/job/Spottedleaf/job/Tuinity/lastSuccessfulBuild/artifact/tuinity-paperclip.jar)

### Note: You need to be signed in to a github account to download these builds below

[DOWNLOAD LATEST 1.16 BRANCH BUILD](https://github.com/Spottedleaf/Tuinity/actions?query=branch%3Aver%2F1.16++)

[DOWNLOAD LATEST DEV-BUILD](https://github.com/Spottedleaf/Tuinity/actions?query=branch%3Adev)

## Contact
[IRC](http://irc.spi.gt/iris/?channels=tuinity) | [Discord](https://discord.gg/CgDPu27)

## How to (Server Admins)
Tuinity uses the same paperclip jar system that Paper uses.

You can download the latest build of Tuinity in [Downloads](#downloads) section above

You can also [build it yourself](#building)

## How to (Plugin developers)
In order to use Tuinity as a dependency you must [build it yourself](#building).
Each time you want to update your dependency you must re-build tuinity.

<details><summary>Gradle</summary>
<p>
 
 * Artifact Information - Tuinity-API

```groovy
dependencies {
    compileOnly "com.tuinity:tuinity-api:1.16.1-R0.1-SNAPSHOT"
}
 ```
* Artifact Information - Tuinity-Server
```groovy
dependencies {
    compileOnly "com.tuinity:tuinity:1.16.1-R0.1-SNAPSHOT" 
}
```

</p>
</details>

<details><summary>Maven</summary>
<p>
    
* Artifact Information - Tuinity-API

```xml
<dependency>
    <groupId>com.tuinity</groupId>
    <artifactId>tuinity-api</artifactId>
    <version>1.16.1-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

* Artifact Information - Tuinity-Server

```xml
<dependency>
    <groupId>com.tuinity</groupId>
    <artifactId>tuinity</artifactId>
    <version>1.16.1-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

</p>
</details>

**There is no repository required since the artifacts should be locally installed
via building tuinity.**

## Building

<details><summary>Requirements</summary>
<p>

- You need **GIT** installed, with a configured user name and email. On windows you need to run from git bash.

- You need **MAVEN** installed

- You need **JDK 8+** installed to compile (and **JRE 8+** to run)

- Anything else that **[Paper](https://github.com/PaperMC/Paper)** requires to build
 
</p>
</details>



 #### If all you want is a paperclip server jar, just run -   ***./tuinity jar***



*Otherwise, to setup the **Tuinity-API** and **Tuinity-Server** repo, just run the following command
in your project root **./tuinity patch** additionally, after you run **./tuinity patch** you can run **./tuinity build** to build the 
respective api and server jars.*


**./tuinity patch** *should initialize the repo such that you can now start modifying and creating
 patches. The folder **Tuinity-API** is the api repo and the **Tuinity-Server** folder
 is the server repo and will contain the source files you will modify.*


## Creating a patch

Patches are effectively just commits in either **Tuinity-API** or **Tuinity-Server**.
To create one, just add a commit to either repo and run **./tuinity rb**, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.

## License

The PATCHES-LICENSE file describes the license for api & server patches,
found in **./patches** and its subdirectories except when noted otherwise.

Everything else is licensed under the MIT license, except when note otherwise.
See https://github.com/starlis/empirecraft and https://github.com/electronicboy/byof
for the license of material used/modified by this project.

### Note


**The fork is based off of aikar's EMC framework found [here](https://github.com/starlis/empirecraft)**

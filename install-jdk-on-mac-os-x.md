# Install JDK on Mac OS X {#jdk-installation}

The purpose of this section is to guide you to install Java in your development environment. JDK is a shortcut for Java™ Platform, Standard Edition Development Kit

The JDK is a development environment for building applications, applets, and components using the Java programming language.

Latest version of JDK is JDK 8.

JDK 8 installation is mandatory if you want to target Android devices.

Navigate to the following URL :[http://www.oracle.com/technetwork/java/javase/downloads/](http://www.oracle.com/technetwork/java/javase/downloads)

Locate the button Java SE Downloads:

![](/assets/Screen Shot 2016-12-27 at 11.49.09.png)

Click on this button.

On the next page select the latest release for the Mac OS X platform: jdk-8u112-macosx-x64.dmg.

Install the package.

## Setup the JAVA\_HOME system variable

Open the Terminal app and type the following command:

```
export JAVA_HOME=$(/usr/libexec/java_home)
```

To check the JAVA\_HOME is correctly setup type the following commands:

```
cd $JAVA_HOME
pwd
ls
```

You should see the following result:

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_112.jdk/Contents/Home
COPYRIGHT                include
LICENSE                    javafx-src.zip
README.html                jre
THIRDPARTYLICENSEREADME-JAVAFX.txt    lib
THIRDPARTYLICENSEREADME.txt        man
bin                    release
db                    src.zip
```

## Persist the JAVA\_HOME system variable for the current user

The JAVA\_HOME system variable must be persisted when you leave and resstart a new Terminal  Window.

One way to do this is to create a .profile file in the users home directory. This file should contain all the commands that should be persisted.

Open the Terminal app and type the following commands:

```
cd $HOME
nano .profile
```

In the Text Editor, type the following line

`export JAVA_HOME=$(/usr/libexec/java_home)`

You should have a screen similar to the following screenshot:

![](/assets/Screen Shot 2016-12-27 at 15.26.59.png)

To save the .profile file, type `CTRL + X`, then type `Y` followed by the `ENTER` key.

Once done, quit the Terminal window, reopen a new one and type the following command to check if the system variable has been persisted:

```
echo $JAVA_HOME
```

You should have a non empty response.




# Perfect - The NTP Utility

![Easy Button](http://i.imgur.com/1JqfhPh.jpg)

Perfect is the **EASIEST** way to install NTP

## Prerequisites

Perfect requires Java 1.6, and access to Github and Artifactory and has been developed and tested for Mac but may work on other Nixes.

You can check your Java version with `java -version`.

[More information about Github ssh keys](https://help.github.com/articles/generating-an-ssh-key/)

[More information about setting up Maven and Artifactory](docs/Artifactory Setup.md)

## Installation

```
  # First install perfect

  curl -s https://raw.githubusercontent.com/octanner/perfect/master/bin/perfect-self | bash

  # Then install ntp

  perfect install

```

## About

Once you have Perfect installed you can use it to install NTP. Currently it is able to build perf-common, perf-ext, and perfork.

The perfect-self install script installs perfect to ~/.perfect. If you want to hack on perfect you can clone it from github and add it to your bashrc manually. See [perfect-self](bin/perfect-self) for more information on perfect installs itself.

By default Perfect installs NTP and it dependencies into ~/ntp. You can change this by passing an argument to perfect install like this `perfect install /some/dir/ntp`. Perfect stores the location of NTP and it's dependencies in ~/.ntp_install_dir. If you ever need to change the location of NTP on your file system you must also update this file.

Perfect is really just a set of Bash scripts. You can learn more about how Perfect works, and how NTP is installed by reading each of the scripts in the [bin directory](bin/). 

Each script cooresponds to a perfect command or a utility. 

1. [perfect](bin/perfect) is a wrapper that creates a pretty interface to the other scripts.
2. [perfect-build](bin/perfect-build) contains the commands that build NTP and it's dependencies.
3. [perfect-env](bin/perfect-env) is a utility script Perfect uses to configure it's envrionment.
4. [perfect-install](bin/perfect-install) contains the commands that download NTP sources and dependencies.
5. [perfect-run](bin/perfect-run) contains the commands that run built NTP artifacts.
6. [perfect-select](bin/perfect-select) contains short cut commands for getting around NTP source directories quickly.
7. [perfect-self](bin/perfect-self) is the Perfect self installation script.
8. [perfect-tidy](bin/perfect-tidy) contains commands for cleaning up NTP source directories.
9. [perfect-update](bin/perfect-update) contains commands for updating NTP source directories.
10. [perfect-usage](bin/perfect-usage) is a utility script Perfect uses to print it's documentation.

### Environment Variables

Perfect installs it's own version of Ant and Maven and sets up it's own environment to ensure everything works as it expects. Perfect doens't hange any of the envrionment variables you have configured in your bashrc or other shell scripts but it may remove or overwrite them in it's own environment.


## Commands

### Install to a specific directory

```
perfect install some/dir/ntp
```

### Update Sources (perfcommon and perfext)

```
perfect update
```

### Build the App

#### Build a given environment

```
perfect build prod|qa|dev
```

#### Build a little faster with Maven -U and skip tests

```
perfect build qa true true
```

### Run the app

```
perfect run
```

### Changing Directories

#### Use perfect to quickly change to a project directory

```
perfect ext # changes dirs to your perfext directory
```

```
perfect common # changes dirs to your perfcommon directory
```

```
perfect jboss # changes dirs to your jboss directory
```

### Changing Branches

#### Use perfect to change all sources to the given branch

```
perfect select R_14_02_1 # switches perfcommon and perfext to branch R_14_02_1
```

#### Quickly switch back to master by passing no arg

```
perfect select
```


#For more information on NTP, please see [here](https://confluence.octanner.com/pages/viewpage.action?pageId=6465994)

# Contribute

Log bugs using github issues or fix them your self and submit a pull request.

## TODO
If a download fails or gets an error eg 404 perfect should notify the user
It would be nice if we always installed the lastest Ant and Maven
It would be nice if there were commands to update Ant and Maven to the latest
Commands should be added to perfect to update and rebuild perfext and perfcommon.
It might also need an option to configure perfcommon to play nice with VirtualBox.

```
        ,--.--._
 ------" _, \___)     N
         / _/____)    T
         \//(____)    P
 ------\     (__)
        `-----"
 _______  _______  _     _
|       ||       || | _ | |
|    _  ||   _   || || || |
|   |_| ||  | |  ||       |
|    ___||  |_|  ||       |
|   |    |       ||   _   |
|___|    |_______||__| |__|
```


## License

[MIT](http://opensource.org/licenses/MIT)


# Perfect - The NTP Utility

![Easy Button](http://i.imgur.com/1JqfhPh.jpg)

Perfect is the **EASIEST** way to install NTP

```
  # First install perfect

  curl -s https://raw.github.com/octanner/perfect/master/bin/perfect-self | bash

  # Then install ntp

  perfect install

```

The only requirement for perfet is Java 1.6. It will install Jboss, Ant, and Maven for you, and build ntp.

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

#### Build prod

```
perfect build prod
```

#### Build QA

```
perfect build prod
```

#### Build Qa, with Maven -U and skip tests

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
MIT



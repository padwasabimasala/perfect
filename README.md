# Perfect - The NTP Utility

![Easy Button](http://i.imgur.com/1JqfhPh.jpg)

#For more information on NTP, please see [here](https://confluence.octanner.com/pages/viewpage.action?pageId=6465994)

Perfect is the **EASIEST** way to install NTP

### Current Method

1. Clone the perfect repo
2. Add an alias for perfect to your .bash_profile `alias perfect='<path>/perfect/bin/perfect'`
3. Add `<path>/perfect/bin` to PATH in .bash_profile
4. Restart your terminal
5. Create a root directory named "ntp" anywhere you prefer. Example: `mkdir ~/ntp`
6. `cd ~/ntp`
7. `perfect install`

### Old Method (Needs to be updated now that the perfect repo is private. Curl command requires an oAuth token.)

```
  # First install perfect

  curl -s https://raw.githubusercontent.com/octanner/perfect/master/bin/perfect-self | bash

  # Then install ntp

  perfect install

```

The only requirement for perfect is Java 1.6, and having set up your ssh keys for github. It will install Jboss, Ant, and Maven for you, and build ntp.

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


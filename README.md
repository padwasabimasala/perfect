# Perfect - The NTP Utility

![Easy Button](http://i.imgur.com/1JqfhPh.jpg)

## About

Perfect is a small bash utility for working with NTP. Install perfect, and then use it to install, and move around in NTP.

If you don't work at Octanner on NTP it probably isn't going to be useful to you.

## Easy Install

```
  curl -s https://raw.github.com/octanner/perfect/master/bin/perfect-self | bash
```

# Examples

## Use perfect to install ntp

Perfect only assumes you have Java 1.6. It will install Jboss, Ant, and Maven for you, and build ntp.

```
perfect install # Installs perfcommon and perfext to $HOME/ntp
```

```
perfect install projects/ntp # Installs perfcommon and perfext to projects/ntp
```

## Use perfect to quickly change to a project directory

```
perfect ext # changes dirs to your perfext directory
```

```
perfect common # changes dirs to your perfcommon directory
```

# Contribute

Log bugs using github issues or fix them your self and submit a pull request.

## TODO
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



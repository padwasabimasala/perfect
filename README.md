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

# Examples

## Use perfect to install ntp to a specific directory

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



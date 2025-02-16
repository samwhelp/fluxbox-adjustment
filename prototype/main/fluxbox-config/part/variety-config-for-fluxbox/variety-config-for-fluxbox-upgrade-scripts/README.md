

# Fluxbox / variety-config-for-fluxbox-upgrade-scripts




## Config File Path

| Config File Path |
| --- |
| [~/.config/variety/scripts/set_wallpaper](./asset/overlay/etc/skel/~/.config/variety/scripts/set_wallpaper) |
| [~/.config/variety/scripts/get_wallpaper](./asset/overlay/etc/skel/~/.config/variety/scripts/get_wallpaper) |


> [~/.config/variety/scripts/set_wallpaper](./asset/overlay/etc/skel/~/.config/variety/scripts/set_wallpaper)

``` sh

# Fluxbox
if [[ "fluxbox" == "$XDG_CURRENT_DESKTOP" || "fluxbox" == "$DESKTOP_SESSION" ]]; then
    fbsetbg "$WP" 2> /dev/null
    ## fix ~/.fluxbox/lastwallpaper to using latest wallpaper when relogin fluxbox
    mkdir -p ~/.fluxbox
    echo '$''full ''$'"full|$WP||:0.0" > ~/.fluxbox/lastwallpaper
fi
```



## Debian Package

| Debian Package |
| --- |
| [fluxbox](https://packages.debian.org/stable/fluxbox) |
| [variety](https://packages.debian.org/stable/variety) |




## Usage


### install

run

``` sh
./install.sh
```

or run

``` sh
make install
```


### package-install

run

``` sh
./package-install.sh
```

or run

``` sh
make package-install
```


### asset-install

run

``` sh
./asset-install.sh
```

or run

``` sh
make asset-install
```


### prototype-install

run

``` sh
./prototype-install.sh
```

or run

``` sh
make prototype-install
```


### config-install

run

``` sh
./config-install.sh
```

or run

``` sh
make config-install
```

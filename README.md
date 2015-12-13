# [AUR] gogs-openrc
Gogs init scripts for OpenRC

## Install

This package is included in the Arch User Repository. Use your preferred method of package installation:

```
yaourt gogs-openrc
```

To start Gogs on boot add the service to a run level, for example `default`:

```
sudo rc-update add gogs default
```

## System settings

Gogs uses the `gogs` user and group and installs to `/usr/share/gogs`. If you have customized your Gogs installation you should update the service too. Edit `/etc/conf.d/gogs` to set new options and see detailed descriptions. The default settings are:

```
user="gogs"
group="gogs"
basedir="/usr/share/gogs"
daemon="gogs"
daemon_opts="web"
defaultconf="${basedir}/conf/app.ini"
customconf="${basedir}/custom/conf/app.ini"
logfile="${basedir}/gogs.log"
pidfile="/run/gogs.pid"
startwait=500
timeout=1000
```

## Uninstall

Don't forget to remove the service from boot first:

```
sudo rc-update del gogs default
```

Now uninstall the package with pacman or your preferred manager:

```
pacman -R gogs-openrc
```

## Bugs / feedback

Please report bugs etc at https://github.com/nochecksum/aur-gogs-openrc/
Feel free to fork and pull request with improvements

## Maintenance

* Update sha1sums in PKGBUILD
* Build with `makepkg --source`
* Install locally with `makepkg -sri`
* Add AUR as remote, include .SRCINFO

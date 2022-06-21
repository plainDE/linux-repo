# plainDE repo storage

## pacman-based distros

To use repository add following lines to the end of your `/etc/pacman.conf`

```
[plainDE]                                                                       
SigLevel = Required                                                             
Server = https://repo.plainde.org/arch/$arch 
```

And then you need to get and trust our gpg key (`Ivan Bushchik <ivabus@ivabus.dev>`). To do this, run as root:

```sh
pacman-key --recv-keys 3E4E9C7D66E44BF7

pacman-key --lsign-key 3E4E9C7D66E44BF7
```

**Caution.** Currently plainDE can work incorrectly after updates. Reinstall plainDE completely to update it.


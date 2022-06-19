# plainDE repo storage

## ArchLinux repository

To use repository add following lines to the end of your `/etc/pacman.conf`

```
[plainDE]                                                                       
SigLevel = Required                                                             
Server = https://repo.plainde.org/arch/$arch 
```

And then you need to get and trust gpg key. To do this, run as root:

```sh
pacman-key --recv-keys 77F2CF964D0A9F5BA3DE3D313E4E9C7D66E44BF7

pacman-key --lsign-key 77F2CF964D0A9F5BA3DE3D313E4E9C7D66E44BF7
```

**Caution.** Currently plainDE can work incorrectly after updates. Reinstall plainDE completely to update it.


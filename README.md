# PKGBUILD for cubo


# Installing cubo on Arch Linux
All you need to do is download the PKGBUILD from this repository. Then run the following command:

```
makepkg -cf
```

This will create a file that ends in .pkg.tar.xz (for example, `cubo-0.2.1.r0.e0dcc39-1-x86_64.pkg.tar.xz`)

Then run:

```
sudo pacman -U *.pkg.tar.xz
```


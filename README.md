# BDlib

What's missing in SM

[https://github.com/Ganondolf/BDlib](https://github.com/Ganondolf/BDlib)

## Installation

Copy the entire content of this library in a subfolder of your local directory. Then edit your `default` file and add the following to the startup2 macro:

```
    load2 "BDlib/bdlib.sm"
    init BDlib
```

Make sure you have the load2 macro in your default file:

```
load2 1
    # load macros in local default directory
    local define macro2 :       # get user directory
    macro read "$!macro2"$1     # read macro file
```

## How to setup a local directory for SuperMongo

If you don't have a local directory, we provide here some basic instructions.
A local SM environment consists in a config file `.sm`, located in your home directory, and a local directory, containing all of your macros. The name and location of the local directory are specified in the `.sm` file in the `macro2` value:

```
macro2      /home/user/Sm/
```
For a comprehensive overview of the `.sm` file and available options, refer the sm manpage.

When SM is started, it will look for a file named `default` in the directory specified in `macro2`, load the macros it finds inside, and execute the `startup2` macro, which should be defined in your `default` file. We provide an example `default` file with this library, already set up to work with BDlib and with some additional features.

## History
BDlib is a collection of macros that were mainly developed by Giacomo Baso during his Ph.D. at the University of Padova, with contributions by the [Padova Cosmology and Structure Formation group](http://www.astro.unipd.it/cosmo/) and collaborators, including but not limited to Mario Bonamigo, Giulia Despali, Carlo Giocoli, Bepi Tormen and Ravi K. Sheth.

# Pantheon Greeter HiDPI

This is my quick and dirty solution to getting the Pantheon Greeter to look
better on my High DPI display (Dell XPS 13 2015).

What I did is checkout the latest branch of [pantheon-greeter from launchpad](https://code.launchpad.net/pantheon-greeter), and made manual tweaks to all the dimensions used in the greeter source code. Then I rebuilt the code from source and installed it over the existing pantheon-greeter

**DISCLAIMER: USE THIS AT YOUR OWN RISK**

As always with things like this use caution as I can't guarantee this won't break something.

If at any point you want to revert to the default greeter run:

```
sudo apt-get install --reinstall pantheon-greeter
```

## Instructions

- Clone this repository:

```
git clone https://github.com/sankethkatta/pantheon-greeter-hidpi.git
```

- You'll need some packages to be able to build:

```
sudo apt-get install cmake valac build-essential libgranite-dev libindicator3-dev libclutter-gtk-1.0-dev liblightdm-gobject-1-dev
```

- Build the package and install:

```
cd pantheon-greeter-hidpi
mkdir build
cd build
cmake ..
make
sudo make install
```

Now logout and you should have a better looking greeter!

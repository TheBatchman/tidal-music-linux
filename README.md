# tidal-music-linux

This is just a simple wrapper around the Tidal web player based on Electron for **Elementary OS Loki** specific! This could however still work for Ubuntu like systems.

![Screenshot](https://raw.githubusercontent.com/Bunkerbewohner/tidal-music-linux/master/screenshot.png)

## Requirements

For music playback to work you need the [PepperFlashPlayer plugin](https://wiki.debian.org/PepperFlashPlayer).

```$ sudo apt-get install pepperflashplugin-nonfree```

Then set the `pepperFlashPluginPath` variable in `main.js` to:

```/usr/lib/pepperflashplugin-nonfree/libpepflashplayer.so```

Elementary needs NodeJS to run this. The version you would need was found on [this](https://stackoverflow.com/questions/21168141/cannot-install-packages-using-node-package-manager-in-ubuntu) page. The one that comes with npm did not work for me.

```sudo apt-get install nodejs-legacy```

## To Use

To clone and run this repository you'll need [Git](https://git-scm.com). From your command line:

```bash
# Clone this repository
$ git clone https://github.com/TheBatchman/tidal-music-linux.git

# Go into the repository
$ cd tidal-music-linux

# Check prefix (https://stackoverflow.com/questions/23090835/npm-install-not-installing-things-at-usr-bin)
$ npm get prefix

# Set prefix correctly for elementary (Ubuntu; CLI symlinks are placed in /usr/bin)
$ npm set prefix /usr

# Install dependencies
$ sudo npm install -g electron

# Install this app globally so you can run "tidal" from the terminal
$ npm install -g

# Move tidal.desktop to /usr/share/applications/tidal.desktop for menu entry
sudo cp ./tidal.desktop /usr/share/applications/tidal.desktop

# Should show up in your menu, if not you can still run it by typing "tidal" in the terminal
```


#### License [MIT](LICENSE)

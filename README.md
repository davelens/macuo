# What is this?
This is just a short guide on how to run Ultima Online on Mac OS 10.11+

Other versions of Mac might work just as well, but are not tested by me.  
Feel free to drop me a line if you get it to work on other versions of OS X, and I will include it into this readme.

## Installation
Run each of the following commands in the given order:

### Homebrew + Cask
```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor
brew update
brew upgrade
brew tap caskroom/cask
```

### GCC 4.8+
I only had these installed, but Mac OS X Developer Tools should work just as well.
```bash
brew tap homebrew/versions
brew install gcc48
```

### XQuartz
This will prompt you for your user password. It might take a while to install.

```bash
brew cask install xquartz
```

### Wine + winetricks
```bash
brew install wine
brew install winetricks
winetricks corefonts
winetricks vcrun6
winetricks dotnet20
winetricks fontfix
```

### Ultima Online
You need to download the installation files of your desired UO version.

For the purpose of this guide I'm downloading Mondain's Legacy in the ```~/Downloads``` dir:

```bash
cd ~/Downloads && curl -O http://largedownloads.ea.com/pub/uo/setup-1.46.0.3.exe
```

Once the download is complete, you can install UO by running:

```bash
wine ~/Downloads/setup-1.46.0.3.exe
```

Follow the instructions you get from the installation, and you should be set!

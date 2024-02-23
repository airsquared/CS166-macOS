This works on both Apple Silicon and Intel Macs.

# Installing Homebrew
If you haven't already:
1. Open Terminal
2. Paste the following and hit enter:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. Follow the prompts shown in the terminal to complete the installation including adding to path if necessary.
4. Quit Terminal and reopen it.

# Installing software
1. To install the software that's normally available in SEEDUbuntu, run the following command in terminal:
```
brew install openssl@3 john python@3.11 ghex && brew install --cask -f wireshark
```
(note: if you already have Python 3 installed, you can leave out `python@3.11`)

2. This means you don't need to install SEEDUbuntu at all, and can just run the commands directly in your Mac's terminal.

# Installing Metasploitable 2 VM
1. Install UTM with:
```
brew install utm
```
2. Open the installed UTM app from `/Applications` folder.
3. Click [this link](https://intradeus.github.io/http-protocol-redirector?r=utm://downloadVM?url=https%3A%2F%2Fgithub.com%2Fairsquared%2FCS166-macOS%2Freleases%2Fdownload%2Futm%2FMetasploitable.utm.zip) to automatically open the UTM app and start downloading the (~1GB) virtual machine.
  - If this doesn't work, download and open in UTM manually from [here](https://github.com/airsquared/CS166-macOS/releases/download/utm/Metasploitable.utm.zip).
5. Once it finishes, you can start the VM and use it as you would with VirtualBox.

# Installing an Ubuntu VM
Click the first link to automatically open the UTM app and start downloading the virtual machine, or the manual download link if the first one doesn't work. (~1.4GB)
 - On Apple Silicon Mac: [one-click install](https://intradeus.github.io/http-protocol-redirector?r=utm://downloadVM?url=https%3A%2F%2Fgithub.com%2Fairsquared%2FCS166-macOS%2Freleases%2Fdownload%2Futm%2FUbuntu.22.04.arm64.utm.zip) or [manual download](https://github.com/airsquared/CS166-macOS/releases/download/utm/Ubuntu.22.04.arm64.utm.zip)
 - On Intel Mac: [one-click install](https://intradeus.github.io/http-protocol-redirector?r=utm://downloadVM?url=https%3A%2F%2Fgithub.com%2Fairsquared%2FCS166-macOS%2Freleases%2Fdownload%2Futm%2FUbuntu.22.04.Intel.utm.zip) or [manual download](https://github.com/airsquared/CS166-macOS/releases/download/utm/Ubuntu.22.04.Intel.utm.zip)

# Uninstalling everything

UTM: (this will delete all VMs!)
```
brew rm --zap utm
```

Wireshark and the software installed earlier:
```
brew rm --zap --cask wireshark
brew rm ghex python@3.11 john openssl@3
brew autoremove
```

Uninstalling Homebrew: (follow the prompts)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"

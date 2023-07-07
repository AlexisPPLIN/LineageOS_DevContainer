# Dev Container for LineageOS build and development

When I started building my own LineageOS image.  
I found out that the build setup process is a bit complicated and made a mess in my system.  
So I built this devcontainer.

This dev container contains :
- Android platform tools (i.e `adb` and `fastboot`).
- USB debugging plug-and-play configuration (i.e. Plug your smartphone into your computer and use adb in the dev container).
- LineageOS build requirements.
- Auto creation of ccache docker volume.

> Based on LineageOS build guides : `https://wiki.lineageos.org/devices/twolip/build`

## Requirements

* Docker
* Visual Studio Code
* Dev Containers vscode extension : https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers

## How to start

1. Clone this repository.
2. Open the repository in vscode.
3. Press `F1` and type `Dev Container > Reopen in Container`.
4. Wait for docker and vscode to build and start your environnement.
5. Then, follow `Initialize the LineageOS source repository` in LineageOS build guide.
6. Enjoy !

## Known issues

If the issue you encounter is not below, please create an issue.

### `adb devices` does not show by device.

Check the following points :
- [ ] Can your USB cable can transmit data and not only power ?
- [ ] Is `USB debugging` enabled in your android dev parameters ?
- [ ] Is your device in `Data transfer` mode (check in the notification menu) ?
- [ ] If adb is already installed on your host machine :
  - Open a new terminal on your host machine and type `adb kill-server`.

After all this checks `adb devices` should at least show your device in `unauthorized` mode. 

# IPA2DEB
Convert iOS .ipa application files to the .deb file format for jailbroken devices, and add it to a Cydia repo Supports appsync and system wide apps
 
**By Alex Free, modified and improved by Ahmad Jerjawi**

IPA2DEB is a tool to convert decrypted `.ipa` files into `.deb` packages for jailbroken iOS devices. It provides a more flexible and traditional method for installing iOS applications in `.deb` format. This can be particularly useful for older devices that no longer support the App Store or when you prefer manual installations.

## Features

- Converts decrypted `.ipa` files into `.deb` packages.
- Three installation methods:
  1. **Fake Sign**: Signs the app with a fake certificate to install it for personal use. This method only works with decrypted `.ipa` files.
  2. **Appinst and Appsync**: Uses `appinst` to install the app and `appsync` for handling installation with additional support for installation and removal. This method is useful for managing app installations on jailbroken devices with enhanced control.
  3. **System-Wide Install**: Installs the app system-wide, making it available across all users like a stock iOS application. This method modifies the installation plist to ensure the app is recognized as a system app.

## Requirements

- Decrypted `.ipa` files.
- Jailbroken iOS device.
- Tools such as `dpkg`, `appinst`, `appsync`, and `ssh` to transfer files and handle the installation process. (or to put the .deb in a cydia repo easier)
## Installation

1. Transfer the decrypted `.ipa` file to your computer.
2. Run the IPA2DEB tool to convert the `.ipa` to `.deb`:
   `./ipa2deb.sh path/to/your_app.ipa`
3. Choose the installation method when prompted:
   - `1`: Fake sign and create `.deb`.
   - `2`: Use `appinst` and `appsync` to install and create `.deb`.
   - `3`: System-wide install and create `.deb`.

4. Transfer the resulting `.deb` file to your jailbroken device.
5. SSH into your device and install the `.deb` file using `dpkg`:
   `dpkg -i your_app.deb`

6. Respring your device if necessary, and your app should be installed!

## Credits

- Alex Free for the original version.
- Modified and improved by Ahmad Jerjawi with additional installation options and optimizations for system-wide installs.

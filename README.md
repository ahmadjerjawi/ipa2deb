# IPA2DEB

Convert decrypted iOS `.ipa` files to `.deb` packages for jailbroken devices and add them to Cydia repos. Supports AppSync and system-wide apps.

## Features

- Convert `.ipa` files to `.deb`.
- **Fake Sign**: For personal use with fake certificates.
- **Appinst & AppSync**: Manage installations with `appinst` and `appsync`.
- **System-Wide Install**: Makes the app available system-wide.

## Requirements

- Decrypted `.ipa` files
- Jailbroken iOS device
- Tools: `dpkg`, `appinst`, `appsync`, `ssh`
- **Optional**: Use a Cydia repo for easier installation. (Refer to your repo or a repo template on GitHub Pages for guidance.)

## Installation

1. Transfer the `.ipa` file to your computer.
2. Convert to `.deb`:
   `./ipa2deb.sh path/to/your_app.ipa`
3. Choose an installation method:
   - `1`: Fake sign and create `.deb`.
   - `2`: Use `appinst` and `appsync`.
   - `3`: System-wide install.
4. Transfer the `.deb` to your device. (By Ssh Or Adding the `.deb` to your cydia repo)
6. optional SSH into your device and install:
   `dpkg -i your_app.deb`
7. Respring if needed.

## Credits

- Ahmad Jerjawi for enhancements.
- Fake Signer by [basti564](https://github.com/basti564/fakesigner/compare/master...hykilpikonna:fakesigner-ios:master)
- [Alex Free](https://github.com/alex-free/ipa2deb/) for the original version.

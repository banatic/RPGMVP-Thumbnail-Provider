# RPGMVP Thumbnail Provider for Windows

![Image](https://github.com/user-attachments/assets/9c15cb4e-4fad-4b17-8eb6-390b1f0b63d6)

A Windows Shell Extension that adds thumbnail preview support for `.rpgmvp` `.png_` files — the encrypted PNG format used in RPG Maker MV and MZ.

View RPGMVP image thumbnails directly in Windows Explorer.

---

## Features

- Generates live thumbnail previews for `.rpgmvp` `.png_`files
- Uses standard COM thumbnail provider interface (`IThumbnailProvider`)

---

## Requirements

- Windows 10 or later (x64)
- Administrator privileges for registration
- RPGMVP files must be valid (with 16-byte PNG XOR header)

---

## Installation & Uninstallation

 Download the `RPGMVPThumbnailProvider.dll` from [Releases](https://github.com/banatic/RPGMVP-Thumbnail-Provider/releases).


Register the thumbnail provider:

```bat
regsvr32 RPGMVPThumbnailProvider.dll
```

Or unregister to uninstall:
```bat
regsvr32 /u RPGMVPThumbnailProvider.dll
```
Then delete the DLL file manually if needed.

# Limitations
Only `.rpgmvp` files following the standard encrypted PNG format are supported.

Corrupt or nonstandard RPGMVP files will not generate thumbnails.

No support for context menu preview or animated thumbnails.

## Credits

- Decryption logic inspired by [Petschko/RPG-Maker-MV-Decrypter](https://github.com/Petschko/RPG-Maker-MV-Decrypter)

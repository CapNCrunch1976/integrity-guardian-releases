# Integrity Guardian

Integrity Guardian is a Windows app for creating verified backups, recovering files, and transferring changes between PCs. This repository contains the official Windows installers and release notes.

## Download and install

1. Open **Releases** on this repository and select the latest published release.
2. Under **Assets**, download the file named `Integrity Guardian Vx.y.z Setup.exe`.
3. Run Setup to install or upgrade Integrity Guardian. The same installer selects the x64 or x86 edition for your PC.
4. Open **Integrity Guardian** from the Start menu. Choose a backup location, then add the folders you want to back up.

## What you can do

- **Backup** creates a verified copy of your selected folders, with optional password-based encryption.
- **Verify Backup** checks the integrity of an existing archive.
- **Recovery** restores an entire backup to a destination folder and replaces that folder’s contents.
- **Transfer** adds missing files and updates changed files while keeping files that exist only in the destination.
- **IG Explorer** lets you browse an archive and preview supported files before restoring them.
- **Secure Deletion** permanently deletes selected backups, files, or folders.

## Backup file types

| Extension | How to open it |
| --- | --- |
| `.igbke` | Open the encrypted archive in Integrity Guardian with its backup password. |
| `.igbk` | Open the unencrypted archive in Integrity Guardian without a password. |

Keep the password for each encrypted archive somewhere you can access during recovery.

## Help and release notes

Open **Help → View User Guide in Integrity Guardian** for setup, backup, and recovery examples. Each GitHub release lists its changes. You can also find them in the app under **Help → Change Log**.

## Publisher and legal notices

Copyright © 2026 Jeremy Mabrey. All rights reserved.

See **Help → About Integrity Guardian → Legal Notices** for copyright and third-party notices.

# Integrity Guardian

Integrity Guardian is a Windows app for verified backups, file recovery, and transferring changes between PCs. This repository contains the official installers and release notes.

## Download and install

1. Open the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest).
2. Under **Assets**, download the file named `Integrity Guardian V4.4.0 Setup.exe`.
3. Run Setup to install or upgrade Integrity Guardian. The same installer selects the x64 or x86 edition for your PC.
4. Open **Integrity Guardian** from the Start menu. Choose a backup location, then add your source folders. To organize them by project or program, create a profile on the Main Menu first.

## What you can do

- **Prepare** sets up an external drive for backups. It can use an existing volume, initialize an unpartitioned drive, or format an eligible volume as NTFS. It also supports verified overwriting of supported external HDDs and firmware block erase on eligible external NVMe drives. Availability depends on the drive, connection, and Windows support.
- **Backup Profiles** organize backups by project, program, or personal collection. Browse to the profile on your backup drive from another PC. Each PC remembers its own working folders.
- **Backup** creates a verified copy of your selected folders, with optional password-based encryption.
- **Verify** checks an existing backup or exports a SHA-256 checksum for comparing archive copies without entering the backup password.
- **Recovery** replaces a destination folder with the backup. It shows dated copies first and falls back to Latest for a source without dated copies.
- **Transfer** shows what will be replaced, added, or kept before it updates a working folder. Files found only in the destination are kept.
- **IG Explorer** lets you browse an archive and preview supported files before restoring them.
- **Secure Deletion** permanently deletes selected backups, files, or folders and protects Windows system paths.

Drive information appears beside the current backup location. It shows free space, available health information, and estimated SSD life if the drive reports wear.

## Backup file types

| Extension | How to open it |
| --- | --- |
| `.igbke` | Open the encrypted archive in Integrity Guardian with its backup password. |
| `.igbk` | Open the unencrypted archive in Integrity Guardian without a password. |

Keep the password for each encrypted archive somewhere you can access during recovery.

Integrity Guardian’s encryption design has not been independently reviewed. Use an approved, independently reviewed solution for sensitive, confidential, or regulated data.

## Help and release notes

Open **Help → View User Guide in Integrity Guardian** for setup, backup, and recovery examples. Each GitHub release lists its changes. You can also find them in the app under **Help → Change Log**.

Use **Help → Check for Updates** to find newer releases. Choose **Download Update** and run the downloaded Setup file when you are ready to upgrade. You can enable a check on startup in **File → Settings**.

## Publisher and legal notices

Copyright © 2026 Jeremy Mabrey. All rights reserved.

Integrity Guardian is available at no charge for personal and business use under the [Integrity Guardian Software License](LICENSE.txt).

See **Help → About Integrity Guardian → Legal Notices** for copyright and third-party notices.

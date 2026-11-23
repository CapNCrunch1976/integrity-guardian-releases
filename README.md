# Integrity Guardian

Integrity Guardian is a Windows app for verified backups, file recovery, and transferring changes between PCs. This repository contains the official installers and release notes.

## Download and install

1. Open the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest).
2. Under **Assets**, download the file named `Integrity Guardian V4.6.0 Setup.exe`.
3. Run Setup to install or upgrade Integrity Guardian. The same installer selects the x64 or x86 edition for your PC.
4. Open **Integrity Guardian** from the Start menu. Choose a backup location, then add your source folders. To organize them by project or program, create a profile on the Main Menu first.

## What you can do

- **Prepare** sets up an external drive for backups. It can use an existing volume, initialize an unpartitioned drive, or format an eligible volume as NTFS. It also supports verified overwriting of supported external HDDs and firmware block erase on eligible external NVMe drives. Availability depends on the drive, connection, and Windows support.
- **Backup Profiles** organize backups by project, program, or personal collection. Browse a shared list of profile names on your backup drive. Each PC remembers its own working folders.
- **Backup** saves or updates Latest and can save a dated copy at the same time. Choose **Dated Backup** to save a dated copy and leave Latest in place. Both actions verify the backup and support password-based encryption.
- **Scheduled Backups** runs unencrypted backups daily or on selected days and times while you are signed in to Windows. Choose Latest, Dated, or both. Missed runs are shown in the app and can be started with **Run Now**. Encrypted backup scheduling is in development.
- **Verify** checks an existing backup or exports a SHA-256 checksum for comparing archive copies without entering the backup password.
- **Recovery** replaces a destination folder with the backup. It prefers dated copies for each backup type. If copies for the selected source are still locked, unlock them before recovering.
- **Transfer** shows what will be replaced, added, or kept before it updates a working folder. Files found only in the destination are kept.
- **IG Explorer** lets you browse an archive and preview supported files before restoring them.
- **Secure Deletion** permanently deletes selected backups, files, or folders and protects Windows system paths.

Drive information appears beside the current backup location. It shows the drive type Windows reports, such as NVMe SSD or SATA SSD, alongside free space, available health information, and estimated SSD life when wear data is available.

Before starting a backup, **Estimated Backup Time** shows a range for each action based on the selected source folders and backup options.

## Backup file types

| Extension | How to open it |
| --- | --- |
| `.igbke` | Open the encrypted archive in Integrity Guardian with its backup password. |
| `.igbk` | Open the unencrypted archive in Integrity Guardian without a password. |

Keep the password for each encrypted archive somewhere you can access during recovery.

Each profile keeps separate Latest copies for encrypted and unencrypted backups.

Integrity Guardian’s encryption design has not been independently reviewed. Use an approved, independently reviewed solution for sensitive, confidential, or regulated data.

## Help and release notes

Open **Help → View User Guide in Integrity Guardian** for setup, backup, and recovery examples. Each GitHub release lists its changes. You can also find them in the app under **Help → Change Log**.

Enable startup update checks in **File → Settings**, or check manually from **Help → Check for Updates**. When a newer version is available, **Update Now** opens the official installer download. Run Setup to finish the update. **Skip This Update** dismisses startup reminders for that version.

## Publisher and legal notices

Copyright © 2026 Jeremy Mabrey. All rights reserved.

Integrity Guardian is available at no charge for personal and business use under the [Integrity Guardian Software License](LICENSE.txt).

See **Help → About Integrity Guardian → Legal Notices** for copyright and third-party notices.

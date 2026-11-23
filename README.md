# Integrity Guardian

Integrity Guardian is a Windows app for verified backups, file recovery, and transferring changes between PCs. This repository contains the official installers and release notes.

## Download and install

1. Open the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest).
2. Under **Assets**, download the file named `Integrity Guardian Vx.y.z Setup.exe`.
3. Run Setup to install or upgrade Integrity Guardian. The same installer selects the x64 or x86 edition for your PC.
4. Open **Integrity Guardian** from the Start menu. Choose a backup location, then add your source folders. To organize them by project or program, create a profile on the Main Menu first.

## What you can do

- **Prepare** sets up an external drive for backups. It can use an existing volume, initialize an unpartitioned drive, or format an eligible volume as NTFS. It also supports verified overwriting of supported external HDDs and firmware block erase on eligible external NVMe drives. Availability depends on the drive, connection, and Windows support.
- **Backup Profiles** organize backups by project, program, or personal collection. Browse a shared list of profile names on your backup drive. Each PC remembers its own working folders.
- **Backup** verifies each new copy before replacing Latest. Choose **Dated Backup** to save a dated copy and leave Latest in place. Both actions can create encrypted backups using either IG encryption method.
- **Scheduled Backups** runs unencrypted backups daily or on selected days and times while you are signed in to Windows. Choose Latest, Dated, or both. Missed runs are shown in the app and can be started with **Run Now**. Encrypted backup scheduling is in development.
- **Verify** checks an existing backup or exports a SHA-256 checksum for comparing archive copies without entering the backup password.
- **Recovery** replaces a destination folder with the backup. It prefers dated copies for each backup type. If copies for the selected source are still locked, unlock them before recovering.
- **Transfer** shows what will be replaced, added, or kept before it updates a working folder. Files found only in the destination are kept.
- **IG Explorer** lets you browse an archive and preview supported files before restoring them. When choosing an archive, **Date/Time** is shown first and backup files appear newest first.
- **Secure Deletion** permanently deletes selected backups, files, or folders and protects Windows system paths.

Drive information appears beside the current backup location. It shows the drive type Windows reports, such as NVMe SSD or SATA SSD, alongside free space, available health information, and estimated SSD life when wear data is available.

Before starting a backup, **Estimated Backup Time** stays visible at the bottom of the Backup side pane and shows a range for each action based on the selected source folders and backup options.

## Backup file types

| Extension | How to open it |
| --- | --- |
| `.igbke` | Open the encrypted archive in Integrity Guardian with its backup password. |
| `.igbk` | Open the unencrypted archive in Integrity Guardian without a password. |

Keep the password for each encrypted archive somewhere you can access during recovery.

Each profile keeps separate Latest copies for every source folder and backup type. Manual and scheduled backups update the matching Latest copy when that option is selected. Scheduled backups are unencrypted.

## Encrypted backup methods

| Method | When to choose it | Recovery |
| --- | --- | --- |
| **IG Password Cipher** | Default for new encrypted backups. Uses fresh hardware-generated key material and a higher password derivation cost. | Requires Integrity Guardian V4.7.0 or later. |
| **IGEH-25519-512** | Choose this when the backup needs to open on a PC running an earlier compatible version of IG. | Opens in V4.7.0 and earlier versions that support IGEH-25519-512. |

Both methods encrypt the files in an `.igbke` archive. Integrity Guardian detects the method automatically during recovery.

An IG Password Cipher backup can include an existing IGEH-25519-512 archive. The included archive keeps its original password. Backup Review flags any IG Password Cipher archive selected for inclusion in an IGEH-25519-512 backup and stops that operation.

Integrity Guardian’s encryption designs have not been independently reviewed. Use an approved, independently reviewed solution for sensitive, confidential, or regulated data.

## Help and release notes

Choose **Help → Help Document** to locate the installed User Guide PDF in File Explorer. Each GitHub release lists its changes. You can also find them in the app under **Help → Change Log**.

New settings check for updates at startup. You can change this in **File → Settings** or check manually from **Help → Check for Updates**. When a newer version is available, **Update Now** opens the official installer download. Run Setup to finish the update. **Skip This Update** dismisses startup reminders for that version.

## Publisher and legal notices

Copyright © 2026 Jeremy Mabrey. All rights reserved.

Integrity Guardian is available at no charge for personal and business use under the [Integrity Guardian Software License](LICENSE.txt).

See **Help → About Integrity Guardian → Legal Notices** for the combined PDF with copyright, third-party notices, and the Rust copyright and license inventory.

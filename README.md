# Integrity Guardian

Integrity Guardian is a Windows app for verified backups, file recovery, and transferring changes between PCs. This repository contains the official installers and release notes.

## Download and install

1. Open the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest).
2. Under **Assets**, download the file named `Integrity Guardian V4.3.0 Setup.exe`.
3. Run Setup to install or upgrade Integrity Guardian. The same installer selects the x64 or x86 edition for your PC.
4. Open **Integrity Guardian** from the Start menu. Choose a backup location, then add the folders you want to back up.

## What you can do

- **Prepare** sets up an external USB drive for backups. It can use an existing volume, initialize an unpartitioned drive, or clear a supported magnetic hard drive with read-back verification of Windows-addressable sectors. For firmware sanitization, follow the drive manufacturer's procedure from the guidance in Prepare.
- **Backup** creates a verified copy of your selected folders, with optional password-based encryption.
- **Verify** checks an existing backup or exports a SHA-256 checksum for comparing archive copies without entering the backup password.
- **Recovery** restores an entire backup to a destination folder and replaces that folder’s contents.
- **Transfer** adds missing files and updates changed files while keeping files that exist only in the destination.
- **IG Explorer** lets you browse an archive and preview supported files before restoring them.
- **Secure Deletion** permanently deletes selected backups, files, or folders.

Open **Drive Details** next to the current backup location to see free space and any drive health information Windows reports.

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

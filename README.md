# Integrity Guardian V5.0.3

*Your Data. Intact. In Your Control.*

Integrity Guardian is a Windows application for verified backups, office-to-home transfers and recovery. V5 introduced the profile redesign. One profile can define multiple folder or individual-file sources, protection options, exclusions and transfer/recovery destination folders.

## Backup, transfer and restore

- **Backup:** create a complete profile backup set and choose whether it requires a password. Save Latest, Dated, or both. Every new archive is verified.
- **Transfer:** add missing files, replace changed files according to the newer-file rule, and optionally delete destination-only files and folders.
- **Restore Entire Backup:** replace each mapped destination folder with the selected set's contents. This overwrites matching files regardless of age and removes extra destination contents. It is not Windows or whole-system recovery.
- **Review:** choose Latest to use the newest complete backup automatically or choose Dated and select its backup date and time. Inspect every source and destination before starting. Missing or replaced set members stop review. Destinations are processed in order; completed destinations remain completed if a later destination fails or cancellation occurs, and results identify them.

For new encrypted backups, use **IG Password Cipher**. Choose **IGEH-25519-512** when the backup needs to open in a compatible older version of IG.

Start with one folder. Use **+ Add Folder/File** to include additional locations. Choose **Browse Source** for the item to back up and **Browse Destination** for the folder that receives its files. You can also type a destination path for a drive or folder that is unavailable. A selected folder includes its files and subfolders, subject to exclusions. Contents go directly into the mapped destination, without an extra source-name folder. An individual-file source is represented by an archive containing that file; its mapped destination is still a folder and is the replacement boundary for Restore Entire Backup.

## Profiles and drive letters

Profile Settings has General, Folders, Backup, Schedule, Transfer and Restore sections. In Folders, select an existing mapping and use **Browse Destination** to change its destination. Select **Save profile** to apply your changes. Transfer and Recovery show the saved mappings even before the first complete profile backup. Destination paths can be entered before their folder or drive exists; execution checks availability. Each Windows installation remembers its destination overrides.

From Profile Settings, choose **Open Profile Backups** and select a backup. Enter its password if asked. IG Explorer shows its files and returns you to the same profile when you choose **Back to Profile**.

The backup-storage location is separate from the recovery destinations. A drive can appear as `D:` at the office and `E:` at home. IG can recognize a remembered backup location when its drive letter changes. Use **Change Backup Location** or **Browse Profiles** if manual selection is needed. A different drive at the old letter is not silently accepted.

On opening, IG scans attached USB storage in the background for existing stores, profiles and recognized standalone archives. Scanning leaves the backups and profiles as they are. A valid current selection is preserved. A remembered or unique profile can be reconnected; ambiguous choices are shown for selection. Use **Scan USB backups** on the Main Menu or Tools menu to rescan after connecting a drive. Startup discovery is enabled by default and can be changed in Settings. If the scan misses your location, use **Change Backup Location** to browse to it.

Keep the entire IG backup folder together when moving it to another drive so complete sets remain available. You can also open a single backup and enter its password if prompted.

## Schedules

Choose any combination of Monday through Sunday, including Monday/Wednesday/Friday, and one or more local times. A profile can schedule backups or transfers on the current PC while its Windows user is signed in. For an encrypted scheduled operation, enter the backup password for your Windows account on each PC where the schedule will run.

Existing schedules retain their unencrypted behavior until explicitly saved using the new profile settings. Scheduled Transfer uses the most recent complete Latest set and the saved destination mappings. Restore Entire Backup is an explicit manual operation.

## Interface and tools

The sidebar provides Main Menu, Backup, Recovery, Transfer, Profiles, Schedules, IG Explorer, Secure Deletion, History, Settings and About. The original shield leads the header, with the new italic tagline. Choose System, Light, Dark or Retro in **File > Settings > Appearance**. Drive preparation, independent archive verification, log export, preview, legal notices and individual-archive recovery remain available.

The Main Menu shows the selected backup drive's capacity and free space, with drive type, health and SSD life where Windows reports them.

## Installation and compatibility

Download **Integrity.Guardian.V5.0.3.Setup.exe** from the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest) and run it to install or upgrade. One installer selects x64 or x86. Open existing profiles and supported backups in V5. Use **Open individual backup** for a standalone backup. Create a profile backup in V5 to start using complete backup sets.

The main window needs a desktop work area of at least 1,024 × 768 at standard Windows scaling. This keeps the layout in view without rearranging menus or controls.

## Help

Open **Help Document** in Settings or download the V5.0.3 Help PDF with the installer.

Use **Help > Get Release Notifications** to follow new releases on GitHub. **Report a Bug** and **Suggest an Improvement** open drafts you can review and submit on GitHub.

Integrity Guardian is available at no charge for personal and business use under the [Integrity Guardian Software License](LICENSE.txt). Open **Legal Notices** from About for licensing and attribution.

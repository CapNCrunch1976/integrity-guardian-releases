# Integrity Guardian V5.4.2

*Your Data. Intact. In Your Control.*

Integrity Guardian is a Windows application for verified backups, transfers and recovery. Back up files or folders directly, or save them in a profile with the settings and destinations you use regularly.

## Backup, transfer and restore

Open **Backup** to run a backup with or without a profile. If a profile is selected, choose **Back Up Without a Profile** to save a backup directly under the current backup location. Both choices support encrypted and unencrypted backups. Use a profile to keep source and destination mappings together for repeated backups, recovery, and transfer.

- **Backup.** Save an encrypted or unencrypted copy of selected files and folders. Choose Latest, Dated, or both. Integrity Guardian verifies every new archive.
- **Transfer:** add missing files, replace changed files according to the newer-file rule, and optionally delete destination-only files and folders.
- **Restore Entire Backup:** replace each mapped destination folder with the selected set's contents. This overwrites matching files regardless of age and removes extra destination contents. It is not Windows or whole-system recovery.
- **Review:** choose Latest to use the newest complete backup automatically or choose Dated and select its backup date and time. Inspect every source and destination before starting. Missing or replaced set members stop review. Destinations are processed in order; completed destinations remain completed if a later destination fails or cancellation occurs, and results identify them.

When you save both Latest and Dated copies, Integrity Guardian computes the archive checksum while copying it. This avoids reading the original archive again. Integrity Guardian still fully verifies the original archive and reads the Dated copy back to confirm it matches.

**Estimated Backup Time** learns from up to five recent successful runs with the same sources, backup location, and options. It adjusts for the current size and item count. New selections use a general estimate until a comparable run has completed.

For new encrypted backups, use **IG Password Cipher**. Choose **IGEH-25519-512** when the backup needs to open in a compatible older version of IG.

Start with one folder using **+ Add Folder/File**. Folder sources default to **Original location**, the source path recorded in the selected backup. Choose **Choose another folder** when you need a different destination on this PC. File sources require a destination folder before recovery. Restore Entire Backup replaces the contents of each destination folder, so review the paths before confirming.

## Profiles and drive letters

In **Profiles > Manage Profile**, move backups into another profile as Dated history, move the profile and its backups to another backup location, or permanently delete the profile and its backups. The receiving profile keeps its Latest backup. Integrity Guardian verifies moved copies before removing originals.

From **Main Menu > Profile Management**, choose **Open Profiles** to create or browse for a profile. A selected profile opens on **General**, where you can choose and read about the default recovery action. In **Folders**, choose **Choose Another Folder** to set an alternate destination or **Use Original Location** to restore the default for a folder source. Existing destination mappings remain available. Select **Save profile** to apply your changes. If you leave with unsaved edits, Integrity Guardian asks whether to save, discard, or continue editing.

When you add a shared or network file or folder to a profile, choose **Backup Only** if the profile should archive it and skip it during Recovery and Transfer. This also applies to scheduled transfers. **Backup Only** is available in **Profiles > Folders** for existing sources. A backup set created with this setting retains it. Clear the setting and create a new backup to enable profile recovery for that source.

Recovery and Transfer show a warning for mapped network drives, network folder paths, and folders Windows reports as shared. Review the affected paths and ask everyone to save and close their files before continuing.

From Profile Settings, choose **Open Profile Backups** and select a backup. Enter its password if asked. IG Explorer shows its files and returns you to the same profile when you choose **Back to Profile**.

The backup-storage location is separate from the recovery destinations. A drive can appear as `D:` at the office and `E:` at home. IG can recognize a remembered backup location when its drive letter changes. Use **Change Backup Location** or **Browse Profiles** if manual selection is needed. A different drive at the old letter is not silently accepted.

On opening, IG scans attached USB storage in the background for existing stores, profiles and recognized standalone archives. Scanning leaves the backups and profiles as they are. A valid current selection is preserved. A remembered or unique profile can be reconnected; ambiguous choices are shown for selection. Use **Scan USB Backups** on the Main Menu or Tools menu to rescan after connecting a drive. Startup discovery is enabled by default and can be changed in Settings. If the scan misses your location, use **Change Backup Location** to browse to it.

Keep the entire IG backup folder together when moving it to another drive so complete sets remain available. You can also open a single backup and enter its password if prompted.

## Schedules

With **No Profile** selected, open **Schedules** and add a folder or file under **Sources**. Choose the copies, days, and times, then select **Save Schedule**. Standalone schedules create unencrypted backups and keep their own saved source selection.

Choose any combination of Monday through Sunday, including Monday/Wednesday/Friday, and one or more local times. A profile can schedule backups or transfers on the current PC while its Windows user is signed in. For an encrypted scheduled operation, enter the backup password for your Windows account on each PC where the schedule will run.

Existing schedules retain their unencrypted behavior until explicitly saved using the new profile settings. Scheduled Transfer uses the most recent complete Latest set and the saved destination mappings. Restore Entire Backup is an explicit manual operation.

## Interface and tools

The sidebar lists Main Menu, Profiles, Backup, Recovery, Transfer, Schedules, Secure Deletion and History. Open **IG Explorer** or **Verify Backup** from **Tools**. **About** is next to **Help** on the menu bar. In **History**, choose **Clear History** to clear the local operation log. Choose **Export Logs and Clear** to save a text copy first. Under **File > Settings > Appearance**, choose **Monterey Light** or **Monterey Dark** for a fixed palette with circular window controls. Choose **System** to follow Windows.

The Main Menu shows the selected backup drive's capacity and free space, along with the manufacturer, model, drive status and estimated SSD life where reported. If Windows restricts access to a drive reading, restarting in Administrator Mode may show more information. Standard Mode is suitable for everyday backups and recovery.

## Installation and compatibility

Download **Integrity.Guardian.V5.4.2.Setup.exe** from the [latest release](https://github.com/CapNCrunch1976/integrity-guardian-releases/releases/latest) and run it to install or upgrade. One installer selects x64 or x86. Open existing profiles and supported backups in V5. Use **Open individual backup** for a standalone backup. Create a profile backup in V5 to start using complete backup sets.

## Help

Open **Help > Help Document** or download the V5.4.2 Help PDF with the installer.

Use **Help > Get Release Notifications** to follow new releases on GitHub. **Report a Bug** and **Suggest an Improvement** open drafts you can review and submit on GitHub.

Integrity Guardian is available at no charge for personal and business use under the [Integrity Guardian Software License](LICENSE.txt). Open **Legal Notices** from About for licensing and attribution.

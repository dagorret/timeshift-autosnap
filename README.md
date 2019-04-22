# timeshift-autosnap
Timeshift auto-snapshot script which runs before package upgrade using Pacman hook.

# Features
*  Creates Timeshift snapshots with unique comment.
*  Deletes old snapshots which are created using this script.
*  Auto generates grub if grub-btrfs package is installed.
*  Can be manually executed by running `timeshift-autosnap` command with elevated privileges.

# /etc/timeshift-autosnap.conf options:
*  `skipAutosnap` - if set to **true** script won't be executed.
*  `deleteSnapshots` - if set to **false** old snapshots won't be deleted.
*  `maxSnapshots` - defines **maximum** number of old snapshots to keep.
*  `updateGrub` - if set to **false** grub entries won't be generated.

# Notes
*  Currently only tested in `BTRFS` mode but should work in `RSYNC` mode too since script is automating Timeshift operations.
*  This script is made in Arch and Arch based distros in mind but if there would be interest it should be easily ported to other distros.

# Contribution
*  All new ideas and contributors are welcomed!

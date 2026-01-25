# keesync

SSH-based KeePass sync written in bash. Recommended to be used with
[KeePassXC](https://keepassxc.org/) on Linux and
[KeePassDX](https://www.keepassdx.com/) on Android.

## Features

- Automatically sync changed KeePass databases to a server via SSH or rsync
- Automatically keeps backups of each revision of the database.
- Automatically suggests merge instructions when both remote and local database
  have changed for conflict resolution.
- Easily allows opening or selecting previous versions of the database.
- Easy configuration via environment variables or a config file.
- Does not depend on the implementation details of the database contents
  (simple file-based sync).

## Installation

This section is not yet complete and will contain full installation
instructions for Arch-based Linux, Debian-based Linux, and Termux Android soon.

- install the `keesync` script into a directory in your `PATH`
- configure `keesync` by setting the configuration variables in your
  environment (e.g. `.profile`) or in `~/.config/keesync/config.sh`
  - `KEESYNC_CONFIGPATH` (path to `config.sh`)
  - `KEESYNC_HOSTNAME` (local name to attribute changes to)
  - `KEESYNC_HPATH` (path from HOME to database dir on remote server)
  - `KEESYNC_LHPATH` (path from HOME to local database dir)
  - `KEESYNC_DBNAME` (name of keepass database)
  - `KEESYNC_SERVER` (remote ssh server, required)
  - (other variables defined at the top of `keesync` script)

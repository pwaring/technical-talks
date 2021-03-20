% Linux Backups
% Paul Waring
% March 20, 2021

# Introduction

 - Different backup strategies
 - Interactive - please ask questions/make comments!

# Why backup

 - User error
 - Disc failure
 - File corruption
 - Malicious actors (esp. on servers)

# Backup principles

 - Backup often (at least daily)
 - Automate backups
 - Automate reminders
 - Test restores
 - Quick/easy restore of individual files
 - Multiple sites if possible

# What to backup

 - Opinions vary
 - Minimum: Anything you can't rebuild/download
 - Local data
 - Remote data: Google Drive, emails etc.
 - Don't forget databases, saved games etc.
 - Full disk snapshots

# What not to backup

 - Huge executables (e.g. Steam library)

# DRM

 - As-is is a good starting point
 - Some DRM can be stripped (e.g. Calibre + DeDRM)

# Hardware

 - USB drives (1TB: £50, 2TB: £70, 4TB: £90)
 - Spread drives amongst manufacturers
 - Buy drives over time - less risk of a bad batch
 - USB 3.0 (both sides!) if possible
 - Seagate + Western Digital have worked for me

# Cloud

 - VPS
 - S3
 - Backblaze

# Trade-offs

 - De-duplication
 - Incremental vs full
 - Compression
 - Encryption

# Security

 - Backup software sometimes has built-in encryption
 - Encrypt the underlying block device too (e.g. LUKS)
 - Keep the keys somewhere secure - don't lose them!

# Borg

 - De-duplication and encryption
 - Supports different backend targets
 - `borg check` can be very slow - run it every X days
 - Available as a package for most distros

# restic

 - Very fast (for my workload)
 - Rapid development
 - Available as a Snap, binary, easy to build from source

# tar

 - Full backups are trivial
 - Every Linux, *BSD and macOS machine has tar
 - Range of compression options
 - Need wrapper scripts for most purposes

# rclone

 - rsync for cloud services
 - Supports Google Drive, Dropbox, lots of others
 - Can upload and download

# Automation

 - Regular backups
 - Prompt to backup (e.g. for USB drives that need to be inserted)
 - `remind` command

# My backups

 - Wrapper scripts for tar, restic, and borg
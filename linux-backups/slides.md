% Linux Backup Options
% Paul Waring
% March 20, 2021

# whoami

 - Freelance PHP developer and Linux system administrator
 - Specialise in legacy code/systems and financial services
 - I like trains, politics and technology (@pwaring)

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

# What to backup

 - Opinions vary
 - Minimum: Anything you can't rebuild/download
 - Local data
 - Remote data: Google Drive, GitHub etc.
 - Don't forget databases, saved games etc.
 - Full disk snapshots

# What not to backup

 - Huge executables (e.g. Steam library)

# DRM

 - Kindle e-books

# Hardware

 - USB drives (1TB: £50, 2TB: £70, 4TB: £90)
 - Spread drives amongst manufacturers
 - Buy drives over time - less risk of a bad batch
 - USB 3.0 (both sides!)
 - Seagate + Western Digital have worked for me

# Cloud

 - S3
 - Backblaze

# Security

 - Backup software sometimes has built-in encryption
 - Encrypt the underlying block device too (e.g. LUKS)
 - Keep the keys somewhere secure - don't lose them!

# Borg

# restic

# tar

# rclone

# Automation

 - Regular backups
 - Prompt to backup (e.g. for USB drives that need to be inserted)

# My backups
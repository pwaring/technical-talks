#include "metadata.yml"

# DNS resolver

 - Hostname to IP address (and other stuff)
 - Usually provided by ISP
 - Can also use Google, OpenDNS etc.

# Why run a local resolver?

 - Cache is closer to users
 - Bulk interception warrants
 - qname minimisation
 - DNS is public, your transactions are private

# What do you need?

 - Raspberry Pi 2 or 3
 - Raspbian (Debian Jessie)
 - Unbound

# Unbound

 - Small, fast resolver
 - Supports DNSSEC
 - Supports qname minimisation (>= 1.5.8)
 - Jessie backports

# qname minimisation

 - Default DNS mode: Send full query to every server
 - Most servers don't need this
 - Leaks some of your browsing history
 - Just send `.tld` to root, then work down
 - Downside: more queries initially
 - RFC 7816

# Extra privacy

 - ISP can still log port 53 traffic
 - SSH tunnel from RPi to cloud servers
 - DNS over TLS (RFC 7858 - stub-recursive)

# Thanks for listening

 - Slides and Ansible playbook at: talks.phpdeveloper.org.uk
 - Email: paul@xk7.net

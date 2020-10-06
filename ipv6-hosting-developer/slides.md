% IPv6: A hosting and developer perspective
% Paul Waring
% October 8, 2020

# Introduction

 - Freelance PHP developer and Linux system administrator
 - Work on the hosting and development side
 - Looking at this from the opposite side to an ISP
 - Different challenges to ISP or datacentre deployment

# Topics

 - The problem with IPv4
 - Current state of play
 - Squeezing the last drops from IPv4
 - Problems deploying IPv6
 - How do we solve this?

# The problem with IPv4

 - Not enough addresses
 - Allocation pools exhausted in many areas
 - RIPE 733: You might get a /24 if you're lucky (waiting list)
 - Every VPS, container etc. potentially needs an IP address
 - IPv6 fix: more addresses (forget everything else)

# Current state of play

 - Some hosting providers don't offer IPv6 at all
 - Very few big providers offer IPv6 with feature parity with IPv4
 - Facebook/Google: 25-30% of incoming traffic on IPv6 (with wide deployment)
 - Probably need dual-stack for now

# Squeezing the last drops from IPv4

 - Make the most of the addresses we do have
 - HTTP/1.1 - Host: header
 - Server Name Indication (broke IE/XP)
 - Private address space
 - Don't really work across servers
 - Proxy - complicates infrastructure, SPoF

# Problems deploying IPv6 (internal, fixable)

 - Services not listening on IPv6 (e.g. SSH)
 - Database schema only supports IPv4 addresses
 - Application logic assumes IPv4 (e.g. ACLs)
 - Monitor both protocols - some software defaults to IPv4
 - More things to go wrong

# Problems deploying IPv6 (external, not always fixable)

 - Third party APIs requiring IPv4 addresses (data + firewall)
 - Stricter spam detection on mail over IPv6
 - Proprietary applications
 - Hardcoded IP addresses
 - No immediate benefit for most customers
 - Lack of feature parity with IPv4 (e.g. no load balancers)

# How can we solve this?

 - Technical: Deploy, debug, fix (repeat ad infinitum)
 - Policy: Regulatory requirement to deploy IPv6
 - Market: IPv6 SEO boost, browser warnings (c.f. HTTPS)

# Takeaways

 - Deploying IPv6 at the hosting side can be a lot of work
 - You will break something
 - But you should still do it
 - Forget starting a hosting provider (for now)
 - Buy <del>land</del> IPv4, they're not making it anymore

# Thanks for listening

  - Slides (+ extra resources): phpdev.uk/talks
  - Email: paul@phpdeveloper.org.uk
  - Twitter: @pwaring
  - Questions?


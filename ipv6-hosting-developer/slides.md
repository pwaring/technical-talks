% IPv6 from a hosting and developer perspective
% Paul Waring
% October 8, 2020

# Introduction

 - Freelance PHP developer and Linux system administrator
 - Work on the hosting and development side
 - Looking at this from the opposite side to an ISP
 - Less attention - both sides must support a protocol

# Topics

 - The problem with IPv4
 - Current state of play
 - Problems deploying IPv6
 - Competition concerns

# The problem with IPv4

 - Not enough addresses
 - Allocation pools exhausted in many areas
 - IPv6 fix: more addresses (forget everything else)

# Lack of addresses "solutions"

 - Make the most of the addresses we do have
 - HTTP/1.1 - Host: header
 - Server Name Indication (broke IE/XP)
 - Don't really work across servers
 - Proxy - complicates infrastructure
 - Only long-term fix: deploy IPv6

# Problems deploying IPv6 (internal, fixable)

 - Services not listening on IPv6 (e.g. SSH stopped working)
 - Databases only supported storing IPv4 addresses
 - Different behaviour in Apache and nginx
 - Need to monitor and test 2 protocols instead of 1
 - More things to go wrong

# Problems deploying IPv6 (external, not always fixable)

 - Third party APIs which require IPv4 addresses
 - Stricter rules on mail over IPv6 (e.g. Google)
 - No obvious benefit for customers (c.f. PHP 5 -> PHP 7)
 - External solution: Google boosts IPv6 results

# Competition concerns

 - Still need IPv4 to start a hosting provider
 - Huge advantage to incumbents
 - Bumps up value of firms with allocations
 - Pay RIPE €2,000 + €1,400/year to become an LIR
 - RIPE 733: You might get a /24 if you're lucky (waiting list)
 - Regulatory requirement to deploy IPv6 (esp. ISPs)?

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
  - Credits: (list of providers who helped)
  - Questions?


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

# The problem with IPv4

 - Not enough addresses
 - Allocation pools exhausted in many areas
 - RIPE 733: You might get a /24 if you're lucky (waiting list)
 - IPv6 fix: more addresses (forget everything else)

# Current state of play

 - Draft standard 1998, ratified in 2017
 - Many hosting providers don't offer IPv6 at all
 - Some offer it but limited use cases
 - Very few big providers offer IPv6 with feature parity with IPv4
 - Unscientific test: 

# Squeezing the last drops from IPv4

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
 - Monitor both protocols - some software defaults to IPv4
 - More things to go wrong

# Problems deploying IPv6 (external, not always fixable)

 - Third party APIs which require IPv4 addresses
 - Stricter rules on mail over IPv6 (e.g. Google)
 - No obvious benefit for customers (c.f. PHP 5 -> PHP 7)
 - Lack of feature parity with IPv4 (e.g. no load balancers)

# How can we solve this?

 - Ask your hosting provider if they support v6
 - Regulatory requirement to deploy IPv6 (esp. ISPs)?
 - If Google gave IPv6 an SEO boost...

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


% Multi Factor Authentication in PHP
% Paul Waring (paul@phpdeveloper.org.uk)
% June 6, 2017

# whoami

 - Freelancing full-time since July 2015
 - PHP developer and Linux system administrator
 - Specialise in legacy code/systems and financial services
 - I like trains, politics and technology (@pwaring)
 - You may know me from: Geek Walks, Currybeer

# Topics

 - Mix of my experiences and practical advice
 - Why you might want to try freelancing (and why not)
 - How to make freelancing work
 - Whatever you want - ask me anything!

# What is Multi Factor Authentication?

 - Traditional authentication: something you know (username, password)
 - Additional factor: something you have access to (e.g. phone)
 - Additional factor: something you are (e.g. fingerprint)
 - Usually restricted to 2 factors
 - Different factors are generally what matters, not the number

# Why do we need MFA?

 - Passwords are often easy to guess
 - Passwords are leaked on a regular basis

# Email

 - Ubiqutous
 - You probably have this data already
 - Deliverability issues
 - Transmission security
 - Same mechanism as password reset
 - Arguably not MFA as email uses username/password

# SMS

  - Nearly universal
  - Deliverability issues, especially time
  - Security issues
  - Data protection
  - Cost to send and receive (in some countries)

# Smartphone app

 - Becoming universal
 - Google Authenticator
 - Windows Phone and Black Berry

# Yubikey

 - Limited browser support for U2F

# When not to use 2FA

 - Shared accounts
 - Accessibility
 - Minor sites, e.g. mailing lists
 - Best practice: optional for users, compulsory for admins

# Gotchas

 - User loses device
 - Setting session before 2FA complete

# Takeaways

 - 2FA is easy
 - Most of the work has been done for you
 - Implement it today

# Thanks for listening

  - Questions?
  - Slides at: talks.phpdeveloper.org.uk

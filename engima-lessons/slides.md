% Lessons Learned from Enigma
% Paul Waring (paul@xk7.net, @pwaring)
% April 6, 2017

# Background

 - World War 2: 1939 - 1945
 - Germany + others (Axis) vs Britain + others (Allies)

# Problem

 - Need to transmit messages across long distances
 - Sender and recipient are not in fixed locations
 - Messages are time sensitive
 - Line of sight not guaranteed
 - Cables take time to run and can be cut
 - Only available technology: radio

# Radio

 - Radio signals are broadcast
 - Anyone can listen
 - Anyone can broadcast
 - Need both identification and encryption
 - Ideally want integrity (but not in scope)
 - Will focus mainly on encryption (and breaking)

# Engima

 - Used for encrypting German messages in WW2

# Enigma as an example

 - Demonstrates flaws in design
 - Demonstrates flaws in operation
 - State vs state - significant resources available
 - Highest stakes possible
 - Probably the biggest 'hack' in history
 - War reduced by 1-2 years, millions of lives saved

# Traffic analysis

 - Can triangulate radio signals to get rough location
 - Track operators by fingerprint
 - Often tells you more than the message
 - Sometimes gives clues for cracking
 - Similar to metadata from emails, websites etc.

# Design

 - Enigma could never encrypt a character as itself
 - If you see 'A' in ciphertext, plaintext cannot be 'a'
 - Reduces key space by factor of 26 - so what?
 - Helps eliminate potential keys
 - Plaintext guessing

# Plaintext 'knowledge'

 - Knowing (or guessing) some of the plaintext helps with cracking
 - Knowing the position of plaintext is even better
 - Army reports tend to be structured and regular (e.g. weather)
 - 'Nothing to report' reports
 - Intentionally cause known messages to be sent

# Compromised keys

 - U-boats spent long times at sea so required monthly(?) books
 - Capture a U-boat and you have the keys
 - Germans did not always revoke keys after sinking (expensive)
 - Extremely dangerous operation, but rewarding
 - Still need cryptoanalysis to continue

# Per-message keys

 - Choose a new key per message, encrypted with the day book setting
 - Reduces the amount of ciphertext using the day book setting
 - Send key twice to avoid transmission problems
 - Repetition is bad!

# U-33

 - Sent to lay mines in Scottish waters
 - Normal procedure: no Enigma machines or codes on mine-layers
 - Ignored

# Security through obscurity

 - Germans careful to keep hold of Enigma machines

# Assumption of security

 - Occasionally not using decrypted messages

# Lessons learned

 - Key space can be reduced by flaws in design and operation
 - Reduced key space + automation = brute force can work
 - Repetition, re-use and regularity undermines cryptography
 - Traffic analysis can sidestep encryption and aid cracking
 - If keys are lost, assume they have been compromised
 - No system survives first contact with users

# Thanks for listening

 - Questions?
 - Slides at: talks.phpdeveloper.org.uk

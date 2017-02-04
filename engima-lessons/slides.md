# Engima

 - Used for encrypting German messages in WW2

# Enigma as an example

 - Demonstrates the flaws in design
 - Demonstrates the flaws in operation
 - State vs state - almost limitless resources
 - Highest stakes possible
 - Probably the biggest 'hack' in history
 - War reduced by 2 years, millions of lives saved

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

# Traffic identification and metadata

 - Can triangulate radio signals to get rough location
 - Track operators by fingerprint
 - Often tells you more than the message
 - Sometimes gives clues for cracking

# Plaintext 'knowledge'

 - Knowing (or guessing) some of the plaintext helps with cracking
 - Knowing the position of plaintext is even better
 - Weather and other structured reports
 - Intentionally cause known messages to be sent

# Lessons learned

 - Key space can be reduced by flaws in design and operation
 - Reduced key space + automation = brute force can work
 - Repetition, re-use and regularity undermines cryptography
 - Traffic analysis can sidestep encryption and aid cracking
 - If keys are lost, assume they have been compromised
 - Users are your weakest link

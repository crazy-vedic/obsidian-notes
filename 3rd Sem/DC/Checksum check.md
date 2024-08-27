Separate data into multiple segments, binary add them using 1s compliment
note: 1s compliment means the carry 1 is to be added normally after addition
Send the normal data along with the checksum as well.

ON receiver side, add the checksum portion to the data (sum of segments)
Answer should be 1 inf.

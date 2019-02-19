# Blowfish-algorithm-python
Implementation of blowfish algorithm in python.

# Algorithm for blowfish encryption and decryption-
# Encryption:
Take plaintext input.
Divide plaintext into two halves of 32 bit each.
For i=1 to 16
  left = left^p[i]
  Right = right ^ F(left)
  Left,right = swap (left,right)
  i++
Left,right = swap(left,right)
Left = left^p[18]
Right = right^p[17]
Combine left and right to get encrypted text.

# Decryption:
Take plaintext input.
Divide plaintext into two halves of 32 bit each.
For i=18 to 3
  left = left^p[i]
  Right = right ^ F(left)
  Left,right = swap (left,right)
  i++
Left,right = swap(left,right)
Left = left^p[0]
Right = right^p[1]
Combine left and right to get decrypted text.

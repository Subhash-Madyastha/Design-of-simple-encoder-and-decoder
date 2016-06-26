# Design-of-simple-encoder-and-decoder

1. convert an integer into a special text encoding and then
2. convert the encoded value back into the original integer.

Encoder Design:
1. Add 8192 to the raw value, so its range is translated to [0..16383].
2. Pack that value into two bytes such that the most significant bit of each is cleared.
3. Format the two bytes as a single 4-character hexadecimal string and return it.


Decoder Design:
Decoding function should accept two bytes on input, both in the range [0x00..0x7F] and recombine
them to return the corresponding integer between [-8192..+8191].

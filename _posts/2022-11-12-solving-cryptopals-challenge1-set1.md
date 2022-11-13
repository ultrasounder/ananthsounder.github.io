# Day 1

## This is my first day of solving the cryptopals challenges. Challenges 1 set 1. 

## [Convert hex to base64](https://cryptopals.com/sets/1/challenges/1)

### You are provided an input string:
    ```49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d```

### which should produce this;
    ```SSdtIGtpbGxpbmcgeW91ciBicmFpbiBsaWtlIGEgcG9pc29ub3VzIG11c2hyb29t```

### This will be a two step-process
1. Decoding Hex to Raw-Bytes
2. Converting Raw-Bytes to base64


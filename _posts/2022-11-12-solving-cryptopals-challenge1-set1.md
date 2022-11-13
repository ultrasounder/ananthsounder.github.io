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

> 

The problem here is that the input is standard string. It works as long as you have strings as your input. But we are using  bytes as our input. So, we need to convert our string to rawbytes.
Python standard library to the rescue. Python has the base64 library which includes functions b16decode and b64encode.

>

### Two-step process 😊

1. we will use the b16decode to decode raw hex bytes to b16 format.
2. we will then use the b64encode to encode the b16 into base64 which is what the problem wants.

[Talk is cheap. Show me the code!](https://www.goodreads.com/quotes/437173-talk-is-cheap-show-me-the-code)

`

            from base64 import b16decode, b64encode

            def hex_to_b64(data_hex: bytes) -> bytes:
                return b64encode(b16decode(data_hex, casefold=True))

            if __name__ == "__main__":

                data_hex = b"49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d"  
                data_b64 = hex_to_b64(data_hex)

                print(f"{data_hex=}")
                print(f"{data_b64}")

    `
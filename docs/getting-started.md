# Getting Started

## Tools
Currently most of the works are manual through the use of a Hex Editor. One of the most popular one available is [HxD](https://mh-nexus.de/en/hxd/), a free to download Hex Editor with a good variety of features.

Furthermore, as you will be working mostly with Base16 number, a way to convert back and forth between Hexadecimal and Decimal numbers is recommended. There are multiple converters freely available online.

## Technical Terms
### Endianess
The games store numbers using Little Endian, as oppose to Big Endian. Big Endian is what we use to refer numbers, with the most significant digit goes first, and the further along a number, the less significant the digits become. Little Endian, on the other hand, puts the most significant digit last. For example:
```
# Big Endian
256 (Decimal) -> 01 00 (Hexadecimal)
# Little Endian
256 (Decimal) -> 00 10 (Hexadecimal)
```

Keep this in mind as you traverse the files searching for a number.

### Specific Terms Breakdown
Throughout the documentation, certain terms will be used to describe certain things. Those terms are as followed:
```
# Normal type
byte:   1 byte of data.
short:  2 bytes of data.
int:    4 bytes of data.
float:  4 bytes of data, in float format.
String: A series of bytes until the \x00 (null) character is encountered.

# Array
type[length]:   Consecutive bytes of `type` that is `length` long.
```

If another term is encountered, it will be explained in the same article.

## Pick a Game to Start
* [Trails of Cold Steel](cs1/overview.md)
* [Trails of Cold Steel 3](cs3/overview.md)
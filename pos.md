Structure
=========

For example, this is a real-world PoS block in Crown LIVENET blockchain. It's generated at `2019-04-17T11:02:09Z`. All Crown blocks generated nowadays are PoS blocks.

In the blockchain file, the whole data related to this block is as follows (625 bytes):

```
b8 eb b3 df 69 02 00 00 02 02 16 00 84 e3 e8 16 0a 14 7f 90 09 ec 23 4b 41 f7 5d f6 74 1d 1a 8c
55 cd 22 c3 b6 13 68 53 db 5c 7b 0c 88 9f 2a 8a 6a 98 2a 2a 0e 34 6e 0c ff 40 63 33 66 f4 db a6
76 19 59 1a 27 86 1c eb b7 69 24 bd b1 07 b7 5c 99 63 04 1d 00 00 00 00 02 01 00 00 00 01 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 ff ff
ff ff 05 03 19 a1 23 00 ff ff ff ff 03 00 00 00 00 00 00 00 00 00 40 e0 06 0b 00 00 00 00 19 76
a9 14 c0 c3 fa ba 85 d8 b4 60 9e 8e a9 e6 48 6a 2f bc 0a ca 2a ce 88 ac 00 5a 62 02 00 00 00 00
19 76 a9 14 fa 23 c7 67 5f a4 c2 39 64 76 04 ed c5 ac be 57 c5 26 52 39 88 ac 00 00 00 00 01 00
00 00 01 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 ff ff ff ff 06 c0 03 19 a1 23 00 ff ff ff ff 01 80 d1 f0 08 00 00 00 00 19 76 a9 14 1a
da 8a 1f 1f cc 64 04 6a ac 24 e1 0a 00 91 fc a6 3d 67 ed 88 ac 00 00 00 00 47 30 45 02 21 00 ba
e0 98 5e 39 96 0c f4 bf 66 fe 0e 50 24 40 06 a4 27 c8 91 07 e4 17 27 d1 0d 7f 13 83 57 9a be 02
20 21 a6 b3 1a 1e 57 6f 4c a2 4d c3 a1 39 b8 5d 17 0c 24 17 25 91 e5 39 18 db e9 fa 3d d7 27 ae
eb 28 c1 eb 24 0e 12 66 75 d5 04 17 62 d2 f7 66 6e f5 40 15 22 73 54 09 fe e2 ef e6 f9 c7 a6 ea
2f 13 54 9c 86 5f 6d e9 72 00 92 20 99 39 65 ad 1e e2 ca c5 f7 7a a7 13 f6 0d 9f 5e b7 1b df 81
9d 01 00 00 00 41 04 2a 13 16 12 46 8d 7f 62 5a 4c 90 1a 0b 5c 55 0d 0b 46 d5 5f 2c ac d8 85 2f
6a 64 0d c7 9d 85 3c 58 b3 c2 c8 88 c5 93 8e 0e 77 f4 ac 15 4d f1 1b 81 eb e4 e7 c3 94 d2 eb 00
9f 16 f3 88 8c 38 bd 21 03 35 8a 22 8e 7f b7 cd fd 4a 8d 65 ab ea 32 32 94 85 85 fd 7f f6 8a 08
cf 43 50 82 67 d5 81 f4 79 47 30 45 02 21 00 a2 6a 59 da 4b eb 76 5f c6 90 fb ab e9 9d 20 26 75
1d d3 d0 03 ed 89 b1 a8 01 e7 c3 ae c0 1a f8 02 20 35 8e e9 c6 90 71 6c 4c 87 8d 1f 36 cd b4 32
f0 df 37 26 0b 36 31 89 24 8c 3a 02 be 7b 95 7b 39
```

`b8 eb b3 df` is the magic. Next to it is `69 02 00 00`, which means the block size (617 bytes). To be accurate, "block" refers to 617 bytes, not 625 bytes.

The first part of the block is the block header, which is fixed to 80 bytes:

```
02 02 16 00 // Version

// Previous Block Hash
84 e3 e8 16 0a 14 7f 90 09 ec 23 4b 41 f7 5d f6 74 1d 1a 8c 55 cd 22 c3 b6 13 68 53 db 5c 7b 0c

// Merkle Root
88 9f 2a 8a 6a 98 2a 2a 0e 34 6e 0c ff 40 63 33 66 f4 db a6 76 19 59 1a 27 86 1c eb b7 69 24 bd

b1 07 b7 5c // Timestamp
99 63 04 1d // Bits
00 00 00 00 // Nonce
```

Then, transactions:

```
02 // Transaction Count

/* First Transaction Begin */

01 00 00 00 // Version

01 // TxIn Count

// Previous Out
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
ff ff ff ff

05 // Script Size
03 19 a1 23 00 // Script
ff ff ff ff // Sequence Number

03 // TxOut Count

00 00 00 00 00 00 00 00 // Amount of First TxOut
00 // Script Size (0 bytes)

40 e0 06 0b 00 00 00 00 // Amount of Second TxOut
19 // Script Size (25 bytes)
76 a9 14 c0 c3 fa ba 85 d8 b4 60 9e 8e a9 e6 48 6a 2f bc 0a ca 2a ce 88 ac // Script

00 5a 62 02 00 00 00 00 // Amount of Third TxOut
19 // Script Size (25 bytes)
76 a9 14 fa 23 c7 67 5f a4 c2 39 64 76 04 ed c5 ac be 57 c5 26 52 39 88 ac // Script

00 00 00 00 // Lock Time

/* First Transaction End */

/* Second Transaction Begin */

01 00 00 00 // Version

01 // TxIn Count

// Previous Out
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
ff ff ff ff

06 // Script Size
c0 03 19 a1 23 00 // Script
ff ff ff ff // Sequence Number

01 // TxOut Count

80 d1 f0 08 00 00 00 00 // Amount
19 // Script Size (25 bytes)
76 a9 14 1a da 8a 1f 1f cc 64 04 6a ac 24 e1 0a 00 91 fc a6 3d 67 ed 88 ac // Script

00 00 00 00 // Lock Time

/* Second Transaction End */
```

Finally, block signature and stake pointer:

```
47 // Size
30 45 02 21 00 ba e0 98 5e 39 96 0c f4 bf 66 fe 0e 50 24 40 06 a4 27 c8 91 07 e4 17 27 d1 0d 7f
13 83 57 9a be 02 20 21 a6 b3 1a 1e 57 6f 4c a2 4d c3 a1 39 b8 5d 17 0c 24 17 25 91 e5 39 18 db
e9 fa 3d d7 27 ae eb

// Stake Pointer Block Hash
28 c1 eb 24 0e 12 66 75 d5 04 17 62 d2 f7 66 6e f5 40 15 22 73 54 09 fe e2 ef e6 f9 c7 a6 ea 2f

// Stake Pointer Transaction Hash
13 54 9c 86 5f 6d e9 72 00 92 20 99 39 65 ad 1e e2 ca c5 f7 7a a7 13 f6 0d 9f 5e b7 1b df 81 9d

01 00 00 00

41 // Size (65 bytes)
04 2a 13 16 12 46 8d 7f 62 5a 4c 90 1a 0b 5c 55 0d 0b 46 d5 5f 2c ac d8 85 2f 6a 64 0d c7 9d 85
3c 58 b3 c2 c8 88 c5 93 8e 0e 77 f4 ac 15 4d f1 1b 81 eb e4 e7 c3 94 d2 eb 00 9f 16 f3 88 8c 38
bd

21 // Size (33 bytes)
03 35 8a 22 8e 7f b7 cd fd 4a 8d 65 ab ea 32 32 94 85 85 fd 7f f6 8a 08 cf 43 50 82 67 d5 81 f4
79

47 // Size (71 bytes)
30 45 02 21 00 a2 6a 59 da 4b eb 76 5f c6 90 fb ab e9 9d 20 26 75 1d d3 d0 03 ed 89 b1 a8 01 e7
c3 ae c0 1a f8 02 20 35 8e e9 c6 90 71 6c 4c 87 8d 1f 36 cd b4 32 f0 df 37 26 0b 36 31 89 24 8c
3a 02 be 7b 95 7b 39
```

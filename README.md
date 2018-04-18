# bitchain

Bitchain is a distributed filesystem based on the concepts of blockchains.

Imagine being able to keep your files encrypted with unique keys for each file without the need to keepup with the keys.

...that's what Bitchain does!

Files are divided into a chain of blocks, each block contains a section of the file as well as an encryption key for the previous block of the chain making an inverse blockchain. In this way, as long as you have the full list of blocks and know the proper order of, you can start with the nth block and decrypt the blocks by going back up the chain.

Two blocks break this pattern however: the root(first) node and the leaf(last) node.

Rather than containing data, the leaf node contains the encrypted key for node n-1 as well as the unencrypted key for the root node.

As for the root node, it contains the unencrypted key for the leaf node's encrypted key portion as well as padding to make node look like a normal node.

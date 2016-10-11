# IP-Adress-Checker
Check if an internet IP address falls within an IP address block

# Overview

This program performs computations on IP blocks. As you may already know, Internet Protocol version 4 (IPv4, or often just IP) is the main network protocol used on the Internet.

An IP address, which identifies a computer on the Internet, is an unsigned 32-bit integer. It is traditionally written as four 8-bit numbers, with the highest (most significant) number first, separated by dots. For example, the IP number 0xACD9002E is written "172.217.0.46".

An IP block, often called a subnet, is a group of IP addresses that share the same bit prefix: all addresses in the block share the same leading (most significant) bits, in their binary representation. The block is traditionally written as an IP address followed by a slash and the number of bits in the prefix. The prefix size is between 0 and 32.

For example, "172.217.0.46/24" is the block consisting of all addresses that share the same first 24 bits with 172.217.0.46. This block contains all addresses of the form 172.217.0.x, since the first 24 bits are specified but the last 8 may take any value.

The number of addresses in the block is determined by the size of the prefix. For example, "172.217.0.46/24" contains 256 addresses.


# block membership

Start by writing a console (shell or terminal) program that takes two arguments on its command line: an IP block and and IP address. The program should parse the block and address in the formats described above. It should then print a message indicating whether or not the address is in the block.

For example, for this invocation, ($ is the shell prompt; ipblock is the program you will write),

$ ipblock 12.23.34.45/15 12.22.35.44
the program responds,

in block
while for this invocation,

$ ipblock 12.23.34.45/16 12.22.35.44
the program responds,

not in block

Once you are satisfied that your code works for basic cases, add some tests to confirm this. Which test cases are you most concerned about?


# Conclusion

If you are curious about what IP blocks are used for, see the Wikipedia page on CIDR.

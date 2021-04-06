# portxch

A weird library that uses port nubmers to transfer data. It's probably helpful for XSS exploit development.


## Explanation

Let's say we wanted to send the binary string `01000001` (ASCII letter A). We can create a TCP server that 
listens on two ports, e.g. 7000 and 7001. We recieve a `0` when someone connects to the first port, and a 
`1` for the second port. Hence, we can transfer arbitrary binary data.

The same idea works for arbitrary bases, e.g. as hexadicmal (16 ports) or base64 (64 ports). With 256 ports, 
we can reliably send about 16 bytes per second. Cool!

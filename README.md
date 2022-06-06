# ssend: Unsecure file transfer for VPN

## Why Bother

These bash scripts offer a speedy method for sending a file from a client to
a server using TCP/IP networking. Scp could be used for this purpose, but
will often be slower. These scripts do not employ encryption of any sort, so
they are most suitable for use where both client and server are contained in
a secure environment such as a VPN.

## Prerequisites

Both client and server require that `socat` be in the shell PATH. If you have
`pv` (pipe viewer) in your path, you can "tune" the client program to use it.
This would yield an animated progress bar while transferring a file.

## Programs

### srecv_server2

This is the server, it receives files from clients. Launch it once and it
will service multiple clients. Launch without arguments to obtain a help
message. At the top of the file are some tuning parameters that you can change.

### ssend2

This is the client, it sends a single file to a remote server ('srecv_server2`).
Launch it once and it will service multiple clients. Launch without arguments
to obtain a help message. At the top of the file are some tuning parameters
that you can change.

## Testing

I have tested `ssend2` on Linux. I have tested `srecv_server2` on MacOS.

## Bugs

The client program `ssend2` does not provide feedback when the server
encounters an error.

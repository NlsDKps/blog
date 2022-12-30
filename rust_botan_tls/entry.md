# Botan TLS in the Rust gRPC implementation

## What is TLS?

## Building the reference implementation in C++

The reference implementation is based on (this)[1] documentation.

Botan supports client and server implementations of several versions of the TLS protocol. For this 
project we aim to support at least TLS v1.2. To implement a TLS secured socket, it utilizes a
callback provided by the user (`output_fn`) to write data, it would like to send to the remote. When
data is received from the remote, the information is passed to botans TLS by using
`TLS::Channel::received_data`. The data passed in results in a change of the current TLS state and
the appropriate user provided callback is invoked.

## TLS in the Botan wrapper

## Botan TLS in Rust gRPC

[1][https://botan.randombit.net/handbook/api_ref/tls.html]

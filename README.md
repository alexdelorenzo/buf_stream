buf_stream
=========

Buffered I/O streams for reading/writing

## About
`buf_stream` is a fork of [bufstream](https://github.com/alexcrichton/bufstream) by Alex Chrichton. 

## Usage

```toml
[dependencies]
buf_stream = "0.2"
```

## Tokio

There is support for tokio's `AsyncRead` + `AsyncWrite` traits through the `tokio`
feature. When using this crate with asynchronous IO, make sure to properly flush
the stream before dropping it since IO during drop may cause panics. For the same
reason you should stay away from `BufStream::into_inner`.


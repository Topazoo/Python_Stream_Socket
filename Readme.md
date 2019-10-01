# Python WebSocket Stream

[![AngularJS](https://img.shields.io/badge/Python-3.5.7+-blue.svg)](https://www.python.org/downloads/)
[![websockets](https://img.shields.io/badge/websockets-8.0.2-green.svg)](https://pypi.org/project/websockets/)

### An easy to use, non-blocking WebSocket server for streaming data.

#### Author: Peter Swanson

## Overview

An "Advantageous" Python WebSocket streaming server that constantly streams data from a passed generator and (optionally) reads a response from the client at the same time.

## Installation

1. Install _websockets_.

```bash
    $ pip install websockets
```

2. Clone this repo or copy Stream_Socket.py to your project.

```bash
    $ git clone https://github.com/Topazoo/Python_Stream_Socket.git
```

## Sample Usage

```Python
from Stream_Socket import Socket_Stream_Server

def sample_generator():
    while True:
        yield random.choice([{'data': 'Hello'}, {'data': 'World'}])

server = Socket_Stream_Server(
            path='127.0.0.1',
            port=5001,
            generator=sample_generator,
            callback=print
        )

server.run()
```

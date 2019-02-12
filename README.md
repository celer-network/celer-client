# Celer Client

## Overview

This repository provides prebuilt client binaries running gRPC API servers that
enable applications to interact with Celer Network. In particular, the gRPC
messages are transported over WebSocket to allow bidirectional streaming from
JavaScript applications in NodeJS and browsers.

## Usage

```
./celer_client_mac -keystore <path-to-keystore-json> -config <path-to-profile-json> -port <port-number>
```

Enter the password for the keystore when promted.

By default, the web API server will be started at `http://localhost:29979`.

See the [Celer Web SDK](https://github.com/celer-network/Celer-Web-SDK) for the
JavaScript APIs.

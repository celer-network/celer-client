# Celer Client

## Overview

This repository provides a prebuilt client binary running a gRPC API server that
enables JavaScript applications to interact with Celer Network in both NodeJS
and browser environments.

## Usage

```
./celer_client_mac -keystore <path-to-keystore-json> -config <path-to-profile-json> -port <port-number>
```

Enter the password for the keystore when prompted. Note that a local folder
`celer-hackathon-ropsten` will be created. The folder contains the your
off-chain states that must be preserved for all interactions with Celer Network.
The path of the directory is configurable via the `StoreDir` field in
`profile.json`.

By default, the web API server will be started at `http://localhost:29979`.

See the [Celer Web SDK](https://github.com/celer-network/Celer-Web-SDK) for the
JavaScript APIs.


# Celer Client

## Overview

This repository provides a prebuilt client binary running a gRPC API server that
enables JavaScript applications to interact with Celer Network in both NodeJS
and browser environments.

## Usage

```
./celer_client_mac -keystore <path-to-keystore-json> -config <path-to-profile-json> -port <port-number>
```

Enter the password for the keystore when prompted.

By default, the web API server will be started at `http://localhost:29979`.

See the [Celer Web SDK](https://github.com/celer-network/Celer-Web-SDK) for the
JavaScript APIs.

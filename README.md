# Note

This go client is experimental and intended to be used as an alternative approach for non mobile hacker. It does not support all celer functionality as mobile SDK does.

## Overview

This is a simple wrapper of celer go lib providing simple conditional payment functionality through http request. 

```
usage: celer_client [<flags>]

Flags:
      --help         Show context-sensitive help (also try --help-long and --help-man).
  -w, --password=""  Password for the key store.
  -d, --amount="4563918244f40000"
                     The deposit to open channel
  -p, --port="8080"  Port the API will use
  -k, --keyFile="key.json"  Key store file path
```
  
## Setup

1. Put `profile.json` and `key.json` into the same directory with the client
2. `./celer_client -w [password for key store]`


## API

* POST `/stat` --- Get current user balance statistics

```
{
  Option: number --- 1 for local query, 2 for on-chain query
}
```

* POST `/sendPay` --- Send payment to another party


```
{
  Dst: string --- destination address,
  Dependency: string ---  onchain dependency contract address,
  Amount: string --- payment amount,
  QueryFinalization: byte --- a byte array used for isFinalized query,
  QueryResult: byte --- a byte array used for condition resolution query,
  Timeout: number --- wait number of blocks until the condition expires
}
```

* POST `/resolveChannel` --- Resolve channel payment

```
{
  Dependency: string ---  onchain dependency contract address
}
```

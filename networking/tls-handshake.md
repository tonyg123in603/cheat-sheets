# TLS Handshake
A TLS handshake takes place whenever a user navigates to a website over HTTPS and the browser first begins to query the website's origin server. A TLS handshake also happens whenever any other communications use HTTPS, including API calls and DNS over HTTPS queries.

SSL, was the original encryption protocol developed for HTTP. SSL was replaced by TLS. SSL handshakes are now called TLS handshakes, although the "SSL" name is still in wide use.

## Steps of a TLS handshake
### Diagram
```
┌───────────────┐                      ┌───────────────┐
│     CLIENT    │                      │     SERVER    │
└───────┬───────┘                      └───────┬───────┘
        │                                      │
        │ 1. SYN                               │
        │ ───────────────────────────────────► │
        │                                      │
        │                           2. SYN/ACK │
        │ ◄─────────────────────────────────── │
        │                                      │
        │ 3. ACK                               │
        │    ClientHello                       │
        │ ───────────────────────────────────► │
        │                                      │
        │                   4. ServerHello     │
        │                      Certificate     │
        │                      ServerHelloDone │
        │ ◄─────────────────────────────────── │
        │                                      │
        │ 5. ClientKeyExchange                 │
        │    ChangeCipherSpec                  │
        │    Finished                          │
        │ ───────────────────────────────────► │
        │                                      │
        │                  6. ChangeSipherSpec │
        │                     Finished         │
        │ ◄─────────────────────────────────── │
        │                                      │
```

### Steps

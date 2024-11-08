# DPI Tunnel Lite

**Version:** 5.0.0 stable as of 08.11.2024  
**Developer:** game-over-op

## Project Description

DPI Tunnel Lite is a lightweight version of a tunneling application designed to bypass restrictions, offering better performance compared to [DPI Tunnel + Dns only](https://4pda.to/forum/index.php?showtopic=915158&view=findpost&p=131876732).

## Technical Requirements

- **Magisk:** Version 19 or higher
- **Android:** 11 or higher

## Settings and Parameters

### Proxy and Tunnel Settings:

- `--mode=<mode>`  
  Sets the proxy mode. Options are: `proxy` (default) or `transparent`.  
  **Example:** `--mode=transparent`.

- `--ca-bundle-path=<path>`  
  Path to the CA certificate bundle file in PEM format for SSL.  
  **Default:** `./ca.bundle`.  
  **Example:** `--ca-bundle-path=/path/to/ca.bundle`.

### Security and Blocking Circumvention Settings:

- `--buffer-size=<size_in_bytes>`  
  Size of the data buffer in bytes. Default is 512.  
  **Example:** `--buffer-size=1024`.

- `--desync-attacks=[<mode0>][,<mode1>]`  
  Defines desynchronization attacks, including `fake rst`, `rstack`, `disorder`, `split`.  
  **Example:** `--desync-attacks=fake,disorder_fake`.

- `--split-at-sni`  
  Enables Client Hello splitting by SNI.

- `--split-position=<offset_in_bytes>`  
  Splits Client Hello at the specified byte. Default is 3.  
  **Example:** `--split-position=5`.

- `--wrong-seq`  
  Sends fake packets with previous SEQ/ACK values.

### TTL and Auto-TTL Parameters:

- `--ttl=<number>`  
  Sets TTL for fake packets.  
  **Example:** `--ttl=5`.

- `--auto-ttl=<a1>-<a2>-<m>`  
  Defines TTL based on distance using parameters `a1`, `a2`, and `m`.  
  **Default:** `1-4-10`.  
  **Example:** `--auto-ttl=2-5-10`.

- `--min-ttl=<number>`  
  Minimum TTL at which fake packets are sent.  
  **Example:** `--min-ttl=3`.

### DNS Settings:

- `--doh`  
  Enables DoH (DNS over HTTPS) for domain resolution.

- `--doh-server=<url>`  
  URL for the DoH server.  
  **Default:** [https://dns.google/dns-query](https://dns.google/dns-query).  
  **Example:** `--doh-server=https://cloudflare-dns.com/dns-query`.

- `--builtin-dns`  
  Enables the built-in DNS resolver for Android.

- `--builtin-dns-ip=<ip>`  
  IP address of the DNS server for the built-in resolver.  
  **Default:** `8.8.8.8`.  
  **Example:** `--builtin-dns-ip=1.1.1.1`.

- `--builtin-dns-port=<port>`  
  Port for the DNS server used by the built-in resolver.  
  **Default:** `53`.  
  **Example:** `--builtin-dns-port=5353`.

### TCP Settings:

- `--wsize=<number>`  
  Sets the TCP window size for splitting the Server Hello.  
  **Example:** `--wsize=64`.

- `--wsfactor=<number>`  
  Multiplier for TCP window scaling used with `wsize`.  
  **Example:** `--wsfactor=6`.

## Notes

- If a hosts file is present on the device, the module will ignore it. This feature may be added in a future update.

## Download

You can download the latest version of DPI Tunnel Lite:

- [Standard Version](https://example.com/download/standard_version)  
- [DNS Version from comss](https://example.com/download/comss_version)

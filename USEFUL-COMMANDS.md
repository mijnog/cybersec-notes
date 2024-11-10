### Privilege Escalation (Linux) to be used in conjunction with [GTFOBins](https://gtfobins.github.io/gtfobins/base64/)

#### List files that have SUID or SGID bits set:

```bash
find / -type f -perm -04000 -ls 2>/dev/null
```

#### List "Capabilities"
```bash
getcap -r / 2>/dev/null
```
Getcap will generate many errors, so redirect `stderr` to `/dev/null` to quiet the output.

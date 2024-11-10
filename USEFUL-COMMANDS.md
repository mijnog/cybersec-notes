### Privilege Escalation (linux)

List files that have SUID or SGID bits set:

```find / -type f -perm -04000 -ls 2>/dev/null```

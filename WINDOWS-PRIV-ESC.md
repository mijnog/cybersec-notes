# Low Hanging Fruit
**Token Abuse**

Check for `SeImpersonatePrivilege` with:
- `whoami /priv`

If `SeImpersonatePrivilege` is enabled, use:
- `PrintSpoofer` or `GodPotato`
- `JuicyPotato` (on older systems)

---

**PrintSpoofer**
Exploits the Windows Print Spooler service (`spoolsv.exe`). It forces the `SYSTEM`-privileged `spoolsv.exe` to connect to an attacker-controlled named pipe, allowing the attacker to impersonate the `SYSTEM` account and execute code.

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


SeDebugPrivilege: Allows a user to open and debug any process, for dumping credentials from memory (e.g. from the LSASS process).

SeTakeOwnershipPrivilege: Allows a user to take ownership of any object (like files or registry keys), which can then be used to modify permissions and inject malicious code.

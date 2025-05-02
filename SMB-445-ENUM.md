## ENUMERATE SHARES ANONYMOUSLY
**smbclient**
- `smbclient -L $VICTIM_IP -N #-L lists shares -N no-user`

- `smbclient //$VICTIM_IP/$SHARE_NAME -U $USERNAME` 
the smb server will prompt for the user's password

**nmap**
- `nmap --script smb-enum* 10.10.10.11`
- `nmap --script smb-vuln* 10.10.10.11`

# Other tools

- **smbmap**
- **crackmapexec**

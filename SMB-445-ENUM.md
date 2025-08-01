## SMB ENUMERATION
**smbclient**
- `smbclient -L $VICTIM_IP -N #-L lists shares -N no-user`

- `smbclient //$VICTIM_IP/$SHARE_NAME -U $USERNAME #the smb server will prompt for the user's password`

**nmap**
- `nmap --script smb-enum\* $VICTIM_IP`
- `nmap --script smb-vuln\* $VICTIM_IP`

### Other tools

- **smbmap**
- **crackmapexec**
- **enum4linux**

#### Connect to a share:
`smbclient //$VICTIM_IP/Users -U 'username'`
`smbclient //$VICTIM_IP/Users -U 'guest'`
`smbclient //$VICTIM_IP/Users -U 'username' -p 'password'`
Connect to a specific share e.g. `IPC$`
`smbclient //10.10.234.187/IPC$ -U 'guest'`

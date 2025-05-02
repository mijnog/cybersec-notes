## ENUMERATE SHARES ANONYMOUSLY
**smbclient**
- `smbclient -L $VICTIM_IP -N #-L lists shares -N no-user`

- `smbclient //$VICTIM_IP/$SHARE_NAME -U $USERNAME` 

Will prompt for a password

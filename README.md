# consul-plugins-sssd

This Cloudbreak recipe aims to configure SSSD service inside Cloudbreak Ambari containers.

Please note that this configuration works for AD 2003R2 and AD 2008, because they use pretty much RFC2307bis compliant attribute names.
To support UNIX clients with AD 2003 or older, you must install Microsoft Services For Unix and map LDAP attributes onto msSFU30* attribute names.

LDAP user attributes for SSSD:
[objectClass]
[uid]
[userPassword]
[employeeNumber]
[roomNumber]
[gecos]
[homeDirectory]
[loginShell]
[krbPrincipalName]
[cn]
[entryUUID]
[modifyTimestamp]
[shadowLastChange]
[shadowMin]
[shadowMax]
[shadowWarning]
[shadowInactive]
[shadowExpire]
[shadowFlag]
[krbLastPwdChange]
[krbPasswordExpiration]
[pwdAttribute]
[authorizedService]
[accountExpires]
[userAccountControl]
[nsAccountLock]
[host]
[loginDisabled]
[loginExpirationTime]
[loginAllowedTimeMap]
[sshPublicKey]

LDAP group attributes for SSSD:
[objectClass]
[cn]
[userPassword]
[gidNumber]
[memberuid]
[modifyTimestamp]
[modifyTimestamp]

Other useful SSSD configurations:
[ldap_user_search_base]
[ldap_group_search_base]

For more details how to configure SSSD please visit the user manuals: (sssd)[http://linux.die.net/man/5/sssd.conf], (LDAP)[http://linux.die.net/man/5/sssd-ldap], (Active Directory)[http://linux.die.net/man/5/sssd-ad]

# consul-plugins-sssd

This Cloudbreak recipe aims to configure SSSD service inside Cloudbreak Ambari containers.

An example Active Directory domain. Please note that this configuration
works for AD 2003R2 and AD 2008, because they use pretty much RFC2307bis
compliant attribute names. To support UNIX clients with AD 2003 or older,
you must install Microsoft Services For Unix and map LDAP attributes onto
msSFU30* attribute names.
# elastix-change-admin-pass
How to change the elastix admin password for the web backend


/usr/bin/sqlite3 /var/www/db/acl.db "UPDATE acl_user SET md5_password = '`echo -n thisisthenewpassword|md5sum|cut -d ' ' -f 1`' WHERE name = 'admin'"

#***************************
# Scripts
#***************************

Some bash scripts I wrote.

#***************************
# mampdebug
#***************************

This script will monitor the error log files for MAMP.  To set up, place the path to your log files in the variable MYPATH.
If you choose, create an alias to the script file.

The -a flag is mandatory, and it is followed by either "php" or "mysql".  It will monitor the corresponding error log.
The -c flaf will first clear the file before monitoring.  The -m flag will not run the script but display the usage file.

#***************************
# patchlocaldb
#***************************

To set this up, you must add the ssh user@host to the variable SSHLOC.  Then update the DBHOST and DB variables as
appropriate for your system.

This script can take one argument, which would be the path to the dump.sql file to patch the database with.  If you
provide no arguments, it will ssh into the server, find the most recent DEV_DUMP_*.sql file, download it,
patch the database, and delete the file.

This script will prompt you for your password twice.  This is a hastle, and can be rectified by setting up SSH Key login
to the server the script will SSH to.  A google search will yield results on how to do this, it does not take long.


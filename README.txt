#========================================================\
#
#    ♥ ♥ ♥ Make a copy of all files ending in .log 
#    and encrypt them for the recipient via gpg. ♥ ♥ ♥
#   
#===================================================================/

#Usage:
bubble-copter 13845604 /var/log/
#Or:
bubc root@localhost
# The first argument is the recpient of the encrypted message, the gpg -r.
# The second argument is the path to the log files.

# I Like to cron it up in roots crontab... example:
0 1 * * * /usr/local/bin/bubc root@localhost /var/log/
0 2 * * * /usr/local/bin/bubc root@localhost /var/tmp/
0 3 * * * /usr/local/bin/bubc users@localhost /home/*/log/
# Simple shell code methods as a wrapper around gpg, nothing special.

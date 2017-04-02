#========================================================\
#
#    ♥ ♥ ♥ Make a copy of files with the date and host
#    and encrypt them for the recipient via gpg. ♥ ♥ ♥
#   
#===================================================================/

#Usage:
bubble-copter 13845604 /var/log/
#Or:
bubc root@localhost
# The first argument is the recipient of the encrypted message, the gpg -r.
# The second argument is the path to the log files.
# The third argument is a regular expression after * matching files that end with the specified regex.
# The third argument is optional but the first and second are not.

# I Like to cron it up in roots crontab... example:
0 1 * * * /usr/local/bin/bubc root@localhost /var/log/ log
0 2 * * * /usr/local/bin/bubc root@localhost /var/tmp/ out
0 3 * * * /usr/local/bin/bubc users@localhost /home/*/ txt
# Simple shell code methods as a wrapper around gpg, nothing special.

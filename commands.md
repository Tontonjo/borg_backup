# Please find here some commands :-)

apt-get install borgbackup

borg init -e authenticated /path/to/repository

borg mount /path/to/repository /path/to/mountpoint

# Docker borg Server:

create a folder that will host your keys:
'mkdir -p borg/sshkeys/clients'

# borg_backup

# Tonton Jo - 2021
Join me on Youtube: https://www.youtube.com/c/tontonjo

If you find this usefull, please think about a sub to support :-)

# GENEARL USAGE
Install borg Backup for your distribution

- Instructions can be found in [commands.txt](https://github.com/Tontonjo/borg_backup/blob/main/commands.txt)

Initialize your backup target: borg init -e authenticated /path/to/backup

Backup the passphase and datastore key as suggested

Copy the borg_backup.sh script on your server

Edit BORG_REPO to your datastore /path/to/backup

Edit BORG_PASSPHRASE to the one you choose when you inited the repository

Edit /folder1 /folder2/data to the folders you want to backup

Edit --exclude as needed

Edit Retention policy

Run script with "bash borg_backup.sh" Use a cronjob to run it on a daily basis

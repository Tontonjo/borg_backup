# borg_backup

## Tonton Jo  
### Join the community:
[![Youtube](https://badgen.net/badge/Youtube/Subscribe)](http://youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw?sub_confirmation=1)
[![Discord Tonton Jo](https://badgen.net/discord/members/h6UcpwfGuJ?label=Discord%20Tonton%20Jo%20&icon=discord)](https://discord.gg/h6UcpwfGuJ)
### Support my work, give a thanks and help the youtube channel:
[![Ko-Fi](https://badgen.net/badge/Buy%20me%20a%20Coffee/Link?icon=buymeacoffee)](https://ko-fi.com/tontonjo)
[![Infomaniak](https://badgen.net/badge/Infomaniak/Affiliated%20link?icon=K)](https://www.infomaniak.com/goto/fr/home?utm_term=6151f412daf35)
[![Express VPN](https://badgen.net/badge/Express%20VPN/Affiliated%20link?icon=K)](https://www.xvuslink.com/?a_fid=TontonJo)  
# GENEARL USAGE
Install borg Backup for your distribution

- Instructions can be found in [commands.md](https://github.com/Tontonjo/borg_backup/blob/main/commands.md)

### Initialize your backup repository 
```ssh
borg init -e keyfile /path/to/backup
```
```ssh
borg init -e keyfile ssh://borg@10.0.0.171:2222/path/to/backup
```
### Backup the passphase and datastore key as suggested

Copy the borg_backup.sh script on your server

Edit BORG_REPO to aim at your local or remote datastore

Edit BORG_PASSPHRASE to the one you choose when you inited the repository

Edit /folder1 /folder2/data to the folders you want to backup

Edit --exclude as needed

Edit Retention policy

Run script with
```ssh
bash borg_backup.sh" 
```
Use a cronjob to run it on a daily basis

## Export repository key - Important
```ssh
 borg key export /path/to/backup /path/to/key
```

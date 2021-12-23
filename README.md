# borg_backup

## Tonton Jo - 2021  
### Join the community:
[![Youtube channel](https://github-readme-youtube-stats.herokuapp.com/subscribers/index.php?id=UCnED3K6K5FDUp-x_8rwpsZw&key=AIzaSyA3ivqywNPQz0xFZBHfPDKzh1jFH5qGD_g)](http://youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw?sub_confirmation=1)
[![Discord Tonton Jo](https://badgen.net/discord/members/2NQskxZjfp?label=Discord%20Tonton%20Jo,%20&icon=discord)](https://discord.gg/2NQskxZjfp)
### Support the channel with one of the following link:
[![Ko-Fi](https://badgen.net/badge/Buy%20me%20a%20Coffee/Link?icon=buymeacoffee)](https://ko-fi.com/tontonjo)
[![Infomaniak](https://badgen.net/badge/Infomaniak/Affiliated%20link?icon=K)](https://www.infomaniak.com/goto/fr/home?utm_term=6151f412daf35)
[![Express VPN](https://badgen.net/badge/Express%20VPN/Affiliated%20link?icon=K)](https://www.xvuslink.com/?a_fid=TontonJo)  

# GENEARL USAGE
Install borg Backup for your distribution

- Instructions can be found in [commands.md](https://github.com/Tontonjo/borg_backup/blob/main/commands.txt)

Initialize your backup target

- borg init -e authenticated /path/to/backup
- borg init -e authenticated ssh://borg@10.0.0.171:2222/path/to/backup

Backup the passphase and datastore key as suggested

Copy the borg_backup.sh script on your server

Edit BORG_REPO to aim at your local or remote datastore

Edit BORG_PASSPHRASE to the one you choose when you inited the repository

Edit /folder1 /folder2/data to the folders you want to backup

Edit --exclude as needed

Edit Retention policy

Run script with "bash borg_backup.sh" Use a cronjob to run it on a daily basis

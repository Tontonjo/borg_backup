# borg_backup

## Tonton Jo - 2021

If you find this usefull, please consider supporting my work:  
- Join me on my [Youtube Channel](http://youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw?sub_confirmation=1)  
- <a href="https://www.buymeacoffee.com/tontonjo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png"></a> <a href="https://www.infomaniak.com/goto/fr/home?utm_term=6151f412daf35"><img src="https://i.ibb.co/KjWSd95/banner-bleu.png"></a> </a> <a href="https://www.xvinlink.com/?a_fid=TontonJo"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/79/ExpressVPN-logo.svg/261px-ExpressVPN-logo.svg.png"></a>  


# GENEARL USAGE
Install borg Backup for your distribution

- Instructions can be found in [commands.txt](https://github.com/Tontonjo/borg_backup/blob/main/commands.txt)

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

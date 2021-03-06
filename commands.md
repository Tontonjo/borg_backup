# General usage commands :-)

##Install borg
```ssh
apt-get install borgbackup
```
## Initiate repository
### local:  
```ssh
borg init -e authenticated /path/to/repository  
```
### remote:  
```ssh
borg init -e authenticated ssh://username@ip_hostname:2222/path/to_repository
```

## Export keys: 
```ssh
borg key export ssh://username@ip_hostname:2222/path/to_repository /root/borg-key
```

## Mount backups:
```ssh
borg mount /path/to/repository /path/to/mountpoint
```

# Docker borg Server:

Source: https://hub.docker.com/r/mannp/docker-borgserver

- create a folder that will host your keys:

mkdir -p /path/to/borg/sshkeys/clients

- Ensure correct rights on folder:

chown 1000:1000 /path/to/borg/sshkeys

- Copy your PUBLIC key to the remote server on a new folder - name this new folder as the repository name you want to use:

- copy content of "/root/.ssh/id_rsa.pub"

nano /path/to/borg/sshkeys/clients/remote-backup

- Paste content - save - exit

- Start your borg backup server container:

docker run -td --name borg-server --restart unless-stopped -p 2222:22 --volume /path/to/borg/sshkeys:/sshkeys --volume /path/to/borg/backup:/backup/ nold360/borgserver:latest


# Passwordless SSH:

https://raw.githubusercontent.com/Tontonjo/debian/master/passwordless_ssh.txt

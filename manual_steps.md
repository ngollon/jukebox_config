# Start:

## Operating System
- Install Raspbian
- Clone ansible files to /home/pi/jukebox_config
- Update system

      apt-get update && apt-get upgrade

- Configure Raspberry PI (raspi-config)
-- WLAN
-- Force Audio out
      
## Ansible

- Install ansible

      apt-get install ansible

- Create user "ansible".

      groupadd sudo
      useradd -m -G sudo ansible

- Make ansible files readable by ansible user.

      chown -R root:ansible /etc/system

- Set password
- Create vault_pass file

# Run ./ansible-run main.yml

# After Installation

 - Set up music library
 - Disable root login in `/etc/sshd_config`: `PermitRootLogin no`
 - Configure fritz.box to resolve juke.box

# Spotify Auth?

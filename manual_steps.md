# Start:

## Operating System
- Install Raspbian
- Install git

      sudo apt install git

- Clone ansible files to /home/pi/jukebox_config
- Update system

      sudo apt update && apt upgrade

- Configure Raspberry PI (raspi-config)
-- WLAN
-- Force Audio out
-- Enable I2C and Serial
- Install mitogen

      wget https://networkgenomics.com/try/mitogen-0.2.9.tar.gz 
      sudo tar -xvf mitogen-0.2.9.tar.gz /usr/share/mitogen/mitogen-0.2.9/
      
## Ansible

- Install ansible

      apt-get install ansible

- Set password
- Create vault_pass file

# Run ./ansible-run main.yml

# After Installation

 - Set up music library
 - Disable root login in `/etc/sshd_config`: `PermitRootLogin no`
 - Configure fritz.box to resolve juke.box

# Spotify Auth?

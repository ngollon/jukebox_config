# Start:

## Operating System
- Install Raspbian
- Place empty `ssh` and wpa-supplicant.conf in boot partition

       # wpa_supplicant.conf
       country=DE
       ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
       update_config=1
       network={
             ssid="..."
             psk="..."
             key_mgmt=WPA-PSK
       }

- Install git

      sudo apt install git

- Clone ansible files to /home/pi/jukebox_config
- Update system

      sudo apt update && apt upgrade

- Configure Raspberry PI (raspi-config)
-- WLAN
-- Force Audio out
-- Enable I2C and Serial
-- Disable Bluetooth
      
## Ansible

- Install ansible

      apt-get install ansible

- Install mitogen

      wget https://networkgenomics.com/try/mitogen-0.2.9.tar.gz 
      sudo tar -xvf mitogen-0.2.9.tar.gz /usr/share/mitogen/mitogen-0.2.9/

- Set password
- Create vault_pass file

# Mopidy

- Add Spotify Auth information to vault

# Run ./ansible-run main.yml

# After Installation

 - Set up music library
 - Disable root login in `/etc/sshd_config`: `PermitRootLogin no`
 - Configure fritz.box to resolve juke.box



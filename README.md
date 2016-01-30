# alligator-manager
Alligator GPIO utility for RaspberryPi

# Install alligator-manager
- Connect to RaspberryPi via SSH client
- Download and install alligator-manager script
```
# cd /etc/init.d
# wget https://raw.githubusercontent.com/3Dartists/alligator-manager/master/alligator-manager
# chmod +x /etc/init.d/alligator-manager
```
- Init alligator-manager at boot
```
# update-rc.d alligator-manager defaults
```

# Install Bossa dependency for firmware update
This step is not necessary if using RepetierServer, the bossac program is already included.
```
# apt-get install bossa-cli
```

- Reboot the RaspberryPi

# Use the alligator-manager

## Reset the Alligator board via RaspberryPi :

```
# /etc/init.d/alligator-manager --reset
```
or 
```
# /etc/init.d/alligator-manager --emergency-stop
```

## Erase Alligator board firmware via RaspberryPi
Attention this command will delete the alligator board firmware, use only for firmware update!
```
# /etc/init.d/alligator-manager --erase
```

# Update Alligator board Firmware via Raspberry Pi
This command is very useful, allowing you to upload a .bin firmware on Alligator via RaspberryPi
```
# /etc/init.d/alligator-manager --fw-upload firmware_name.bin
```
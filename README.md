# bluetooth-connection-via-terminal

To connect bluetooth manually through the terminal, use the below mentioned commands:
```
hcitool scan  # to get the MAC address of your device
bluetoothctl
agent on
scan on  # wait for your device's address to show up here
scan off
trust MAC_ADDRESS
pair MAC_ADDRRESS
connect MAC_ADDRESS
```

Sometimes, in order to identify the MAC_Address of the bluetooth device, it won't show the name of the device, just the address. Thus, I used bluez-tools.  

`sudo apt-get install bluez-tools`  
After this run `bt-device -l`, you will now see the device name along with mac_address.

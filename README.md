# raspberry-pi

## Getting WiFi network details
To scan for WiFi networks, use the command 
`sudo iwlist wlan0 scan`

If there is too much information, use grep to find the fields you need. For example to see just the ESSIDs, use:
```
sudo iwlist wlan0 scan | grep ESSID
```

## Adding the network details to the Raspberry Pi

Open the wpa-supplicant configuration file in vi:

sudo vi /etc/wpa_supplicant/wpa_supplicant.conf

Go to the bottom of the file and add the following:
```
network={
    ssid="testing"
    psk="testingPassword"
}
```

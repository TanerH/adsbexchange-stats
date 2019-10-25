# adsbexchange-stats
ADSBexchange.com Statistics Beta

Looks for dump1090-fa and dump1090-mutability in default directories

Stats only.  Be sure to install ADSBexchange.com feeder package first.

    sudo apt-get install git
    git clone https://github.com/adsbxchange/adsb-exchange.git
    cd adsb-exchange
    chmod +x setup.sh
    sudo ./setup.sh

THEN

    git clone https://github.com/adsbxchange/adsbexchange-stats.git
    cd adsbexchange-stats
    chmod +x install.sh
    sudo ./install.sh
    
**After completing the setup do not delete this repository.**

### Systemd Status
sudo systemctl status adsbexchange-stats


### Restart
sudo systemctl restart adsbexchange-stats

## Palworld template

This template uses steam (command line) as an anonymous user to download and update the dedicated server.
The template is written so all server variables are editable through the PufferPanel dashboard, then written to the config file immediately before server startup.
Template written by Spusuf.
Config file is current as of 4th Feburary 2025.

## Requirements
Requires a workaround to get the latest DepotDownloader. See issue #310.
```
curl  https://github.com/SteamRE/DepotDownloader/releases/download/DepotDownloader_2.7.4/DepotDownloader-linux-x64.zip -L -o /tmp/dd.zip
unzip /tmp/dd.zip -d /tmp/dd
rm /var/lib/pufferpanel/binaries/depotdownloader/DepotDownloader
mv /tmp/dd/DepotDownloader /var/lib/pufferpanel/binaries/depotdownloader/DepotDownloader
chown pufferpanel:pufferpanel /var/lib/pufferpanel/binaries/depotdownloader/DepotDownloader 
rm -r /tmp/dd.zip /tmp/dd
```


## Notes
This was tested on Debian 12, but should work on all Linux systems

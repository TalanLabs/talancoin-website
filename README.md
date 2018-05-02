# TalanCoin Official Website
This project aims to provide the official website for TalanCoin project.
Its purpose is external communication.

Staging URL (auto-deploy on push on `master` branch) = http://talancoin.talanlabs.net/talancoin-website-external  
Production URL (deploy on 192.168.24.26 server) = https://www.talancoin.com

## How to use
1. Open `index.html` in a browser.
2. Enjoy.

## Staging release
1. Merge on `master` branch
2. Auto-deploy by Gitlab CI
3. Check on [http://talancoin.talanlabs.net/talancoin-website-external](http://talancoin.talanlabs.net/talancoin-website-external)

## Production release
1. Copy project files on 192.168.24.26 (static server) : `scp -r -P 22 path/to/talancoin-website/* user@192.168.24.26:/home/user`
2. Move files on server : `rm -Rf /var/www/tcwww/public_html/* && rsync -a /home/user/* /var/www/tcwww/public_html && rm -Rf /home/user/*`
3. Check on [https://www.talancoin.com](https://www.talancoin.com)
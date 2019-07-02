# SSL Guide

## Creating the certificates
1. Download [certbot](https://certbot.eff.org/) onto a linux machine 
1. Run `sudo certbot certonly --manual -d mywebsite.co.uk -d www.mywebsite.co.uk`, replacing the `-d ...` with each domain you want to update. We recommend doing this from a terminal that allows copying and pasting output (like hyper.js), because you'll need to copy some of the output data into the web servers' source
1. Follow the steps in the terminal to copy the data to your live site
1. Please note that when you're adding them to your live site, they must be in UTF-8 encoding (not UTF-8 with BOM), and with no trailing newline
1. Take a note of the output paths for the certs - you'll need this in the next step

## Converting the certificates from \*.pem to \*.pvk
> #### Windows Subsystem for Linux only
> You'll need to copy the generated certs out of the `/archive` (NOTE: `/archive`, NOT `/live`) folder that they were generated in as the terminal does not have permission by default. 
> 1. Where the WSL files are stored on Windows is unique to each windows update, and linux distro. Start [here](https://superuser.com/questions/1067373/where-is-the-linux-subsystems-filesystem-located-in-windows-10) for a guide to finding yours
> 1. Copy the contents to a folder that you can access easily like your documents. Make sure to copy `archive`, and not `live`
> 1. In your WSL, then head to the location you created. You can access your Windows file system via `/mnt` from WSL

1. Navigate to `/etc/letsencrypt/archive/website.co.uk` (or, if you're using WSL, navigate to wherever you copied the certs to)
1. Run `openssl pkcs12 -inkey ./privkey.pem -in ./cert.pem -export -out ./cert.pfx`
1. Enter a randomly generated password when it prompts for a password. Store this password temporarily - you'll need it shortly

## Uploading to Azure
1. Head to the Azure Portal, and go to the app service you want to update
1. Head to SSL Settings, and then the Private Certificates tab
1. Upload the generated \*.pfx file to Azure via the Azure Portal (SSL Settings). Enter the password you generated earlier when prompted
1. Switch back to the Bindings tab, and Add SSL Binding to your new certificate
1. Delete the old certificate

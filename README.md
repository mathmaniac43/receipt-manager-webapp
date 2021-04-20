# Receipt Manager Webapp

### Docker Install guide:
1. Install receipt parser server: [Install guide](https://receipt-parser-server.readthedocs.io/en/master/installation.html# "Install guide")
2. Pull Image `docker pull dielee/receipt-manager-webapp:latest`
3. Start Container `docker run -d --network host --name "receipt-manager-webapp" -e backendIP="backendIP" -e backendPort="backendPort" -e backendLanguage="de-DE" -e parserIP="parserIP" -e parserPort="8721" -e parserToken="parserToken" -e sqlServerIP="sqlServerIP" -e sqlDatabase="reciptData" -e sqlUsername="sqlUsername" -e sqlPassword="sqlPassword" dielee/receipt-manager-webapp:latest`

### Manual Install guide:
1. Install receipt parser server: [Install guide](https://receipt-parser-server.readthedocs.io/en/master/installation.html# "Install guide")
2. Download latest release from releases page: [Link](https://github.com/ReceiptManager/receipt-manager-webapp/releases "Link")
3. Unzip release and fill in settings into config.yml
4. <ins>Only Linux</ins> - Install unixODBC `sudo apt-get install unixodbc-dev`
5. Install python dependencies with `pip install -r requirements.txt`
6. Go into /src and run `python3 __init__.py` or on windows `python .\__init__.py`
7. Webapplication is now available at your IP and port defined in config.yml.
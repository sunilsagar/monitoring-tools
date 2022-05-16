# Steps to setup monitoring tools on Apple M1 Chipset
1. Download file from [URL](https://drive.google.com/uc?export=download&id=1ppFG-MGSLH_y9tH_wXrmiGFbC6vABD1_) .
2. Copy Downloaded tar file monitoring-lab22.tar.gz to "Documents" folder.
3. Untar Downloaded file. It may take 5 min to uncompress files. "tar -xvzf monitoring-lab22.tar.gz"
4. All activity will be performed on terminal , 3 terminals will be required.
** **
6. Start Telegraf
    * Open Terminal and run below commands
    ``` 
        cd "/Users/$(whoami)/Documents/monitoring-lab22/telegraf"
        ./telegraf --config telegraf.conf 
    ```
    * Access URL : http://localhost:9273/metrics

** **   

7. Start Prometheus
    * Open new Terminal and run below commands
    ```
        cd "/Users/$(whoami)/Documents/monitoring-lab22/prometheus"
        ./prometheus --config.file=prometheus.yml
    ```
    * Access URL : http://localhost:9090/

** **

8. Start Grafana
    * Open new Terminal and run below commands
    ```
        cd cd "/Users/$(whoami)/Documents/monitoring-lab22/grafana/bin"
        ./grafana-server start
    ```
    * Access URL http://localhost:3000
    * Default Credentials
        * Username : admin
        * Password : admin

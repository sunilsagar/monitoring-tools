# Steps to setup monitoring tools on Windows
1. Download file from [URL](https://drive.google.com/uc?export=download&id=170_OzTn4j7QtuPH54nALacDeux75c_uA) .
2. Copy Downloaded zip file monitoring-lab22.zip to "Documents" folder.
3. Unzip Downloaded file. It may take 5 min to uncompress files.
4. To open powershell, type powershell in shearch.
** **
5. Start Telegraf
    * Open Powershell and run below commands
    ``` 
        cd Documents\monitoring-lab22\telegraf
        .\telegraf --config telegraf.conf 
    ```
    * Access URL : http://localhost:9273/metrics

** **   

6. Start Prometheus
    * Open new Powershell and run below commands
    ```
        cd Documents\monitoring-lab22\prometheus
        .\prometheus.exe --config.file=prometheus.yml
    ```
    * Access URL : http://localhost:9090/

** **

7. Start Grafana
    * Open new Powershell and run below commands
    ```
        cd Documents\monitoring-lab22\grafana
        .\bin\grafana-server.exe start
    ```
    * Access URL http://localhost:3000
    * Default Credentials
        * Username : admin
        * Password : admin


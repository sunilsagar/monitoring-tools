# Steps to setup monitoring tools on Windows
1. Download file from [URL](https://drive.google.com/uc?export=download&id=170_OzTn4j7QtuPH54nALacDeux75c_uA) .
2. Go to "Documents".
3. Create Folder "monitoring".
4. Copy Downloaded zip file to monitoring folder.
5. Unzip Downloaded file. It may take 5 min to uncompress files.
** **
6. Start Telegraf
    * Open Powershell and run below commands
    ``` 
        cd Documents\monitoring\telegraf
        \telegraf --config telegraf.conf 
    ```
    * Access URL : http://localhost:9273/metrics

** **   

7. Start Prometheus
    * Open new Powershell and run below commands
    ```
        cd Documents\monitoring\prometheus
        .\prometheus.exe --config.file=prometheus.yml
    ```
    * Access URL : http://localhost:9090/

** **

8. Start Grafana
    * Open new Powershell and run below commands
    ```
        cd Documents\monitoring\grafana
        .\bin\grafana-server.exe start
    ```
    * Access URL http://localhost:3000
    * Default Credentials
        * Username : admin
        * Password : admin


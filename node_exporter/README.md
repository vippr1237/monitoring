## Install Step

```
sudo mkdir /opt/node_exporter && cd /opt/node_exporter/
sudo chmod 777 /opt/node_exporter
wget https://github.com/prometheus/node_exporter/releases/download/v1.7.0/node_exporter-1.7.0.linux-amd64.tar.gz
tar -xvf node_exporter-1.7.0.linux-amd64.tar.gz
cd node_exporter-1.7.0.linux-amd64/
chmod a+x node_exporter
```

### Create service for node exporter
```
sudo vi /etc/systemd/system/node_exporter.service
# Input the content of the file node_exporter.service
sudo systemctl daemon-reload
sudo systemctl enable node_exporter
sudo systemctl start node_exporter
systemctl status node_exporter
```
### Update prometheus to read node exporter metrics
Modify prometheus.yml in `monitor_server`
## Install step

### Install promtail
```
sudo apt install unzip
sudo mkdir /opt/promtail && cd /opt/promtail
sudo chmod 777 /opt/promtail -R
curl -O  -L https://github.com/grafana/loki/releases/download/v2.8.9/promtail-linux-amd64.zip
unzip promtail-linux-amd64.zip
chmod a+x "promtail-linux-amd64"
```
### Create service for promtail
```
vi ec2-promtail.yaml
# Input the content of ec2-promtail.yaml file
vi /etc/systemd/system/promtail.service
# Input the content of the promtail.serice file
sudo systemctl daemon-reload
sudo systemctl enable promtail.service
sudo systemctl start promtail.service
systemctl status promtail
```

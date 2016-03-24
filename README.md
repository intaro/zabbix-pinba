# zabbix-pinba

50x HTTP codes monitoring from Pinba in Zabbix.

## Installation

1) Install the scripts

```
cd /tmp
git clone https://github.com/intaro/zabbix-pinba
sudo cp zabbix-pinba/* /etc/zabbix/scripts/
sudo chmod +x /etc/zabbix/scripts/pinba
```

2) Edit config (database connection and hosts list)

```
cp /etc/zabbix/scripts/pinba.conf.php.dist /etc/zabbix/scripts/pinba.conf.php
nano /etc/zabbix/scripts/pinba.conf.php
```

3) Install template in Zabbix

Install `/tmp/zabbix-pinba/pinba-template.xml` in Zabbix. In template you can configure the border `$PINBA_ERRORS_MAX` for trigger errors count.

# DS4700_zabbix_monitoring
Monitor Storage IBM DS4700 with Zabbix Server 3.2

## Prerequisites
* Install SMCLI on Ubunt 16.04 (64bit)

Use the steps of this post.
https://wiki.geant.org/display/~federated-user-3/Installing+SMcli+on+Ubuntu+12.04

#### Aditional info to above link:

Use this apt-get instead of post:
```
apt-get install libxi6 libxtst6 alien default-jre default-jdk
```
Use below SMCLI (64bit) download instead of above post.
http://delivery04.dhe.ibm.com/sar/CMA/SDA/04671/1/SM10.86_Linux_64bit_x86-64_SMIA-10.86.x5.43.tgz

Create below link required by installer
```
ln -s /lib/x86_64-linux-gnu/libc.so.6 /lib/libc.so.6
```
Ignore the post from this point. 
* "Edit the check_IBM_DS_health script so that it uses the right command:"

You can test using command below
 
/opt/IBM_DS/client/SMcli <IP_CONTROLLER_A> <IP_CONTROLLER_B> -c "show storageSubsystem healthStatus;"

```
/opt/IBM_DS/client/SMcli 192.168.217.24 192.168.217.25 -c "show storageSubsystem healthStatus;"
Performing syntax check...
Syntax check complete.
Executing script...
Storage Subsystem health status = optimal.
Script execution complete.
SMcli completed successfully.
```

License
-------

This template were distributed under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

### Copyright

  Copyright (c) Levi Pereira

### Authors

  Levi Pereira
  (levi |dot| pereira |at| gmail |dot| com)







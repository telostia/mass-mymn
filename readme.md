## Blademaster mymn example

**Install & configure 10 MYMN masternodes using ipv6:**

```
bash ./install.sh -p mymn -n 6 -c 10 
```
**Install Bootstrap:**

```
bash ./mymn-bootstrap.sh
```
When asked for number of masternodes, enter 10 for e.g . It will download and extract bootstrap to each data folder. If you made mistakes here, you have to wipe all mn and start over again. (refer to Wipe all masternodes data below if need be)

**Handy masternode genkey script:**

```
bash ./mymn-genkey.sh
```
When asked for number of masternodes, enter 10 for e.g and followed by each genkey and press Enter key one after another til finnish all 10.

**Final command (symbolic link lost somehow during the bootstrapping and genkey):**
```
bash ./install.sh -p mymn -n 6 -c 10 
```

**Run nodes:**
```
activate_masternodes_mymn
```
this command will load all masternodes set. 

To check/stop/fix each node service do
systemctl status mymn_n5 where 16 equals the one editing(mn5) or systemctl status mymn_n2(mn2).

commands: systemctl status mymn_n<number>
                    stop   mymn_n<number>
                    start  mymn_n<number>

                    <number> = the masternode number for e.g master 2 would be: 2
sample command for stopping mn2:                     
    ```
    systemctl stop mymn_n2
    ```
sample command for starting mn3:
    ```
    systemctl start mymn_n3
    ```
sample command for checking mn3:
    ```
    systemctl status mymn_n3
    ```

**Wipe all MYMN masternode data:**

```
bash ./install.sh -p mymn -w
```

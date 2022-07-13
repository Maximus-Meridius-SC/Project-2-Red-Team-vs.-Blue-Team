## Cheat Sheet

### Host Discovery

**ARP Scan**
```bash
$ netdiscover -r 192.168.0.1/24
```

**Ping Sweep**

```bash
$ nmap -pn 192.168.0.1/24
```

**SYN Scan with OS Detection**

```bash
$ nmap -Ss -A 192.168.0.1/24
```

### Brute Force Attacks

```bash
$ hydra -l $USERNAME -P /path/to/wordlist -s $TARGET_PORT -f -vV $TARGET_URL

# For example
$ hydra -l admin -P /usr/opt/wordlist.txt -s 80 -f -vV victim.com/vulnerable_folder
```

### Gunzip

```bash
# gunzip help menu
$ gunzip --help 

# example usage
$ gunzip zipfile.txt.gz
```

### Using Kibana Overview 

### Kibana Metrics and Logs Orientation

Locate the two screens inside Kibana that you will use to visualize this traffic:
- Metrics
- Logs

  ![](../13-Elk-Stack-Project/Images/metrics-kibana/Metrics-Logs.png)

These pages will show you the changes in data that we will create.

**Logs:**

Click on logs to view some general system logs coming from the web machines.

![](../13-Elk-Stack-Project/Images/metrics-kibana/Logs-General.png)

Notice that you can Stream logs live from the machines. 

![](../13-Elk-Stack-Project/Images/metrics-kibana/Stream-Live.png)

**Metrics:**

Next, click on **Metrics** on the left side. 

- Here we can see all machines that are sending back metrics.

- The large squares represent the VMs. Click on one square. 

- Choose **View metrics** from the dropdown that appears.

  ![](../13-Elk-Stack-Project/Images/metrics-kibana/Metric-VM-Dropdown.png)

- Notice that you can see CPU and Memory usage here.

  ![](../13-Elk-Stack-Project/Images/metrics-kibana/Host-Overview.png)

### Going Further

#### Custom Dashboards

Kibana can very effectively utilize dashboards. The only caveat is that you have to create your own.

  - A great free tutorial for creating a Kabana dashboard can be found [here](https://www.tutorialspoint.com/kibana/kibana_create_dashboard.htm).

  - The official Elastic tutorial for creating a dashboard is [here](https://www.elastic.co/guide/en/kibana/current/dashboard-create-new-dashboard.html).

#### Searching in Kibana

Kibana also allows you to search logs and data directly.

- A few great resources for creating search queries can be found [here](https://deep-log-inspection.readthedocs.io/en/latest/user/kibana-logs/) and [HERE](https://www.elastic.co/guide/en/kibana/current/search.html).

---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

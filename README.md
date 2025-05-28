# ops345-assignment1
Load Balanced Apache Web Server Deployment (OPS345)

This assignment demonstrates building a load-balanced Apache web server setup using multiple EC2 instances, iptables for NAT-based traffic distribution, and automation via `cron` and `rsync`.

## Technologies Used
- Amazon EC2 / AMI / EBS
- Apache Web Server
- iptables
- rsync
- cron
- Python
- SSH key-based authentication

## Screenshot Explanations

### `asg1-ss01-amis.png`
**AWS AMI**  
Created a reusable AMI (`www-for-asg1-p1`) from the master server, used to deploy identical slave servers.

### `asg1-ss02-ebs.png`
**Elastic Block Store Volumes**  
Attached EBS volumes for each slave instance to store web content persistently.

### `asg1-ss03-routersg.png`
**Security Group Config**  
Configured custom SSH port forwarding (2221, 2224, 2223) for each slave VM via the router.

### `asg1-ss04-iptables.png`
**iptables NAT Rules**  
Used iptables with probability matching to balance traffic randomly between web servers.

### `asg1-ss05-sshkeys.png`
**SSH Key Authentication**  
Verified passwordless SSH from slave to master using a private key for seamless `rsync`.

### `asg1-ss06-files.png`
**rsync Testing**  
Tested bidirectional file syncing between master and slave servers using rsync commands.

### `asg1-ss07-crontab.png`
**cron Jobs**  
Configured cron jobs to automate rsync every 5 minutes on slave servers.

### `asg1-ss08-firefox.png`
**Browser Load Balancer Test**  
Verified randomized traffic routing by observing different server IPs in page output.

### `asg1-ss09-script.png`
**Python Script Output**  
Used a custom script to confirm distribution of requests among servers.

---

## Project Files

All screenshots and the documentation for this assignment are included in this repo.  
You can view them [here](./).

---

## Author
**Harnoor Kaur**  
Computer Systems Technician Student  
Seneca Polytechnic college 

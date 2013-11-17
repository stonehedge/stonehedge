Stonehedge
==========

A fortified warehouse-scale computing platform created at [Wrale](https://www.linkedin.com/in/jmdots) for AWS EC2 multi-zone VPCs.

- **Version**: 0.1.0
- **Status**: Early development (unstable)
- **License**: Apache Software License, Version 2.0

Features
--------

- CFNdsl
- Chef
- Chronos
- ElasticSearch
- Exhibitor
- FreeIPA
- Graphiti
- GlusterFS + HDFS connector
- Kibana
- Jenkins
- Logstash
- Lumberjack
- Marathon
- Mesos
- OpsWorks
- Packer
- PeerVPN
- Sensu
- Smartstack Nerve
- Smartstack Synapse
- Ubuntu
- Zookeeper


Components
----------

### Integrated AWS Services

  - CloudFormation
  - EBS
  - EC2
  - ELB
  - IAM
  - Route53
  - S3
  - SES
  - SNS
  - VPC


### Instances

#### Privacy Level: All

  - **All Instances: Baseline**
    - Configuration management (chef-client)
    - Encrypted backups (duplicity + rdiff-backup + duply)
    - Local email relay (postfix-server)
    - GNU/Linux operating system (ubuntu-12.04.latest.x86_64 + 3.8 kernel)
    - Logs transport (lumberjack-client)
    - Monitor and metrics agent (sensu-client)
    - Rootkit scanner (rootkit-hunter)
    - Secure transport (openssh-server)
    - Service discovery (smartstack-synapse + haproxy)
    - Service registration (smartstack-nerve)
    - Software-based RAID10-backed "/vault" encrypted file system (mdadm + cryptsetup + ext4)
    - Stateful packet inspection firewall (netfilter + iptables + ufw + fail2ban)
    - Time synchronization (ntp-client)

#### Privacy Level: Public

  - **Anchor Instances: Infrastructure**
    - Caching proxy for external APIs and distro package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay-to-external server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor and alert server (sensu-server)
    - Monitor dashboard (sensu-admin)
    - Security sentinel (nmap)
  - **Bastion Instances: Administrative Access Point**
    - Secure landing strip for interactive login (openssh-server)

#### Privacy Level: Private

  - **Barrow Instances: Logs & Metrics**
    - Logs dashboard (kibana)
    - Logs storage (elasticsearch-server)
    - Logs transport (logstash-server)
    - Metrics dashboard (graphiti)
    - Metrics storage (graphite)
  - **Lintel Instances: Compute**
    - Cluster execution engine (mesos-slave)
    - Mesh VPN cluster fabric (peervpn)
    - Distributed file system client (glusterfs-client + glusterfs-hadoop)
    - Distributed file system server (glusterfs-server)
  - **Trilithon Instances: Manager**
    - Cluster manager (mesos-master)
    - Distributed configuration service (zookeeper)
    - Distributed configuration service supervisor (exhibitor)
    - Framework for long running services (marathon-server)


### Cookbooks
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

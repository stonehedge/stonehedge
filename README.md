Stonehedge
==========

A fortified warehouse-scale computing platform developed at [Wrale](https://www.linkedin.com/in/jmdots) for AWS EC2 VPCs.

Components
----------

### Instances

#### Privacy Level: All

  - **All Instances: Baseline**
    - Configuration management (chef-client)
    - Encrypted backups (duplicity + rdiff-backup + duply)
    - Local email relay (postfix-server)
    - GNU/Linux operating system (ubuntu-12.04.latest.x86_64)
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


Cookbooks
---------
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

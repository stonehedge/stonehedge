Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------

#### Privacy Level: All

  - **All Instances**
    - Configuration management (chef-client)
    - Encrypted backups (duplicity + rdiff-backup + duply)
    - Local email relay (postfix-server)
    - GNU/Linux operating system (ubuntu-12.04.latest.x86_64)
    - Logs transport (lumberjack-client)
    - Monitor and metrics agent (sensu-client)
    - Rootkit scanner (rootkit-hunter)
    - Secure transport (openssh-server)
    - Software RAID (mdadm + msdos-mbr)
    - Stateful packet inspection firewall (netfilter + iptables + ufw)
    - Time synchronization (ntp-client)

#### Privacy Level: Public

  - **Anchor Instances**
    - Caching proxy for AWS APIs and distro package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay-to-external server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor and alert server (sensu-server)
    - Monitor dashboard (sensu-admin)
    - Security sentinel (nmap)
  - **Bastion Instances**
    - Secure landing strip for interactive login (openssh-server)

#### Privacy Level: Private

  - **Barrow Instances**
    - Logs dashboard (kibana)
    - Logs storage (elasticsearch-server)
    - Logs transport (logstash-server)
    - Metrics dashboard (graphiti)
    - Metrics storage (graphite)
  - **Lintel Instances**
    - Distributed configuration service (zookeeper)
    - Distributed configuration service supervisor (exhibitor)
    - Cluster manager (mesos-master)
    - Framework for long running services (marathon-server)
    - Mesh VPN cluster fabric (peervpn)
    - Distributed file system (glusterfs-server)
  - **Trilithon Instances**

Cookbooks
---------
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

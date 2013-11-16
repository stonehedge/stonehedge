Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------


#### Privacy Level: Public

  - **Anchor Instances**
    - Caching proxy for AWS APIs and distro package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor and alert server (sensu-server)
    - Monitor dashboard (sensu-admin)
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

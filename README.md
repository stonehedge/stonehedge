Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------


#### Privacy Level: Public

  - Instance Group: **Bastion**
    - Secure landing strip for interactive login (openssh-server)
  - Instance Group: **Anchor**
    - Caching proxy for AWS APIs and distro package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor and alert server (sensu-server)
    - Monitor dashboard (sensu-admin)

#### Privacy Level: Private

  - Instance Group: **Barrow**
    - Logs dashboard (kibana)
    - Logs storage (elasticsearch-server)
    - Logs transport (logstash-server)
    - Metrics dashboard (graphiti)
    - Metrics storage (graphite)
  - Instance Group: **Lintel**
    - Distributed configuration service (zookeeper)
    - Distributed configuration service supervisor (exhibitor)
    - Cluster manager (mesos-master)
    - Framework for long running services (marathon-server)
    - Mesh VPN cluster fabric (peervpn)
    - Distributed file system (glusterfs-server)
  - Instance Group: **Trilithon**

Cookbooks
---------
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

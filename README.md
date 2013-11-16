Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------

### Instance Groups

#### Public Privacy Level

  - Bastion
    - Secure landing strip for interactive login (openssh-server)
  - Anchor
    - Caching proxy for AWS APIs and Ubuntu package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor and alert server (sensu-server)
    - Monitor dashboard (sensu-admin)

#### Private Privacy Level

  - Barrow
    - Logs dashboard (kibana)
    - Logs storage (elasticsearch-server)
    - Logs transport (logstash-server)
    - Metrics dashboard (graphiti)
    - Metrics storage (graphite)
  - Lintel
  - 
  - Trilithon

### Cookbooks
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

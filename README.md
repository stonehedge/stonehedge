Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------



### Instance Tiers

#### Public Privacy Level

  - Bastion
    - Secure landing strip for interactive login (openssh-server)
  - Anchor
    - Caching proxy for AWS APIs and Ubuntu package downloads (squid-proxy)
    - Continuous integration engine (jenkins)
    - Email relay server (postfix-server)
    - Identity, DNS and time server (freeipa-server)
    - Monitor server (sensu-server)
    - Monitor dashboard (sensu-admin)

#### Private Privacy Level

  - Barrow
  - Lintel
  - Trilithon

### Cookbooks
  - stonehedge-anchor
  - stonehedge-barrow
  - stonehedge-base
  - stonehedge-bastion
  - stonehedge-lintel
  - stonehedge-trilithon

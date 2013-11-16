Stonehedge
==========

A fortified and elastic warehouse-scale computing platform for AWS EC2 VPCs.


Components
----------



### Instance Tiers

#### Public Privacy Level

  - Anchor
    - Functions
      - Caching proxy for AWS APIs and Ubuntu package downloads (squid-proxy)
      - Monitor server (sensu-server)
      - Monitor dashboard (sensu-admin)
      - Email relay server (postfix-server)
      - Continuous integration engine (jenkins)
      - Identity, DNS and time server (freeipa-server)
  - Bastion
    - Functions
      - Secure landing strip for interactive login (openssh-server)

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

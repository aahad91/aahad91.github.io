---
layout: project
type: project
image: images/backflip.png
title: BAcKFLiP
permalink: projects/backflip
# All dates must be YYYY-MM-DD format!
date: 2020-03-30
labels:
  - VNFs
  - SFC
  - Proxy Servers
  - Load Balancers
  - Telecommunications
  - Docker
  - OpenStack
  - OSM
  - Benchmarking
  - Python
  - Shell
  - Prediction Analysis
  - GitHub
summary: Benchmarking network functions to collect the world's largest NFV performance dataset.
---

<img class="ui medium right floated rounded image" src="../images/backflip.png">

In the next generation of networks (you may know it as “5G”) many network components will be moved to the cloud to improve the flexibility and manageability of our networks. In this scenario, called network function virtualisation (NFV), virtualised network functions (VNFs), like firewalls or intrusion detection systems, which are installed in virtual machines or containers [Docker](https://www.docker.com) and can be deployed on-demand on cloud infrastructures, such as [OpenStack](https://www.openstack.org) or [Kubernets](https://kubernetes.io). These VNFs can then be connected (chained) to form more complex network services. This simplifies the development of novel network services, because deployments can be fully automated and be done in minutes instead of days, as required by legacy, hardware-based network functions.

To deploy such VNFs and services, it has to be decided how many resources, like vCPU cores or memory, have to be assigned to the VNFs to meet the expected performance goals. Those resource dimensioning decisions can, for example, be based on so-called VNF performance profiles (VNF-PP) [1], [2]. VNF-PPs can be generated by (offline) profiling/benchmarking procedures [1]. They describe the relationship between assigned resources and various performance metrics achieved by single VNFs or chained services. These VNF-PPs can then serve (i) as inputs to orchestration systems (e.g., [OpenSource MANO](https://osm.etsi.org/)), (ii) utilised by placement and scaling optimisation algorithms [3], or (iii) be used for further (offline) data analyses, e.g., to find performance issues.

However, the availability of such VNF-PP datasets is still limited to few examples. Because of this, the research community is seeking for more public datasets, based on real-world measurements, to serve as the basis for further research and the development of new tools that make use of VNF-PPs.

The goal of this project group is to collect those datasets for a diverse collection of different VNFs and network services. To perform and automate this collection process, existing measurement tools, like the [5GTANGO NFV benchmarking tool](https://github.com/sonata-nfv/tng-sdk-benchmark), will be used and extended within this project. Finally, the collected datasets need to be polished and analysed before they are made available for the research community, i.e., through one or more scientific publications.

### Milestones / Goals

* Identify and analyse candidate VNFs and network service projects to be benchmarked (e.g. [Open5GCore](https://www.open5gcore.org/), [OpenIMS](https://www.openimscore.com/), [Docker](https://www.docker.com/), etc.)
* Setup a benchmarking testbed and integrate it with existing NFV benchmarking solutions
* Design and run a first set of benchmarking experiments using the existing toolchain
* Integrate VNFs and network services to be executed and tested on the benchmarking testbed
* Extend and improve the [5GTANGO benchmarking tool](https://github.com/sonata-nfv/tng-sdk-benchmark) to be able work with one of the most prominent NFV MANO solutions in the telecom industry: [OpenSource MANO](https://osm.etsi.org/)
* Run a second set of benchmarking experiments using your extended toolchain
* Document all experiment setups and outcomes
* Analyse the outcomes and polish the data for publication

Source: <a href="https://cn-upb.github.io/pg-backflip-cat/"><i class="large github icon"></i>CN-UPB/pg-backflip-cat</a>

### References

* [1] M. Peuster and H. Karl: [Profile Your Chains, Not Functions: Automated Network Service Profiling in DevOps Environments](http://ieeexplore.ieee.org/document/8169826/). IEEE Conference on Network Function Virtualization and Software Defined Networks (NFV-SDN), Berlin, Germany. (2017)
* [2] R. Rosa, C. Rothenberg, M. Peuster, H.Karl:  [Methodology for VNF Benchmarking Automation. IETF draft BMWG (ongoing work)](https://datatracker.ietf.org/doc/draft-rosa-bmwg-vnfbench/) (2018)
* [3] S. Dräxler, S. Schneider, and H. Karl: [Scaling and Placing Bidirectional Services with Stateful Virtual and Physical Network Functions](https://ieeexplore.ieee.org/document/8459915/). In 2018 IEEE Conference on Network Softwarization (NetSoft)

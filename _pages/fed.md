---
layout: archive
title: "Resource Aware Anonymous Clustering/Tiering in Federated learning"
permalink: /research_publications/fed
author_profile: true
---


### Problem
Device Heterogeneity in federated learning causes the straggler problem, where the low resource device slows down the entire distributed training process. The works that tackle this problem require collecting or inferring the devices' computational capabilities by the server. However, client devices' configuration or resource information is a sensitive information. Leaking that information could expose the client device to DoS attacks or other resource exhaustion attacks. So, we need to plan a secure aggregation based clustered federated learning framework where the device information is not communicated to or cannot be inferred by the server.

### Solution Idea
We propose to fill this gap by designing an Anonymous Tier-Based Federated Learning framework. The elements of our framework include,

- **Broadcast of Model and Tier Schedules**: The server begins each training round by announcing tier-specific training schedules that will be used for that round. This announcement includes a set of deadlines or time windows for reporting updates for each cluster.
- **Client Tier Self-Assessment**: Each client evaluates its own training speed and resource capacity without revealing this to the server and assigns itself to a tier.
- **Tier Based Group Authentication**: The participating clients will have a tier membership certificate once they assign themselves to a tier, which will be used for secure aggregation.
- **Local Training Phase**: Each client trains as many epochs as it can within an the tier alloted time deadline.
- **Anonymous Update Submission with Secure Aggregation**: The server maintains aggregation buffer for each tier and then after the tier deadline for updates, tier based secure aggregation is done.  


### Threat Models
We have identified three additional threat models that we want to tackle ,
- **Curious but honest client and server** - This is the standard threat considered for most federated learning security based scenarios.
- **Misassigning Client**: A client may deliberately misalign itself to the wrong tier/cluster to slow down training.   
- **Sybil Attacks**: Typical sybil attacks are identified based on client model update similarity from multiple clients but in our framework, individual model updates are not known, therefore the typical identification won't work. We are working on how to combat this threat.
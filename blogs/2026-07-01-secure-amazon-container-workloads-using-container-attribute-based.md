---
title: "Secure Amazon container workloads using container attribute-based rules in AWS Network Firewall"
url: "https://aws.amazon.com/blogs/security/secure-amazon-container-workloads-using-container-attribute-based-rules-in-aws-network-firewall/"
date: "2026-07-01"
author: "Amit Gaur"
feed_url: "https://aws.amazon.com/blogs/security/feed/"
---
AWS Network Firewall now supports container attribute-based rules for protecting traffic in Amazon EKS and ECS clusters. Instead of relying on ephemeral IP addresses, organizations can define firewall rules using Kubernetes attributes like namespaces, pod names, cluster names, and labels, with the feature automatically discovering and tracking matching pods in near real-time. The post walks through creating container associations and Suricata-compatible rules, with testing examples for allowed and blocked traffic.

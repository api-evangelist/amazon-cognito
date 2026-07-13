---
title: "How to use the AWS Workload Credentials Provider for cross-account secret retrieval and prefetching secrets"
url: "https://aws.amazon.com/blogs/security/how-to-use-the-aws-workload-credentials-provider-for-cross-account-secret-retrieval-and-prefetching-secrets/"
date: "2026-07-01"
author: "Derik Wang"
feed_url: "https://aws.amazon.com/blogs/security/feed/"
---
This guide covers two new features of the AWS Workload Credentials Provider: role chaining for cross-account secret retrieval and secret prefetching to reduce cold-start latency. Role chaining lets a single provider instance access secrets across AWS accounts through IAM role assumption, while prefetching populates an in-memory cache at startup. The post includes prerequisites, configuration steps, and examples of explicit secret specification and tag-based discovery.

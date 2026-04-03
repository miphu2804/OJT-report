---
title : "Apply Infrastructure & Collect Outputs"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 4.5.3.6 </b> "
---

#### Goal

Apply infrastructure from .tf files and publish outputs for downstream jobs.

#### Key steps

1. terraform apply with auto-approve.
2. Read outputs and write them to $GITHUB_OUTPUT.

---
title : "Fork & Clone Repo"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 4.3. </b> "
---

#### Repository

Repo: https://github.com/AWS-FCJ-Project/EduTrust_origin.git

#### Fork and clone

1. Open the repo on GitHub and click **Fork**.
2. Clone your fork:
```
git clone https://github.com/<your-username>/EduTrust_origin.git
```
3. Move into the project folder:
```
cd EduTrust_origin
```

#### Create a working branch

```
git checkout -b feature/<branch-name>
```

#### Sync with main

```
git fetch origin
git rebase origin/main
```

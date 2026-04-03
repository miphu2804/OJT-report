---
title : "Cleanup"
date : 2024-01-01
weight : 8
chapter : false
pre : " <b> 4.8. </b> "
---
#### Cleanup with terraform destroy

1. Run from the Terraform directory or through CI/CD.
2. Execute:
```
terraform destroy
```
3. Confirm the action when prompted.

#### Manual cleanup

1. **ACM certificates**: remove unused certificates.
2. **CloudFront/Amplify**: delete distributions or apps if still present.
3. **Logs/Snapshots**: delete unused log groups and snapshots.

#### Verify deletion

1. Ensure Terraform state has no remaining resources.
2. Check AWS Console for any billable leftovers.

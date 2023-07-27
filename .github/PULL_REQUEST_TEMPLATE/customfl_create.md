## Custom FL Creation Pull Request

---
### Instructions (tick box as the step is performed)
1. [ ] Submit manifest in this Custom FL Creation pull request
2. [ ] Accomplish all items in the Manifest Checklist below
3. [ ] Reviewer will check PR and add comment "LGTM"
4. [ ] From this PR branch, install in target cluster
5. [ ] Accomplish the Deployment Checklist below
6. [ ] Reviewer will approve this pull request and merge to master
7. [ ] Re-sync `~/environment/devops-manifest` in the Cloud9
---

### Relevant Links
1. Custom FL Creation Request issue: <!-- indicate here -->
2. Custom FL Test Plan / Report issue: <!-- indicate here -->

### Manifest Checklist
<!-- Suggestion: Use ~~strikethrough~~ for entries that do not apply, instead of removing the entry -->
1. Requirement completeness
   - [ ] All items in Custom FL Creation Request issue are addressed
2. Testing completeness
   - [ ] All tests in Custom FL Test Plan / Report issue are completed
3. Manifest files
   - [ ] Files are separated per resource type (e.g., 1-accounts, 2-archive, etc.)
   - [ ] Folder structure is respected (CustomFLs/active/clusterName/customFLName)
4. Manifest completeness
   - [ ] Accounts
     - [ ] Accounts are assigned for all validators
     - [ ] Endowed accounts are created according to Custom FL Creation Request issue
   - [ ] Validator
     - [ ] Image = 
     - [ ] Accounts used are in the accounts manifest file
     - [ ] Nodeselector, pod affinity and antiaffinity are all specified
     - [ ] Liveness and readiness probes are specified
     - [ ] Resource limits and requests are specified
     - [ ] `persistence.deleteOnFinalizing=false`
     - [ ] alt-producer parameters are all checked
   - [ ] Archive
     - [ ] Image = 
     - [ ] AccountSet is separate
     - [ ] Bootnodes section matches Validator
     - [ ] Nodeselector, pod affinity and antiaffinity are all specified
     - [ ] Liveness and readiness probes are specified
     - [ ] Resource limits and requests are specified
     - [ ] `persistence.deleteOnFinalizing=false`
     - [ ] Ingress host follows the requested URL for both RPC and WS
     - [ ] alt-producer parameters are all checked
   - [ ] Dedicated archive for Blockscout
     - [ ] Image and all settings match Archive
     - [ ] AccountSet is separate
     - [ ] Manifest file is separate
   - [ ] Blockscout
     - [ ] Image = 
     - [ ] Image used is customized for token symbol and testnet name
     - [ ] Nodeselector is specified for both main and postgresql
     - [ ] Affinity will schedule both main and postgresql together
     - [ ] Resource limits and requests are specified
     - [ ] Ingress host follows the requested URL
     - [ ] Archive service accessed is the dedicated one for blockscout
     - [ ] Readers enabled
       - [ ] Replica count = 
       - [ ] `DISABLE_WEBAPP=false` and `DISABLE_INDEXER=true`
     - [ ] Main pod has `DISABLE_WEBAPP=true` if readers are enabled

### Deployment Checklist
<!-- Suggestion: Use ~~strikethrough~~ for entries that do not apply, instead of removing the entry -->
1. Deployment overview
   - [ ] AWS Account = 
   - [ ] EKS Cluster = 
   - [ ] Volume autoscaling is enabled in cluster
   - [ ] Load balancer autoscaling is enabled in cluster
   - [ ] Node autoscaling is enabled for all nodegroups used
2. Deployment details
   - [ ] Double-check all alt-producer parameters for validators and archives
   - [ ] Pod scheduling is OK for everyone
   - [ ] No other unexpected pods are sharing the nodes
   - [ ] All URLs are reachable
   - [ ] Blockscout is showing new blocks in real time
3. Testing
   - [ ] Follow and update the Custom FL Test Plan / Report issue
   - [ ] Add comment "testing done" plus a link to any related comment in the test issue
4. Others
   - [ ] Secrets are shared in 1Pass: <!-- Add the vault and note location here -->
   - [ ] <!-- Add your own here as needed -->

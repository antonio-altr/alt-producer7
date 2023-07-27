## Custom FL Test Plan / Report

---
### Instructions
1. List down the required tests in the issue description
2. Add a new comment for every update on the test results
   - All retests should also be in separate comments
3. Maintain this issue together with the custom FL creation request issue
---

### Relevant Links
1. Custom FL Creation Request issue: <!-- indicate here -->
2. Custom FL Creation pull request: <!-- indicate here -->

### Test Plan
<!-- Change the sample contents below as needed -->
1. Stress test
   - Type: ERC20 airdrop
   - Scale: m=10 n=10 pods=100
   - Check CPU/mem usage
2. Archive scale-in / scale-up
   - Check no unexpected pod restarts
   - Check syncing pods are not servicing requests

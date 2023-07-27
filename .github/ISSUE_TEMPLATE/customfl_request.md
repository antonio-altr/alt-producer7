## Custom FL Creation Request

---
### Instructions (tick box as the step is performed)
1. [ ] Submit this Custom FL Creation Request issue
2. [ ] DevOps team will create
   - [ ] Custom FL Test Plan / Report issue
   - [ ] Custom FL Creation pull request
3. [ ] Close the issue **after** the custom FL is terminated
---

### Relevant Links
1. Custom FL Test Plan / Report issue: <!-- DevOps team will indicate here -->
2. Custom FL Creation pull request: <!-- DevOps team will indicate here -->

### Background
<!--
Example:
1. DF Ares needs a FL for their event from 1-5 June 2023
2. They will also conduct pre-event testing from 1-5 May 2023
3. Expected player count is 1,000
-->

### Chain Spec / Main Requirements
1. ChainID: <!-- indicate here or say "let DevOps team assign" -->
2. Token
   - Symbol: <!-- indicate here -->
   - Decimals: 18
3. FCFS: <!-- Yes or No -->
4. Block time: 2s
5. No gas fees: <!-- Yes or No -->
6. Endowed accounts
   - Account #1 = <!-- amount in wei -->
   - Account #2 = <!-- amount in wei -->
   - <!-- Add more accounts as needed -->
7. Validator count: 1
8. Other chain settings
   - <!-- Add more settings as needed -->
9. Blockscout
   - Need blockscout? <!-- Yes or No -->
   - Custom token symbol: <!-- indicate here -->
   - Custom network name: <!-- indicate here -->
10. URLs
   - RPC: https://myfl.alt.technology
   - WS: wss://myfl.alt.technology
   - Blockscout: https://myfl-explorer.alt.technology
   - Grafana: <!-- DevOps team will indicate here -->

### Other Custom Requirements
<!--
Example:
1. We expect very high volume in first few minutes for this NFT mint. Please make sure ingress and archives can handle the traffic.
2. Target users are in Asia. Please set up the nodes in JP region.
-->

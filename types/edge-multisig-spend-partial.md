# `edge-multisig-spend-partial`

**Phase:** spend  
**Direction:** A cosigner who added their signature

```json
{
  "type": "edge-multisig-spend-partial",
  "version": 1,
  "spendId": "spend-1",
  "walletProposalId": "18f3c2a1b4e90c7d",
  "npub": "npub1b…",
  "psbtBase64": "cHNidP8…",
  "signers": [
    { "npub": "npub1a…", "status": "signed" },
    { "npub": "npub1b…", "status": "signed" },
    { "npub": "npub1c…", "status": "pending" }
  ]
}
```

# `edge-multisig-spend-complete`

**Phase:** spend  
**Direction:** After broadcast (`txid` is Bitcoin)

```json
{
  "type": "edge-multisig-spend-complete",
  "version": 1,
  "spendId": "spend-1",
  "walletProposalId": "18f3c2a1b4e90c7d",
  "txid": "abc…",
  "psbtBase64": "cHNidP8…",
  "signers": [
    { "npub": "npub1a…", "status": "signed" },
    { "npub": "npub1b…", "status": "signed" },
    { "npub": "npub1c…", "status": "pending" }
  ]
}
```

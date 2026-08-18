# `edge-multisig-spend-request`

**Phase:** spend  
**Direction:** Spend initiator → other cosigners

```json
{
  "type": "edge-multisig-spend-request",
  "version": 1,
  "spendId": "spend-1",
  "walletProposalId": "18f3c2a1b4e90c7d",
  "requiredSignatures": 2,
  "totalCosigners": 3,
  "psbtBase64": "cHNidP8…",
  "amountNative": "10000",
  "destAddress": "bc1q…",
  "feeNative": "500",
  "initiatorNpub": "npub1…",
  "signers": [
    { "npub": "npub1a…", "status": "signed" },
    { "npub": "npub1b…", "status": "pending" },
    { "npub": "npub1c…", "status": "pending" }
  ]
}
```

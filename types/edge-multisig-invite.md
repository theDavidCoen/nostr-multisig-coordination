# `edge-multisig-invite`

**Phase:** wallet creation  
**Direction:** Initiator → each invitee (encrypted separately)

```json
{
  "type": "edge-multisig-invite",
  "version": 1,
  "proposalId": "18f3c2a1b4e90c7d",
  "walletName": "Family 2-of-3",
  "requiredSignatures": 2,
  "totalCosigners": 3,
  "initiatorNpub": "npub1…",
  "initiatorXpub": "xpub6…",
  "cosignerNpubs": [
    "npub1invitee-a…",
    "npub1invitee-b…"
  ]
}
```

`cosignerNpubs` is the other signers (not including the initiator). `totalCosigners` = initiator + `cosignerNpubs.length`.

# `edge-multisig-complete`

**Phase:** wallet creation  
**Direction:** Initiator → all other npubs once every slot has an xpub

```json
{
  "type": "edge-multisig-complete",
  "version": 1,
  "proposalId": "18f3c2a1b4e90c7d",
  "cosigners": [
    {
      "npub": "npub1initiator…",
      "xpub": "xpub6…",
      "status": "local",
      "parentFingerprint": "aabbccdd"
    },
    {
      "npub": "npub1invitee-a…",
      "xpub": "xpub6…",
      "status": "accepted",
      "parentFingerprint": "11223344"
    },
    {
      "npub": "npub1invitee-b…",
      "xpub": "xpub6…",
      "status": "accepted",
      "parentFingerprint": "55667788"
    }
  ]
}
```

Clients independently derive `wsh(sortedmulti(m, [fp/48'/0'/0'/2']xpub/<0;1>/*, …))` (BIP-380, BIP-67). They MUST NOT trust a P2WSH address shipped in the complete message as the sole source of truth (Edge currently omits the address from this JSON and derives it).

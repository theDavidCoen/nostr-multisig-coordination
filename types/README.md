# Message types

Application JSON in this folder is the **rumor `content`** (kind **14**). `version` is `1` for every message here.

Each file is one wire `type` string. Add a new type by copying an existing file, giving it a unique `type` (`edge-multisig-<name>`), and linking it in the tables below.

Shared identifiers (`proposalId`, `spendId`, xpubs) are defined in the [root README](../README.md#identifiers).

## Wallet creation

| `type` | Direction | Spec |
|--------|-----------|------|
| `edge-multisig-invite` | Initiator → each invitee | [edge-multisig-invite.md](./edge-multisig-invite.md) |
| `edge-multisig-accept` | Invitee → initiator and the other npubs | [edge-multisig-accept.md](./edge-multisig-accept.md) |
| `edge-multisig-complete` | Initiator → all other npubs | [edge-multisig-complete.md](./edge-multisig-complete.md) |

## Spend

Same transport. PSBT is base64 in JSON (still inside NIP-44). Relays do not see the unsigned tx.

Clients MUST re-verify the PSBT against the known descriptor (amount, destination, change, prevouts) before signing. Status arrays in JSON are hints; the PSBT signatures are authoritative.

| `type` | Direction | Spec |
|--------|-----------|------|
| `edge-multisig-spend-request` | Spend initiator → other cosigners | [edge-multisig-spend-request.md](./edge-multisig-spend-request.md) |
| `edge-multisig-spend-partial` | Cosigner who added a signature | [edge-multisig-spend-partial.md](./edge-multisig-spend-partial.md) |
| `edge-multisig-spend-reject` | Cosigner who refuses the spend | [edge-multisig-spend-reject.md](./edge-multisig-spend-reject.md) |
| `edge-multisig-spend-complete` | After broadcast | [edge-multisig-spend-complete.md](./edge-multisig-spend-complete.md) |

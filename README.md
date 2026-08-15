# TwinVault Omega Core v2 — Advanced Threat Primitives

10 next-generation security modules that go beyond standard security. Designed for journalists, executives, military, activists, and classified programs worldwide.

## Modules

1. **Post-Quantum Migration Layer** (pqMigration.js) — hybrid classical + lattice encryption, auto-rotation
2. **Honeytoken Canary Engine** (honeytoken.js) — decoy credentials that detect exfiltration with attribution
3. **Deniable Vault Layering** (stegoVault.js) — nested hidden volumes, plausible deniability under legal compulsion
4. **Air-Gapped Key Ceremony** (keyCeremony.js) — offline key generation via QR exchange + camera entropy
5. **Zero-Knowledge Breach Oracle** (zkBreachOracle.js) — exposure prediction without revealing credentials (k-anonymity)
6. **Oblivious Access Obfuscation** (obliviousAccess.js) — PIR-lite, server cannot determine which record you access
7. **Cross-Domain Key Sharding** (crossDomain.js) — shares across device, HSM, cloud, trustee, blockchain
8. **Compulsion-Resistant Auth** (compulsionAuth.js) — fails under duress even with correct credentials
9. **Proof-of-Life Chain** (proofOfLife.js) — tamper-evident voluntariness attestation, auto-notify trustees
10. **AI Extraction Boundary** (aiBoundary.js) — sandboxed inference, canary tokens, prompt-injection defense

## Usage

Each module is zero-dependency, Web Crypto API only.

```js
import { generateHybridKey, hybridEncrypt } from "./src/pqMigration.js";
const key = await generateHybridKey();
const env = await hybridEncrypt(secretData, key);
```

## License

MIT

# TwinVault Omega Core v2

10 next-generation security modules for the most sensitive environments — journalists, executives, military, activists, and classified programs.

## Modules

1. **Post-Quantum Migration Layer** (pqMigration.js) — hybrid classical + lattice encryption with auto-rotation
2. **Honeytoken Canary Engine** (honeytoken.js) — decoy credentials that detect exfiltration with attacker attribution
3. **Deniable Vault Layering** (stegoVault.js) — nested hidden volumes with plausible deniability under legal compulsion
4. **Air-Gapped Key Ceremony** (keyCeremony.js) — offline key generation via QR exchange + camera entropy + signed transcript
5. **Zero-Knowledge Breach Oracle** (zkBreachOracle.js) — exposure prediction using k-anonymity, credentials never leave device
6. **Oblivious Access Obfuscation** (obliviousAccess.js) — PIR-lite, server cannot determine which record you access
7. **Cross-Domain Key Sharding** (crossDomain.js) — shares across device, HSM, cloud, trustee, blockchain time-lock
8. **Compulsion-Resistant Auth** (compulsionAuth.js) — fails under duress even with correct credentials via cognitive + timing analysis
9. **Proof-of-Life Chain** (proofOfLife.js) — tamper-evident voluntariness attestation, auto-notify trustees on break
10. **AI Extraction Boundary** (aiBoundary.js) — sandboxed inference with canary tokens and prompt-injection defense

## Usage

Each module is zero-dependency, Web Crypto API only.

```js
import { generateHybridKey, hybridEncrypt } from "./src/pqMigration.js";
const key = await generateHybridKey();
const env = await hybridEncrypt(secretData, key);
```

```js
import { generateHoneytokens, checkActivation } from "./src/honeytoken.js";
const tokens = generateHoneytokens(realIdentity, 3);
const alert = checkActivation(tokens[0].id, { ip: "..." });
```

```js
import { createLayeredVault, openLayer } from "./src/stegoVault.js";
const vault = await createLayeredVault([
  { id: "outer", password: pwd1, data: decoyData },
  { id: "hidden", password: pwd2, data: realData }
]);
```

## License

MIT

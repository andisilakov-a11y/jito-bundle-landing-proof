# Jito Bundle Landing Proof — last 30 days

  Independent re-verification of every Solana bundle our system submitted via authenticated Jito gRPC `sendBundle` over the last 30 days.

  ## Files

  - **`jito_proof_full.md`** — full report (bundle-level + transaction-level success rates, lifecycle, samples, per-launch breakdown, every signature listed).
  - **`jito_landing_proof_classified.csv`** — every on-chain signature (7,401) with origin classification (`OURS` vs `OUTSIDE`) and the actual fee-payer pulled from `getTransaction`.

  ## Headline numbers (user-owned txns only)

  | Metric | Value |
  |---|---:|
  | Mints | 100 |
  | User-owned on-chain transactions | **6,833** |
  | Confirmed OK | 6,765 |
  | Application-level revert | 68 |
  | **Transaction-level success rate** | **99.00 %** |
  | Launch-bundle landing rate | 100 / 100 (100 %) |
  | Initial-buy landing rate | 100 / 100 (100 %) |
  | Follow-up bundle landing (excl. operator-aborted) | 98.5 % |

  ## Verification

  Anyone can independently verify any signature with:
  ```bash
  curl https://api.mainnet-beta.solana.com -H 'content-type: application/json' \
    -d '{"jsonrpc":"2.0","id":1,"method":"getTransaction",
         "params":["<SIGNATURE>",{"maxSupportedTransactionVersion":0}]}'
  ```
  
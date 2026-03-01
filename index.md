# Privacy Policy — MetalPulse

**Last updated: 2026-03-01**

MetalPulse ("the app", "we") is an independent app for Metal Blockchain node operators.
This Privacy Policy explains what data the app accesses, how it is stored, and what your rights are.

---

## 1. What Data We Collect — And What We Don't

### Data stored locally on your device

MetalPulse stores the following data **exclusively on your device**, encrypted using iOS
Keychain or Android EncryptedSharedPreferences:

| Data | Purpose |
|---|---|
| Validator Node ID (NodeID-…) | Identify which validators you monitor |
| Node nickname | Your personal label for a node |
| VPS/RPC URL (optional) | Direct connection to your own validator node |
| Notification preferences | Whether and when to alert you |
| Uptime snapshots | Power the 24-hour uptime chart (AsyncStorage) |
| Local validation history | Track completed validation periods |

### Data explicitly NOT collected

- ❌ No user accounts or registration
- ❌ No email addresses, phone numbers, or real names
- ❌ No device identifiers (IDFA, GAID, fingerprints)
- ❌ No location data
- ❌ No analytics or telemetry sent to our servers
- ❌ No crash reports sent to third parties
- ❌ No advertising

---

## 2. How Data Is Stored

All app data is stored **locally on your device**:

- **Node configurations, validation history, alert rules**: iOS Keychain / Android
  EncryptedSharedPreferences via `expo-secure-store`. Protected by device PIN/biometrics.
  HMAC integrity checks detect tampering.
- **Uptime chart data**: Plain on-device storage (`AsyncStorage`). This data contains only
  numeric uptime percentages and timestamps — no identifiers or personal data.
- **In-memory only**: Validator data fetched from the blockchain is held in RAM (React Query
  cache) and discarded when the app is closed. Nothing is written to disk beyond what is
  listed above.

**We have no server.** We cannot access, see, or retrieve any data from your device.

---

## 3. Data Shared With Third Parties

The app makes network requests to the following public blockchain APIs:

| Endpoint | Data sent | Purpose |
|---|---|---|
| `api.metalblockchain.org` | Validator NodeID (public blockchain identifier) | Fetch validator status, uptime, stake data |
| `explorerapi.metalblockchain.org` | NodeID, reward-owner P-Chain address (public on-chain data) | Fetch historical validation periods |

**Both endpoints receive only public blockchain identifiers**, not personal data. These are
equivalent to looking up a public record.

Your VPS/RPC URL (if configured) is sent **directly from your device to your own server
only** — never to us or any third party.

---

## 4. Local Notifications

If you grant notification permission, MetalPulse schedules **local notifications** on your
device for:

- Node offline / back online
- Low uptime warnings
- Validator expiry reminders (30, 14, 7, 1 day)
- Delegator changes
- Low peer count

These notifications are generated and delivered entirely **on-device**. No notification
content is transmitted to any server. No push notification token is created or stored.

You can revoke notification permission at any time in your device's system settings.

---

## 5. Your Rights (GDPR / DSGVO)

If you are in the European Union, you have the following rights:

- **Right to access**: All data is stored on your device — you can view it directly in the app.
- **Right to erasure**: Removing a node ("Remove Node" button) permanently deletes all
  associated data: node config, uptime history, validation history, and notification schedules.
  Uninstalling the app removes all remaining data.
- **Right to portability**: All data is stored in standard JSON format on your device.
- **Right to object**: You can disable notifications at any time without affecting core
  app functionality.

Since we operate no server and collect no personal data, there is no "data subject request"
process — you have full control through the app itself and device settings.

---

## 6. Data Retention

Data persists until you remove the node or uninstall the app:

- Node config + validation history: Deleted when you tap "Remove Node"
- Uptime snapshots: Capped at 1,440 entries (24 hours); older entries are automatically
  overwritten. Also deleted on "Remove Node".
- Notification schedules: Cancelled on "Remove Node".

---

## 7. No Financial Advice

MetalPulse displays publicly available data from the Metal Blockchain network (uptime,
stake amounts, delegation capacity, reward status). This information is provided for
**informational purposes only**.

Nothing in MetalPulse constitutes financial advice, investment advice, or a recommendation
to stake, delegate, or interact with any validator or blockchain protocol. Past reward
history and current uptime metrics do not guarantee future rewards.

Staking and delegating digital assets involves risk, including the risk of reward
forfeiture if a validator fails to meet uptime requirements. Always do your own research
and consult a qualified financial advisor before making financial decisions.

---

## 8. Children's Privacy

MetalPulse is intended for blockchain node operators. We do not knowingly collect any
information from children under 13 (or the applicable age in your jurisdiction).

---

## 9. Changes to This Policy

We will post any updates to this policy at https://metalpulse-app.github.io/metalpulse-legal with an updated
"Last updated" date. Continued use of the app after changes constitutes acceptance.

---

## 10. Contact

Questions about this privacy policy:

**MetalPulse**
Email: blockade.kanaele-5h@icloud.com
Privacy Policy: https://metalpulse-app.github.io/metalpulse-legal

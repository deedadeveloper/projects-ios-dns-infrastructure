# iOS Encrypted DNS Infrastructure Pipeline

An isolated, zero-overhead configuration profile repository deployed via Cloudflare Pages to enforce high-performance network filtering natively on iOS.

## 🛠️ System Architecture
* **Target OS Stack:** iOS CoreTelephony & Network Extensions
* **Hosting Interface:** Cloudflare Pages Anycast Edge (MIME-mapped via `_headers`)
* **Upstream Resolver Engine:** AdGuard Secure (DoH over TLS/SSL termination)
* **Operational Overhead:** \$0.00/mo (Infinite static egress scaling)

## 🛡️ Active Security Policies
* **In-App Mobile Ads:** Drops requests to known mobile ad telemetry nets (AdMob, AppLovin, Unity Ads).
* **Malware Mitigations:** Structural intercept of malicious phishing, tracker, and crypto-mining endpoints.
* **Zero Telemetry Tracking:** No local query logging or structural tracking dashboards maintained.

## 📲 Client Deployment Guide
1. Launch **Safari** on the target iOS device.
2. Navigate directly to your deployed Cloudflare endpoint: `https://<your-project>.pages.dev/dns-setup.mobileconfig`
3. Tap **Allow** when the system prompt requests profile download authorization.
4. Navigate to **Settings** -> **Profile Downloaded** on the iPhone.
5. Review the cryptographic signature parameters and tap **Install** (authenticate via device passcode).
6. Verify persistent initialization by checking **Settings** -> **General** -> **VPN & Device Management** -> **DNS**.

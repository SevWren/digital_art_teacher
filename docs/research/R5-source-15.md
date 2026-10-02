# Source: https://www.illustrationage.com/
# Original target: https://www.illustrationage.com/
# Method: 2/6 (Wayback CDX API + curl Wayback) — BLOCKED BY ANTI-BOT
# Retrieved: 2026-10-02
---
RETRIEVAL PARTIAL — BLOCKED

The Illustration Age website (https://www.illustrationage.com/) uses JavaScript-based bot detection (Cloudflare or similar) that returns "Checking your browser... Javascript required" when accessed via curl/wget/python.

Wayback Machine CDX API returned an available snapshot:
URL: http://web.archive.org/web/20260930013951/https://illustrationage.com/
Timestamp: 20260930013951

However, fetching that Wayback URL also returned the bot-block message:
"Your request is being blocked because our system has flagged it as suspected abusive bot traffic that is degrading the performance of the Wayback Machine."

Raw responses:
Method 3 (direct curl): "Checking your browser... Javascript required"
Method 6 (Wayback): "Your request is being blocked because our system has flagged it as suspected abusive bot traffic"

Methods attempted:
- Method 1: WebFetch — internal API auth error (403)
- Method 2: Wayback CDX API — snapshot found at 20260930013951 but blocked on fetch
- Method 3: curl browser UA — JS/bot check blocks access
- Method 4: wget — same JS block
- Method 5: Python urllib — same JS block
- Method 6: Wayback timestamps — blocked by Wayback anti-bot system

No substantive content could be retrieved from this source.

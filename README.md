# varnascn-uptime — external watchdog
Hits the OCR API (https://varnascn.varnaakshara.com/health) and the frontend (https://scan.varnaakshara.com) every 5 minutes via GitHub Actions — **independent of the VPS hosting them**.

- Anything down → opens a `down`-labeled issue (auto-updated while failing, auto-closed on recovery). GitHub also emails you on failing workflow runs.
- Daily keepalive commit prevents GitHub's 60-day scheduled-workflow auto-disable.
- This repo intentionally contains **no project code and no secrets** (it's public only so Actions minutes stay free).

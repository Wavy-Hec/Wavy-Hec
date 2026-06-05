# Profile README — Setup Guide

One-time setup steps to enable the optional dynamic features in `README.md`. Each is independent.

---

## 1. 📊 Detailed metrics dashboard

The `.github/workflows/metrics.yml` workflow is already committed. It needs a token:

1. Create a **classic** Personal Access Token: <https://github.com/settings/tokens> → *Generate new token (classic)* → scopes **`repo`** and **`read:org`**.
2. Add it as a repo secret: repo **Settings → Secrets and variables → Actions → New repository secret**, name **`METRICS_TOKEN`**.
3. Run it: **Actions** tab → *Generate Metrics* → **Run workflow**. It commits `github-metrics.svg`.
4. Uncomment the embed in the `// metrics` section of `README.md`.

---

## 2. ⚡ Self-host the stats widgets (fix the flaky cards)

The public `github-readme-stats.vercel.app` instance is rate-limited (the 503s you may see). Host your own so the stats card, top-languages, and any pin-cards are reliable:

1. **Fork** <https://github.com/anuraghazra/github-readme-stats>.
2. Create a GitHub PAT (classic; add **`repo`** scope if you want private-repo counts).
3. <https://vercel.com/new> → import your fork → add env var **`PAT_1`** = the token → **Deploy**.
4. In `README.md`, replace every `github-readme-stats.vercel.app` with your instance host `https://<your-grs>.vercel.app` (the stats card and the `top-langs` card).

> The streak card (`github-readme-streak-stats`) is a separate project with its own self-host repo if you want it bulletproof too — same fork-and-deploy pattern.

---

## 3. 📝 Add repo descriptions (so links read well)

Several featured repos have empty GitHub descriptions. Set them from the repo page (**About** ⚙️) or with the `gh` CLI:

```bash
gh repo edit Wavy-Hec/VLM             -d "Vision-language models for agent instruction-following"
gh repo edit Wavy-Hec/ObjectDetection -d "Real-time YOLO object detection for robotics"
gh repo edit Wavy-Hec/Chess-AlphaGO   -d "AlphaGo-style self-play reinforcement learning agent for chess"
gh repo edit Wavy-Hec/KissICP         -d "LiDAR odometry via point-to-point ICP"
```

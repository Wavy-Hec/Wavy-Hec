# Profile README — Setup Guide

One-time setup steps to enable the optional dynamic features in `README.md`. Each is independent.

---

## 1. ⏳ WakaTime coding activity

Shows a live breakdown of what languages/editors you actually spend time in. The `.github/workflows/waka.yml` workflow + the `coding_activity` section in `README.md` are already wired up — you just connect your account.

1. Sign up (free) at <https://wakatime.com> and copy your **Secret API Key** from <https://wakatime.com/settings/account>.
2. Install the WakaTime plugin in your editor and paste the API key when prompted:
   - **VS Code:** Extensions → search "WakaTime" → install.
   - **JetBrains (PyCharm/CLion):** Settings → Plugins → "WakaTime".
3. Add the key as a repo secret: **Settings → Secrets and variables → Actions → New repository secret**, name **`WAKATIME_API_KEY`**.
4. Code for a day or two so stats accumulate, then run **Actions → Waka Readme → Run workflow**. It fills in the `// coding_activity` section automatically (and refreshes daily).

> No extra token needed — the workflow uses the built-in `GITHUB_TOKEN` to commit.

---

## 2. 📌 GitHub native "Pinned repositories"

These are the cards GitHub shows **above** your README. Make them match your featured table (this is a profile UI setting — it can't be set from code):

1. Go to your profile: <https://github.com/Wavy-Hec>.
2. In the "Popular repositories" area, click **Customize your pins**.
3. Select up to 6, e.g. **VLM**, **RL_IsaacLab**, **ObjectDetection**, **Chess-AlphaGO**, **KissICP**, **PortfolioWebsite** → **Save pins**.

---

## 3. 📊 Detailed metrics dashboard

The `.github/workflows/metrics.yml` workflow is already committed. It needs a token:

1. Create a **classic** Personal Access Token: <https://github.com/settings/tokens> → *Generate new token (classic)* → scopes **`repo`** and **`read:org`**.
2. Add it as a repo secret named **`METRICS_TOKEN`** (Settings → Secrets and variables → Actions).
3. Run it: **Actions** tab → *Generate Metrics* → **Run workflow**. It commits `github-metrics.svg`.
4. Uncomment the embed in the `// metrics` section of `README.md`.

---

## 4. ⚡ Self-host the stats widgets (fix the flaky cards)

The public `github-readme-stats.vercel.app` instance is rate-limited (the 503s you may see). Host your own so the stats card and top-languages render reliably:

1. **Fork** <https://github.com/anuraghazra/github-readme-stats>.
2. Create a GitHub PAT (classic; add **`repo`** scope if you want private-repo counts).
3. <https://vercel.com/new> → import your fork → add env var **`PAT_1`** = the token → **Deploy**.
4. In `README.md`, replace every `github-readme-stats.vercel.app` with your instance host `https://<your-grs>.vercel.app`.

> The streak card (`github-readme-streak-stats`) is a separate project with its own self-host repo if you want it bulletproof too — same fork-and-deploy pattern.

---

## 5. 📝 Add repo descriptions (so links read well)

Several featured repos have empty GitHub descriptions. Set them from the repo page (**About** ⚙️) or with the `gh` CLI:

```bash
gh repo edit Wavy-Hec/VLM             -d "Vision-language models for agent instruction-following"
gh repo edit Wavy-Hec/ObjectDetection -d "Real-time YOLO object detection for robotics"
gh repo edit Wavy-Hec/Chess-AlphaGO   -d "AlphaGo-style self-play reinforcement learning agent for chess"
gh repo edit Wavy-Hec/KissICP         -d "LiDAR odometry via point-to-point ICP"
```

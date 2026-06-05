# Profile README — Setup Guide

One-time setup steps to enable the dynamic features in `README.md`. Work through whichever you want; each is independent.

---

## 1. 🎧 Live Spotify "now playing"

Your `Wavy-Hec/SpotifyReadMe` is a fork of **[novatorem](https://github.com/novatorem/novatorem)**. It needs three secrets and a Vercel deploy. Endpoint will be `https://<your-app>.vercel.app/api/spotify`.

### a. Create a Spotify app
1. Go to <https://developer.spotify.com/dashboard> → **Create app**.
2. Copy the **Client ID** and **Client Secret**.
3. In the app's settings, add a **Redirect URI** — any valid URL works, e.g. `https://localhost/callback`. Save.

### b. Get a refresh token (one-time)
1. Open this URL in your browser (replace `CLIENT_ID` and the redirect to match step a), approve access:
   ```
   https://accounts.spotify.com/authorize?client_id=CLIENT_ID&response_type=code&redirect_uri=https://localhost/callback&scope=user-read-currently-playing%20user-read-recently-played
   ```
2. After approving you'll be redirected to `https://localhost/callback?code=XXXX`. Copy the `code` value.
3. Exchange the code for a refresh token. In **PowerShell** (fill in the three values):
   ```powershell
   $id="CLIENT_ID"; $secret="CLIENT_SECRET"; $code="THE_CODE_FROM_STEP_2"
   $auth=[Convert]::ToBase64String([Text.Encoding]::ASCII.GetBytes("$id`:$secret"))
   Invoke-RestMethod -Method Post -Uri "https://accounts.spotify.com/api/token" `
     -Headers @{ Authorization = "Basic $auth" } `
     -Body @{ grant_type="authorization_code"; code=$code; redirect_uri="https://localhost/callback" }
   ```
   Copy the `refresh_token` from the response.

### c. Deploy to Vercel
1. <https://vercel.com/new> → **Import** `Wavy-Hec/SpotifyReadMe`.
2. Add **Environment Variables**:
   | Name | Value |
   |------|-------|
   | `SPOTIFY_CLIENT_ID` | your Client ID |
   | `SPOTIFY_SECRET_ID` | your Client Secret |
   | `SPOTIFY_REFRESH_TOKEN` | the refresh token from step b |
3. **Deploy**. Visit `https://<your-app>.vercel.app/api/spotify` to confirm it renders.

### d. Enable in the README
In `README.md`, find the `// now_playing` block, replace `<your-vercel-app>` with your deployment, and uncomment the `<p>...</p>` inside the comment.

---

## 2. 📊 Detailed metrics dashboard

The `.github/workflows/metrics.yml` workflow is already committed. It needs a token:

1. Create a **classic** Personal Access Token: <https://github.com/settings/tokens> → *Generate new token (classic)* → scopes **`repo`** and **`read:org`**.
2. Add it as a repo secret: repo **Settings → Secrets and variables → Actions → New repository secret**, name **`METRICS_TOKEN`**.
3. Run it: **Actions** tab → *Generate Metrics* → **Run workflow**. It commits `github-metrics.svg`.
4. Uncomment the embed in the `// metrics` section of `README.md`.

---

## 3. ⚡ Self-host the stats widgets (fix the flaky cards)

The public `github-readme-stats.vercel.app` instance is rate-limited (the 503s you saw). Host your own so the stats card, top-languages, and pin-cards are reliable:

1. **Fork** <https://github.com/anuraghazra/github-readme-stats>.
2. Create a GitHub PAT (classic; add **`repo`** scope if you want private-repo counts).
3. <https://vercel.com/new> → import your fork → add env var **`PAT_1`** = the token → **Deploy**.
4. In `README.md`, replace every `github-readme-stats.vercel.app` with your instance host `https://<your-grs>.vercel.app` (the stats card, the `top-langs` card, and all six `api/pin/` URLs).

> The streak card (`github-readme-streak-stats`) and trophy (`github-profile-trophy`) are separate projects with their own self-host repos if you want those bulletproof too — same fork-and-deploy pattern.

---

## 4. 📝 Add repo descriptions (so pin-cards read well)

Several featured repos have empty GitHub descriptions, which makes the pin-cards look bare. Set them from the repo page (**About** ⚙️) or with the `gh` CLI:

```bash
gh repo edit Wavy-Hec/VLM            -d "Vision-language models for agent instruction-following"
gh repo edit Wavy-Hec/ObjectDetection -d "Real-time YOLO object detection for robotics"
gh repo edit Wavy-Hec/Chess-AlphaGO   -d "AlphaGo-style self-play reinforcement learning agent for chess"
gh repo edit Wavy-Hec/KissICP         -d "LiDAR odometry via point-to-point ICP"
```

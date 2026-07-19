# Sport Showdown — GitHub Pages edition

This edition is configured as a static Next.js export so GitHub Pages can host the actual app instead of displaying the README.

## Included

- Three-round debate flow
- Offline Practice mode
- Daily Debate
- Private friend-challenge links
- Back button
- History, streaks, and debate statistics
- Timer, sound, vibration, transcript sharing, and scorecard downloads
- PWA service worker

## Important limitation

GitHub Pages cannot securely run the OpenAI API because it has no server. Offline Practice works fully. Online AI works only when the site is connected to a separate backend endpoint through the `NEXT_PUBLIC_DEBATE_API_URL` repository secret.

Never place an OpenAI API key in browser code or a public GitHub repository.

## Deploy

1. Upload the contents of this folder to the root of the GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Open the **Actions** tab and wait for “Deploy Sport Showdown to GitHub Pages” to finish.
5. The workflow writes `debatesports.com` as the custom domain automatically.

For the normal GitHub project URL instead of a custom domain, remove the “Add custom domain” step from `.github/workflows/deploy-pages.yml` and configure a Next.js `basePath` matching the repository name.

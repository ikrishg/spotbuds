> [!WARNING]
> **Unmaintained.** This repository is no longer actively maintained. SpotBuds depended on the Spotify Web API; after Spotify limited indie developer access, the app only worked for a small allowlisted set of users. The author moved on to a Last.fm-based version in [tastebuds](https://github.com/ikrishg/tastebuds). This repo is kept for reference only.

<div align="center">
<div><img src="https://github.com/ikrishg/spotbuds/raw/main/assets/favicon.svg" alt="SpotBuds logo" width="96" height="96"></div>
<h1>SpotBuds</h1>
<p>One line AI-generated description of your recent music taste 💄</p>
<div><img src="https://github.com/ikrishg/spotbuds/raw/main/assets/cover.png" alt="SpotBuds cover image" width="600"></div>
</div>

## Status

SpotBuds is a static site that connected to Spotify, analyzed your listening history, and used [ai.hackclub.com](https://ai.hackclub.com) to generate a short description of your taste. It is **not maintained** and is unlikely to work for new users because of Spotify’s developer policies.

A hosted demo may still exist at [spotbuds.krishg.com](https://spotbuds.krishg.com), but expect broken or invite-only behavior.

## How this worked

1. The home page had a button to connect your Spotify account.
2. Clicking it redirected you to Spotify’s authorization page.
3. After authorization, Spotify redirected back to an auth page.
4. The auth page stored the access token in the browser’s local storage.
5. A button on the auth page led to the results page.
6. The results page fetched Spotify data using the access token.
7. The app analyzed that data and generated a witty description of your music taste.
8. It used ai.hackclub.com to generate the description.

## Running locally (historical)

1. Clone the repository: `git clone https://github.com/ikrishg/spotbuds.git`
2. Navigate to the project directory: `cd spotbuds`
3. Open `index.html` in your browser through a local server (for example `live-server` or another static server).
4. Create a Spotify app at the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications).
5. In `config.js`, add a Spotify client ID and redirect URI.

**NOTE:** The redirect URI should be your local server URL with an `/auth` path, for example `http://localhost:3000/auth`. Use the same redirect URI in the Spotify Developer Dashboard and in `config.js`.

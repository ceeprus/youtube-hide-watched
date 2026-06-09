# youtube-hide-watched

A simple userscript for toggling visibility of watched videos in YouTube, on your Subscriptions page and elsewhere on the site. Also provides toggles to hide YouTube Shorts, YouTube Mixes, and videos from channels you're already subscribed to.

# Installation

- Install [TamperMonkey](https://www.tampermonkey.net), [GreaseMonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) or [UserScripts](https://github.com/quoid/userscripts) extension for your browser
- Open [main.user.js](https://raw.githubusercontent.com/ceeprus/youtube-hide-watched/master/main.user.js) and your userscript manager will prompt you to install it
- Visit YouTube (or refresh the YouTube page if it's already open)

# How to Use

The script adds four small buttons at the top of the page, see screenshot below. Pressing the "Watched Videos" button cycles through showing watched videos normally, then dimmed, then entirely hidden. The "Shorts", "Mixes", and "Subscribed Channels" buttons do the same for Shorts, YouTube Mixes (the auto-generated "Mix" / radio playlists), and videos from channels you already follow, respectively.

You will see the buttons at the top of the page, to right of the Search box.

![screenshot](screenshot.png 'Screenshot')

The "Watched Videos" button keeps track of different areas of YouTube separately. This allows you to hide watched videos on the Subscriptions page, show watched as dimmed in the sidebar recommendations, and show watched normally on channel pages. Here are the areas that the button keeps track of separately:

- Subscriptions page
- Channel pages
- Trending page
- Recommendations sidebar when watching a video
- Playlist pages
- Everywhere else

YouTube does not keep track of which Shorts you've watched, so the "Shorts" button dims/hides all Shorts.

The "Mixes" button hides YouTube Mixes wherever they appear — your home feed, search results, and the watch-page sidebar. Like the "Watched Videos" button, it remembers its setting separately per area.

The "Subscribed Channels" button hides — or tints darker — videos on your homepage from channels you're already subscribed to, so the homepage surfaces things you don't already follow. It builds your subscription list automatically the first time you enable it and refreshes it periodically. This one only applies to the homepage.

# Settings

Click the gear button to open settings:

- **Hide/Dim Videos Above Percent** — how much of a video must be watched (per YouTube's native progress bar) before it counts as watched.
- **Subscribed Channels Tint Brightness %** — how dark the "tint" state makes subscribed-channel tiles (lower is darker).
- **Refresh Subscription List Every (hours)** — how often the auto-built subscription list is rebuilt.
- **Refresh subscription list now (on Save)** — tick this and hit Save to rebuild the list immediately (useful right after subscribing to something new).

# Works with Watchmarker for YouTube

YouTube only marks *recently* watched videos, so the "Watched Videos" button can only catch what YouTube still draws a progress bar on. If you also use **Watchmarker for YouTube** — a browser extension that tracks your full watch history and marks every video you've already seen — this script's "Watched Videos" button will hide/dim those marked videos too, giving you complete watched-history hiding.

Install Watchmarker:

- Firefox: [watchmarker-for-youtube](https://addons.mozilla.org/en-US/firefox/addon/watchmarker-for-youtube/)
- Chrome: [watchmarker-for-youtube](https://chromewebstore.google.com/detail/watchmarker-for-youtube/pfkkfbfdhomeagojoahjmkojeeepcolc)

No setup is needed beyond installing it — this script detects Watchmarker's marks automatically.

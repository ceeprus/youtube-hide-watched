# youtube-hide-watched

A simple userscript for toggling visibility of watched videos in YouTube, on your Subscriptions page and elsewhere on the site. Also provides toggles to hide YouTube Shorts and YouTube Mixes.

# Installation

- Install [TamperMonkey](https://www.tampermonkey.net), [GreaseMonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) or [UserScripts](https://github.com/quoid/userscripts) extension for your browser
- Open [main.user.js](https://raw.githubusercontent.com/ceeprus/youtube-hide-watched/master/main.user.js) and your userscript manager will prompt you to install it
- Visit YouTube (or refresh the YouTube page if it's already open)

# How to Use

The script adds three small buttons at the top of the page, see screenshot below. Pressing the "Watched Videos" button cycles through showing watched videos normally, then dimmed, then entirely hidden. The "Shorts" button does the same for Shorts, and the "Mixes" button does the same for YouTube Mixes (the auto-generated "Mix" / radio playlists).

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

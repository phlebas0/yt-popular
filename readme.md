# yt-popular

a Chrome extension that jumps from a YouTube channel page to that channel's
popular videos playlist.

YouTube builds hidden playlists for every channel by rewriting the `UC` prefix
on the channel ID. `UULP` is uploads sorted by view count, which the normal
channel interface does not offer.

## install

1. download the ZIP file and extract it
2. go to `chrome://extensions` and turn on `Developer mode`
3. click `Load unpacked` and pick the extracted folder

## use

open a channel page, then click the toolbar button or press `Alt+P`. handle,
`/channel/`, `/c/` and `/user/` URLs all work.

## notes

the channel ID is read from the URL, then from `meta[itemprop="identifier"]`,
then from the canonical link. if none of them yield an ID the extension does
nothing and logs to the page console.

not every channel has a populated `UULP` playlist. where it doesn't exist
YouTube shows an error page.

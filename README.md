# the-wayback

See the design history of any website. Type `wayback.` in front of a site's address and the Wayback Machine opens that site's archive calendar. It's a fun way to see what the internet used to look like.

```
wayback.google.com        ->  web.archive.org/web/*/google.com
wayback.github.com/about  ->  web.archive.org/web/*/github.com/about
```

Type `first.` instead to jump straight to the oldest snapshot.

```
first.google.com          ->  google.com as archived in 1998
```

## Install

1. Clone this repo.
2. Open `chrome://extensions` and turn on **Developer mode**.
3. Click **Load unpacked** and select the repo folder.

Chrome asks for access to all sites because a redirect rule needs permission for the URL it rewrites, and Chrome has no pattern for "any host that starts with `wayback.`". The extension has no scripts. It ships two redirect rules in `rules.json` and nothing else.

## No-install alternative

Add a Chrome site search shortcut instead:

1. Open `chrome://settings/searchEngines`.
2. Next to **Site search**, click **Add**.
3. Set **Shortcut** to `wayback` and **URL** to `https://web.archive.org/web/*/%s`.

Then type `wayback google.com` (with a space) in the address bar.

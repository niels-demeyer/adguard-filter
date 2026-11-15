# adguard-filter

A custom filter list for **AdGuard** and **uBlock Origin** that:

- Removes YouTube clutter: end-screen cards, annotations, branding watermarks, live chat, "Enhanced bitrate", Playables, member-only videos
- **Blocks YouTube Shorts** everywhere: home/subscriptions/search shelves, sidebar entry, channel tab, search chip, mobile bottom bar, and direct `/shorts/` links
- Blocks Facebook trackers on third-party sites
- Hides ads and annoyances on a handful of news, email, cricket and job sites

## Subscription URL

```
https://raw.githubusercontent.com/niels-demeyer/adguard-filter/main/filter.txt
```

Subscribing means your blocker picks up updates automatically (checked every few days).

## Install

### uBlock Origin

**Option A: subscribe (auto-updates)**

1. Open the uBlock Origin **Dashboard** (click the extension icon, then the gear icon).
2. Go to the **Filter lists** tab.
3. Scroll to the bottom, open **Import...**, and paste the subscription URL above.
4. Click **Apply changes**.

**Option B: one-click**

With uBlock Origin installed, click
[**Subscribe**](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Fniels-demeyer%2Fadguard-filter%2Fmain%2Ffilter.txt&title=Custom%20Filter%20List)
and confirm.

**Option C: paste manually (no auto-updates)**

1. Open the Dashboard → **My filters**.
2. Paste the contents of [`filter.txt`](filter.txt).
3. Click **Apply changes**.

### AdGuard browser extension

1. Open AdGuard **Settings** → **Filters** → **Custom**.
2. Click **Add custom filter**, paste the subscription URL, and confirm.

### AdGuard for Windows / Mac / Android / iOS

1. Go to **Settings** → **Content blocking** (or **Filters**) → **Custom filters**.
2. Tap **Add custom filter**, paste the subscription URL, and confirm.

> Note: on AdGuard for iOS, extended CSS rules (`:has()`, `:has-text()`) need **Advanced protection** enabled.

### AdGuard Home

AdGuard Home is DNS-level only and **can't** apply cosmetic rules, so most of this list (including Shorts hiding) won't work there. Use the browser extension or app instead.

## Notes

- YouTube changes its page structure from time to time. If Shorts start showing up again, open an issue or update the selectors in `filter.txt`.
- Clicking a Short from inside YouTube isn't blocked at the network level (YouTube navigates without a full page load), but Shorts links and entry points are hidden, so there's nothing to click.
- The Outlook rules use auto-generated class names and may be outdated.

## Credits

Based on the custom static filter list by Sushant Aggarwal.

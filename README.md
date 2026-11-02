# RedditClean

**Review and clean your Reddit history, with control over what stays.**

RedditClean is a **Chrome extension (beta)** for reviewing your own Reddit comments and posts. It uses your existing signed-in session on **old.reddit.com**; you do not need Reddit API credentials or a separate RedditClean login.

**Current version: v0.43 (beta).** This is pre-release software. Export a backup, start with a small selection, and verify the results before processing more content.

## What RedditClean does

- **Replace comments in bulk** with a standard Markdown message. The free version **edits comments; it does not delete them**.
- **Delete selected posts**, subject to the daily attempt allowance. Post deletion can be irreversible.
- **Preview and select** individual items before processing, including selecting all or preserving all matching items.
- **Filter** by included subreddits, preserved subreddits, free text contained in comments, and a from/to date range. Applying filters limits the preview to matching items. A **Filters applied** indicator shows the number of active filters and matching items; **Clear filters** appears when filters are active. Clearing filters does not reset individual preservation choices.
- **Export a CSV backup** of discovered items locally before making changes.
- **Manually rescan** to refresh discovered history; reopening the workspace does not intentionally start a new scan.
- **Track processing** with a progress bar, daily allowance, average seconds per edit, ETA, and last editor-open/save-verification times.
- **Pause, resume, and stop** processing. **Done** closes the full-screen workspace without stopping the job; **Stop** ends the job.
- **Follow live results:** successfully replaced comments from the current processing job appear in green at the top with a **✓ Replaced this session** label. Previously replaced items are hidden by default and can be shown with the history checkbox.

### Processing sessions and history

A **session means one processing job**, not one opening of the workspace. Pausing, resuming, or closing and reopening the workspace does not create a new job. Starting a new job creates a new session.

The preview distinguishes **Completed this session**, **Remaining selected**, and **Previously replaced**. Historical counts shown in the filtered preview can reflect the active filters and discovered items, rather than every comment ever edited on Reddit. Replacement history is stored locally in the browser and may be lost if extension storage is cleared or the extension is removed.

## Free allowance and planned Pro

| Capability | Free (current) | Pro (planned, not available) |
| --- | --- | --- |
| Successful comment replacements | **51 per UTC day** | No product-side daily allowance* |
| Post deletion attempts | **5 per UTC day** | No product-side daily allowance* |
| Preview, filters, selection, CSV backup | Included | Planned |
| Pause, resume, stop, progress metrics | Included | Planned |
| Randomise comments before deletion | Not included | Planned |
| Delete comments after replacement | Not included | Planned |
| Pricing | Free | One-time purchase planned; no price announced |

*Reddit's own rate limits and restrictions still apply. Free allowance is tracked in this browser installation, across Reddit accounts, and resets at **00:00 UTC**. Browser-local limits are not tamper-proof. Post deletion allowance counts **attempts**, not just confirmed deletions.

## Installation (unpacked extension)

1. Download the latest RedditClean ZIP and extract it.
2. Open Chrome and navigate to `chrome://extensions`.
3. Enable **Developer mode**.
4. Select **Load unpacked** and choose the extracted `redditclean-extension` directory (the folder containing `manifest.json`).
5. Pin RedditClean to the Chrome toolbar if convenient.
6. Sign in to Reddit in Chrome, then select **Replace Comments** or **Delete Posts** in the extension popup.

To update an unpacked installation, replace the extracted files and use **Reload** on the extension card. If you remove and reinstall the extension instead, **Chrome may delete its local storage**, including saved replacement history and selections. Keep the same extension installation when possible.

## Replace comments

1. Sign in to Reddit and select **Replace Comments** from the RedditClean toolbar popup.
2. Wait for the **Filters & preview** workspace to load discovered comments.
3. Optionally set subreddit, text, or date filters in the left sidebar, then click **Apply filters**. Use **Clear filters** to return to the unfiltered view.
4. Review the matching comments. Uncheck anything you want to preserve, or use **Select all** / **Preserve all** for matching items.
5. Click **Export CSV backup** if you want a local record of discovered content.
6. Select **Replace Comments**, review the confirmation, and start the job.
7. Watch green completed rows appear at the top. Use **Pause**, **Resume**, or **Stop** as needed. **Done** only closes the workspace; it does not stop a running job.

The free version replaces comment content with:

```markdown
Deleted by [RedditClean](https://github.com/DamnYouRohan/RedditClean)
```

This is an edit, **not a permanent comment deletion**. The original text may remain available through caches, archives, search engines, or third-party services.

## Delete posts

1. Select **Delete Posts** in the popup.
2. Review discovered posts and choose which ones to delete.
3. Export a backup if needed and confirm the action.
4. Monitor the result. Stop if Reddit reports an error or the outcome is uncertain.

**Deleting posts can be irreversible.** The free allowance is five deletion **attempts** per UTC day, not five guaranteed successful deletions.

## Privacy and permissions

RedditClean operates using your existing Reddit session and stores selections, job state, allowances, and replacement history locally in Chrome. CSV exports are generated locally. It does not ask for your Reddit password or require Reddit API credentials.

The extension requests `storage` and `activeTab` permissions and access to `https://old.reddit.com/*` so it can read your visible Reddit history and interact with Reddit's editing and deletion controls. Do not share exported CSV files or diagnostic screenshots if they contain sensitive information.

## Known limitations

- **Beta / live-site dependency:** Reddit interface changes, network problems, and rate limits can disrupt scanning, editing, verification, or deletion. A successful syntax check is not proof of correct live behaviour.
- **History completeness:** Reddit may not expose all historical items through profile pages. A scan is not a guarantee of complete account history.
- **Preview accuracy:** Some comment bodies may be unavailable or incorrectly extracted from Reddit's HTML. Try **Rescan** when no job is active, and confirm the content before replacing anything.
- **Local state:** Removing the extension or clearing its storage can erase saved session/history information. The daily allowance is browser-local, not an account-wide service.
- **Irreversibility:** Post deletion and overwriting comment text may be impossible to undo. CSV export provides a reference copy, not automatic restoration.
- **Pro is not implemented:** Permanent comment deletion, randomisation, and Pro licensing are future plans, not current features.

## Reporting a problem

Open an issue in the project repository and include the RedditClean version, Chrome version, steps to reproduce, expected behaviour, and actual behaviour. Remove private information from screenshots and logs. For safety, test fixes with a small selection before running larger batches.

## Project and disclaimer

Source and issue tracker: [RedditClean on GitHub](https://github.com/DamnYouRohan/RedditClean).

RedditClean is an independent project and is **not affiliated with, endorsed by, or sponsored by Reddit**. Use it only for content you are authorised to manage. Review selections carefully and use at your own risk.

---

**RedditClean. Your Reddit history, your choice.**

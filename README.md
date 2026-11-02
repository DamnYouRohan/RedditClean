# RedditClean

**Clean up your Reddit history.**

RedditClean is a Chrome extension that helps you review, edit and delete your Reddit comments and posts in bulk.

You can preview your history, filter by subreddit, text or date, and choose what to keep or remove.

RedditClean works through your existing Reddit session on old.reddit.com. No separate login or Reddit API credentials are required.

The extension is free to use, with an optional Pro version planned as a one-time purchase.

> **Current version: v0.43 (Beta)**
>
> RedditClean is under development. Please back up important content and review your selections before making changes.

## Features

- **Bulk comment replacement:** Replace multiple Reddit comments with a standard message.
- **Post deletion:** Delete selected posts from your Reddit history.
- **Preview before cleaning:** Review comments and posts before making changes.
- **Selective cleaning:** Choose which comments or posts to process or preserve.
- **Subreddit filters:** Include or exclude specific subreddits.
- **Free-text filter:** Find comments containing specific words or phrases.
- **Date filters:** Clean content from a selected date range.
- **Filter status and clearing:** See when filters are applied, how many items match, and clear active filters in one click.
- **Pause, resume and stop:** Control a processing job without losing its session progress.
- **CSV export:** Download a backup of your discovered Reddit history.
- **Live preview:** Watch newly replaced comments appear in green with a **✓ Replaced this session** indicator.
- **Processing sessions:** Track replacements made in the current job separately from historical replacements.
- **Replacement history:** Show or hide previously replaced comments in the preview.
- **Progress tracking:** See completed items, remaining allowance, average processing time and estimated time remaining.
- **Automatic pagination:** Discover multiple pages of your Reddit history.
- **Manual rescan:** Refresh discovered items when you choose, without automatically rescanning whenever the workspace reopens.
- **Compact workspace:** Review more comments at once in the full-screen Filters & Preview workspace.

## Free vs Pro

RedditClean offers a free version for occasional use. A Pro version is planned for users who want to clean larger amounts of content.

**Pro will be a one-time purchase. No subscription or recurring fees.**

| Feature | Free | Pro (planned) |
|---|---|---|
| Replace Reddit comments | 51 successful replacements per UTC day | Unlimited* |
| Delete Reddit posts | 5 attempts per UTC day | Unlimited* |
| Randomise comments before deletion | — | ✓ |
| Permanently delete comments | — | ✓ |
| Preview comments and posts | ✓ | ✓ |
| Select individual items | ✓ | ✓ |
| Filter by subreddit | ✓ | ✓ |
| Filter by date | ✓ | ✓ |
| Filter by comment text | ✓ | ✓ |
| Exclude specific subreddits | ✓ | ✓ |
| Pause, resume and stop | ✓ | ✓ |
| Export history to CSV | ✓ | ✓ |
| Live preview and session tracking | ✓ | ✓ |
| Progress and timing metrics | ✓ | ✓ |
| Automatic pagination and manual rescan | ✓ | ✓ |
| Payment | Free | One-time payment |

\* Unlimited means no RedditClean daily allowance. Reddit's own rate limits and restrictions still apply.

**Pro is not yet available.** Pricing and availability will be announced closer to release.

The free daily allowance resets at **00:00 UTC** and is tracked across Reddit accounts within the same browser installation. Post deletion counts **attempts**, not just successful deletions. Clearing extension data or reinstalling may reset local records; browser-local limits cannot be made tamper-proof.

## Installation

RedditClean is currently available as a Chrome extension that can be installed manually.

1. Download the latest ZIP file from this repository's **Releases** section, when published, or from the latest distributed package.
2. Extract the ZIP file.
3. Open Chrome and go to `chrome://extensions`.
4. Enable **Developer mode**.
5. Click **Load unpacked**.
6. Select the extracted `redditclean-extension` folder containing `manifest.json`.

You can pin RedditClean to your Chrome toolbar for easy access.

**Updating:** Replace the extracted extension files and click **Reload** on the extension card. Removing and reinstalling the extension may erase browser-local replacement history and selections. Keep the existing installation where possible.

## How to Use

### Clean Comments

1. Log in to Reddit in Chrome.
2. Open RedditClean and select **Replace Comments**.
3. Wait for the **Filters & Preview** workspace to scan your comment history.
4. Optionally filter by subreddit, free text or date, then select **Apply filters**. The preview shows matching items and indicates when filters are active.
5. Select the comments you want to clean. Uncheck anything you want to keep. **Select all** and **Preserve all** act on the matching items.
6. Export a CSV backup if required.
7. Click **Replace Comments** and confirm the processing job.
8. Follow progress in the live preview. Comments replaced during this job appear in green at the top. Use **Pause**, **Resume** or **Stop** as needed.

**Done** closes the full-screen workspace without stopping an active job. A processing **session** means one job: pausing, resuming or reopening the workspace does not create a new session.

The free version replaces comments with:

```markdown
Deleted by [RedditClean](https://github.com/DamnYouRohan/RedditClean)
```

It **does not permanently delete comments**. Previously replaced comments are hidden from the default preview but can be displayed using **Show previously replaced (history)**. The summary distinguishes **Completed this session**, **Remaining selected** and **Previously replaced**. Historical counts in a filtered preview may reflect the currently discovered, matching items.

### Delete Posts

1. Open RedditClean and select **Delete Posts**.
2. Wait for the scan to complete.
3. Preview the posts and select those you want to remove.
4. Confirm your selection.
5. Monitor progress and any errors.

**Post deletion is irreversible.** Review your selections before proceeding. The free allowance is five deletion attempts per UTC day.

### Filters and Preview

The left sidebar supports **Only subreddits**, **Preserve subreddits**, **Contains text**, **From date** and **To date**. Apply filters to restrict the preview to matching comments. A **Filters applied** indicator appears beside the selection controls, and **Clear filters** is shown only while filters are active.

Clearing filters restores the unfiltered preview without intentionally undoing individual preservation choices. Use **Rescan** to refresh discovered history when processing is stopped.

## Privacy

RedditClean is designed to work locally in your browser.

- Uses your existing Reddit session.
- Does not require your Reddit password.
- Does not require a separate RedditClean account for the free version.
- Generates CSV exports locally.
- Does not require uploading your Reddit history to an external processing service.
- Stores processing progress, selections, allowance usage and replacement history in browser-local extension storage.

RedditClean is designed to minimise the information it needs to operate. It still interacts with Reddit's website to perform the edits and deletions you request.

## Limitations

**Reddit rate limits**

Reddit may temporarily restrict editing or deleting content. RedditClean does not bypass these restrictions.

**Historical content**

RedditClean scans content available through your Reddit profile. Some older comments and posts may not be accessible, so a complete history cannot be guaranteed.

**Comment replacement**

Replacing a comment does not guarantee that the original content has been removed from search engines, archives or third-party services.

**Browser-local history**

Previously replaced counts depend on records retained in the extension's local storage and on the active preview filters. Clearing storage or reinstalling can remove those records.

**Beta software**

RedditClean is still being developed and tested. Reddit interface changes may affect functionality. Automated checks do not replace live browser testing.

We recommend testing with a small number of items before running larger operations.

## Roadmap

We're continuing to improve RedditClean, with a focus on reliability and ease of use.

Planned improvements include:

- More reliable deletion verification and error handling.
- More extensive end-to-end testing and regression coverage.
- Improved progress reporting and recovery from interruptions.
- Additional filtering options.
- Permanent comment deletion.
- Comment randomisation before deletion.
- Pro licensing and activation.
- Performance improvements.

## Feedback and Issues

If you encounter a problem or have a suggestion, please open an issue in this repository.

Include the RedditClean version, Chrome version and a description of the issue. Screenshots are helpful, but please remove personal information before uploading them.

## Disclaimer

RedditClean is an independent project and is not affiliated with, endorsed by or sponsored by Reddit.

Editing and deleting Reddit content can be irreversible. Please review your selections and use the extension at your own risk.

---

**RedditClean. Your Reddit history, your choice.**

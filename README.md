# RedditClean

**Clean up your Reddit history.**

RedditClean is a Chrome extension that helps you review, edit and delete your Reddit comments and posts in bulk.

You can preview your history, filter by subreddit or date, and choose what to keep or remove.

RedditClean works through your existing Reddit session. No separate login or Reddit API credentials are required.

The extension is free to use, with an optional Pro version planned as a one-time purchase.

> **Current version: v0.16 (Beta)**
>
> RedditClean is under development. Please back up important content and review your selections before making changes.

## Features

- **Bulk comment replacement:** Replace multiple Reddit comments with a standard message.
- **Post deletion:** Delete posts from your Reddit history.
- **Preview before cleaning:** Review comments and posts before making changes.
- **Selective cleaning:** Choose which comments or posts to process.
- **Subreddit filters:** Include or exclude specific subreddits.
- **Date filters:** Clean content from a selected date range.
- **Pause and resume:** Pause processing and continue later.
- **CSV export:** Download a backup of your discovered Reddit history.
- **Progress tracking:** See how many items have been processed and how many remain.
- **Automatic pagination:** Scan multiple pages of your Reddit history.

## Free vs Pro

RedditClean offers a free version for occasional use. A Pro version is planned for users who want to clean larger amounts of content.

**Pro will be a one-time purchase. No subscription or recurring fees.**

| Feature | Free | Pro (planned) |
|---|---|---|
| Replace Reddit comments | 51 per day | Unlimited* |
| Delete Reddit posts | 5 attempts per day | Unlimited* |
| Randomise comments before deletion | — | ✓ |
| Permanently delete comments | — | ✓ |
| Preview comments and posts | ✓ | ✓ |
| Select individual items | ✓ | ✓ |
| Filter by subreddit | ✓ | ✓ |
| Filter by date | ✓ | ✓ |
| Exclude specific subreddits | ✓ | ✓ |
| Pause and resume | ✓ | ✓ |
| Export history to CSV | ✓ | ✓ |
| Progress tracking | ✓ | ✓ |
| Automatic pagination | ✓ | ✓ |
| Payment | Free | One-time payment |

\* Unlimited means no RedditClean daily allowance. Reddit's own rate limits and restrictions still apply.

**Pro is not yet available.** Pricing and availability will be announced closer to release.

## Installation

RedditClean is currently available as a Chrome extension that can be installed manually.

1. Download the latest ZIP file from this repository's **Releases** section.
2. Extract the ZIP file.
3. Open Chrome and go to `chrome://extensions`.
4. Enable **Developer mode**.
5. Click **Load unpacked**.
6. Select the extracted RedditClean folder containing `manifest.json`.

You can pin RedditClean to your Chrome toolbar for easy access.

## How to Use

### Clean Comments

1. Log in to Reddit in Chrome.
2. Open RedditClean and select **Delete Comments**.
3. Wait for RedditClean to scan your comment history.
4. Use **Filters & Preview** to review your comments.
5. Select the comments you want to clean.
6. Export a CSV backup if required.
7. Start cleaning.

The free version replaces comments with a standard message. It does not permanently delete them.

### Delete Posts

1. Open RedditClean and select **Delete Posts**.
2. Wait for the scan to complete.
3. Preview the posts and select those you want to remove.
4. Confirm your selection.
5. Monitor progress.

**Post deletion is irreversible.** Review your selections before proceeding.

## Privacy

RedditClean is designed to work locally in your browser.

- Uses your existing Reddit session.
- Does not require your Reddit password.
- Does not require a separate RedditClean account for the free version.
- Generates CSV exports locally.
- Does not require uploading your Reddit history to an external processing service.

RedditClean is designed to minimise the information it needs to operate.

## Limitations

**Reddit rate limits**

Reddit may temporarily restrict editing or deleting content. RedditClean does not bypass these restrictions.

**Historical content**

RedditClean scans content available through your Reddit profile. Some older comments and posts may not be accessible, so a complete history cannot be guaranteed.

**Comment replacement**

Replacing a comment does not guarantee that the original content has been removed from search engines, archives or third-party services.

**Beta software**

RedditClean is still being developed and tested. Reddit interface changes may affect functionality.

We recommend testing with a small number of items before running larger operations.

## Roadmap

We're continuing to improve RedditClean, with a focus on reliability and ease of use.

Planned improvements include:

- More reliable deletion verification and error handling.
- Improved progress tracking and reporting.
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

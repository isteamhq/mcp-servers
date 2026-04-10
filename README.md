# is.team MCP Servers

Open-source [Model Context Protocol](https://modelcontextprotocol.io) servers that let AI agents interact with real-world platforms — social media, advertising, and news.

All servers work with **Claude Code**, **Claude Desktop**, **Cursor**, and any MCP-compatible client. Zero config, just `npx`.

Built by [is.team](https://is.team) — the AI-native project management platform where AI agents and humans collaborate as real teammates.

---

## Servers

### Twitter/X &mdash; [@isteam/twitter-mcp](https://github.com/isteamhq/twitter-mcp)

Search tweets, post, reply, like, retweet, and follow — all through your AI agent.

**15 tools** | OAuth 1.0a | [npm](https://www.npmjs.com/package/@isteam/twitter-mcp)

```json
{
  "mcpServers": {
    "twitter": {
      "command": "npx",
      "args": ["-y", "@isteam/twitter-mcp"],
      "env": {
        "TWITTER_API_KEY": "your-api-key",
        "TWITTER_API_SECRET": "your-api-secret",
        "TWITTER_ACCESS_TOKEN": "your-access-token",
        "TWITTER_ACCESS_TOKEN_SECRET": "your-access-token-secret"
      }
    }
  }
}
```

<details>
<summary>All tools</summary>

| Tool | Description |
|------|-------------|
| `search_tweets` | Search tweets by keywords, hashtags, or phrases |
| `get_mentions` | Get recent mentions of the authenticated user |
| `get_user_tweets` | Get a user's recent tweets by username |
| `post_tweet` | Post a new tweet (max 280 characters) |
| `reply_tweet` | Reply to a tweet |
| `quote_tweet` | Quote tweet with commentary |
| `delete_tweet` | Delete a tweet |
| `like_tweet` | Like a tweet |
| `retweet` | Retweet a tweet |
| `follow_user` | Follow a user by username |
| `get_me` | Get authenticated user info |
| `get_tweet` | Get a specific tweet with metrics |
| `get_user` | Look up a user by username |
| `update_profile` | Update your profile |

</details>

---

### Bluesky &mdash; [@isteam/bluesky-mcp](https://github.com/isteamhq/bluesky-mcp)

Search posts, create content, engage with the AT Protocol ecosystem.

**15 tools** | App Password auth | [npm](https://www.npmjs.com/package/@isteam/bluesky-mcp)

```json
{
  "mcpServers": {
    "bluesky": {
      "command": "npx",
      "args": ["-y", "@isteam/bluesky-mcp"],
      "env": {
        "BLUESKY_IDENTIFIER": "your-handle.bsky.social",
        "BLUESKY_APP_PASSWORD": "your-app-password"
      }
    }
  }
}
```

<details>
<summary>All tools</summary>

| Tool | Description |
|------|-------------|
| `search_posts` | Search posts by keywords, hashtags, or phrases |
| `search_users` | Search users by name or handle |
| `get_user_feed` | Get a user's recent posts |
| `get_timeline` | Get your home timeline |
| `create_post` | Create a new post (max 300 chars, auto-detects links/mentions) |
| `reply_post` | Reply to a post |
| `delete_post` | Delete a post by AT URI |
| `like_post` | Like a post |
| `repost` | Repost a post |
| `follow_user` | Follow a user by handle |
| `get_profile` | Get a user's profile |
| `get_post` | Get a specific post with metrics |
| `get_thread` | Get a full post thread with replies |
| `get_notifications` | Get recent notifications |
| `update_profile` | Update your display name or bio |

</details>

---

### LinkedIn &mdash; [@isteam/linkedin-mcp](https://github.com/isteamhq/linkedin-mcp)

Post updates, share articles, comment, and track engagement on LinkedIn.

**10 tools** | OAuth 2.0 | [npm](https://www.npmjs.com/package/@isteam/linkedin-mcp)

```json
{
  "mcpServers": {
    "linkedin": {
      "command": "npx",
      "args": ["-y", "@isteam/linkedin-mcp"],
      "env": {
        "LINKEDIN_ACCESS_TOKEN": "your-access-token",
        "LINKEDIN_PERSON_ID": "your-person-id"
      }
    }
  }
}
```

<details>
<summary>All tools</summary>

| Tool | Description |
|------|-------------|
| `create_post` | Create a LinkedIn text post (max 3000 chars) |
| `create_article_post` | Share an article link with commentary |
| `delete_post` | Delete a post by URN |
| `comment_on_post` | Comment on a post (max 1250 chars) |
| `like_post` | Like/react to a post |
| `get_me` | Get authenticated user info |
| `get_post` | Get a post by URN |
| `get_comments` | Get comments on a post |
| `get_own_posts` | Get your recent LinkedIn posts |
| `get_post_stats` | Get like/comment counts for a post |

</details>

---

### Google Ads &mdash; [@isteam/google-ads-mcp](https://github.com/isteamhq/google-ads-mcp)

Full campaign management — create campaigns, manage keywords, run reports, track conversions.

**27 tools** | OAuth 2.0 + Developer Token | [npm](https://www.npmjs.com/package/@isteam/google-ads-mcp)

```json
{
  "mcpServers": {
    "google-ads": {
      "command": "npx",
      "args": ["-y", "@isteam/google-ads-mcp"],
      "env": {
        "GOOGLE_ADS_CLIENT_ID": "your-client-id",
        "GOOGLE_ADS_CLIENT_SECRET": "your-client-secret",
        "GOOGLE_ADS_DEVELOPER_TOKEN": "your-developer-token",
        "GOOGLE_ADS_REFRESH_TOKEN": "your-refresh-token",
        "GOOGLE_ADS_CUSTOMER_ID": "123-456-7890"
      }
    }
  }
}
```

<details>
<summary>All 27 tools</summary>

**Campaigns**: `list_campaigns`, `create_campaign`, `update_campaign`, `pause_campaign`, `remove_campaign`

**Ad Groups**: `list_ad_groups`, `create_ad_group`, `update_ad_group`

**Keywords**: `list_keywords`, `add_keywords`, `remove_keyword`, `keyword_ideas`

**Ads**: `list_ads`, `create_search_ad`, `update_ad_status`

**Budgets**: `list_budgets`, `update_budget`

**Reports**: `campaign_report`, `ad_group_report`, `keyword_report`, `search_terms_report`, `custom_query`

**Conversions**: `list_conversions`, `create_conversion_action`

**Audiences**: `list_audiences`, `create_audience`, `target_audience`

</details>

---

### Hacker News &mdash; [@isteam/hackernews-mcp](https://github.com/isteamhq/hackernews-mcp)

Search stories, read threaded comments, track trends, and explore user profiles. **No API key required.**

**10 tools** | No auth needed | [npm](https://www.npmjs.com/package/@isteam/hackernews-mcp)

```json
{
  "mcpServers": {
    "hackernews": {
      "command": "npx",
      "args": ["-y", "@isteam/hackernews-mcp"]
    }
  }
}
```

<details>
<summary>All tools</summary>

| Tool | Description |
|------|-------------|
| `top_stories` | Get current top stories |
| `new_stories` | Get newest stories |
| `best_stories` | Get highest-voted stories |
| `ask_stories` | Get Ask HN stories |
| `show_stories` | Get Show HN stories |
| `job_stories` | Get job postings |
| `get_story` | Get a specific story by ID |
| `search` | Full-text search via Algolia |
| `get_user` | Get a user profile |
| `get_comments` | Get threaded comments on a story |

</details>

---

## Why MCP?

[Model Context Protocol](https://modelcontextprotocol.io) is an open standard that lets AI agents call external tools. Instead of copy-pasting data into ChatGPT, your agent connects directly to the platforms you use.

These servers turn your AI into a real operator:

- **Marketing**: "Search Twitter for mentions of our product, then post a thank-you reply to each one"
- **Advertising**: "Create a Google Ads campaign for our spring sale with a $50/day budget"
- **Research**: "What's trending on Hacker News about AI agents? Summarize the top discussions"
- **Social**: "Post this announcement on Twitter, Bluesky, and LinkedIn simultaneously"

## Architecture

All servers share the same minimal architecture:

- **TypeScript** with strict mode
- **@modelcontextprotocol/sdk** for the MCP protocol layer
- **Zod** for input validation
- **Zero external dependencies** beyond the platform SDK (if needed)
- **Stdio transport** — works with any MCP client
- **Lazy auth** — credentials validated on first tool call, not on startup

Each server is a standalone npm package. Install with `npx`, no build step needed.

## Contributing

Each server has its own repository:

| Server | Repository | Issues |
|--------|------------|--------|
| Twitter/X | [isteamhq/twitter-mcp](https://github.com/isteamhq/twitter-mcp) | [Open issues](https://github.com/isteamhq/twitter-mcp/issues) |
| Bluesky | [isteamhq/bluesky-mcp](https://github.com/isteamhq/bluesky-mcp) | [Open issues](https://github.com/isteamhq/bluesky-mcp/issues) |
| LinkedIn | [isteamhq/linkedin-mcp](https://github.com/isteamhq/linkedin-mcp) | [Open issues](https://github.com/isteamhq/linkedin-mcp/issues) |
| Google Ads | [isteamhq/google-ads-mcp](https://github.com/isteamhq/google-ads-mcp) | [Open issues](https://github.com/isteamhq/google-ads-mcp/issues) |
| Hacker News | [isteamhq/hackernews-mcp](https://github.com/isteamhq/hackernews-mcp) | [Open issues](https://github.com/isteamhq/hackernews-mcp/issues) |

PRs welcome. Keep it minimal — no unnecessary dependencies, no feature creep.

## About is.team

[is.team](https://is.team) is an AI-native project management platform. AI agents join your boards as real team members — they create tasks, chat in threads, and ship work alongside humans.

These MCP servers are part of the is.team open-source ecosystem. We use them internally to let our AI agents manage social media, run ad campaigns, and monitor tech communities — all from within project boards.

**Try is.team free** &rarr; [is.team](https://is.team)

## License

All servers are MIT licensed.

# Video transcripts by Clipscript

Video transcript generator for Claude and Codex: transcribe YouTube videos and Shorts, TikTok, Instagram Reels, Facebook and X videos to text with [Clipscript](https://cliptranscript.app). Paste a link, get the video as text with timestamps, then summarise it, quote it or export subtitles and captions as TXT, SRT, VTT or JSON.

## Install

```sh
/plugin marketplace add cliptranscript/plugin
/plugin install clipscript@clipscript
```

The plugin adds the remote MCP server `https://cliptranscript.app/mcp` and a skill. The first tool call opens cliptranscript.app for sign-in and consent. Without the plugin, add the same URL as a custom connector in Claude (Settings → Connectors) or run `claude mcp add --transport http clipscript https://cliptranscript.app/mcp`. On Pro and Scale you can connect with an API key instead: send `Authorization: Bearer cs_live_…` (keys at https://cliptranscript.app/app/developers/).

## Tools

| Tool | Plan | What it does |
| --- | --- | --- |
| `get_transcript` | All | Transcript of one video link, with optional timestamps. |
| `bulk_transcripts` | Creator and up | Up to 10 links in one call. |
| `list_channel_videos` | Creator and up | Latest videos of a YouTube channel, TikTok or Instagram profile. Read-only. |
| `list_history` | All | Your saved transcripts. Read-only. |
| `get_saved_transcript` | All | Full text of one saved transcript. Read-only. |
| `export_transcript` | All (SRT, VTT, JSON on Creator and up) | TXT, SRT, VTT or JSON. Read-only. |
| `get_usage` | All | Your plan and allowance used. Read-only. |

Each new transcript uses 1 from your plan; videos already in your history are free to reopen. Plans: Free account with 5 free transcripts, once, no card; subscribe for more: Creator $9/month (400), Pro $19/month (1,500, API keys), Scale $49/month (4,000).

[Website](https://cliptranscript.app) · [Privacy](https://cliptranscript.app/privacy/) · [Terms](https://cliptranscript.app/terms/) · MIT license

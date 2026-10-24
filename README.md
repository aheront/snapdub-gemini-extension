# SnapDub extension for Gemini CLI

Turn long videos into short vertical clips with captions from your terminal. Paste a YouTube,
Twitch, Kick, Rumble or Zoom link, and [SnapDub](https://snapdub.ai) finds the moments that stand
on their own, crops them to 9:16 and burns in captions for TikTok, Reels and Shorts.

## Install

```
gemini extensions install https://github.com/aheront/snapdub-gemini-extension
```

The first SnapDub call opens your browser to sign in (a free account includes starting credits).

## Use

- `/clip https://www.youtube.com/watch?v=...` - make clips from a video
- `/clips` - show the finished clips of your latest video
- Or just ask: "make clips from this stream", "how many SnapDub credits do I have left?"

It talks to the SnapDub MCP server at `https://snapdub.ai/mcp` (OAuth). More:
[snapdub.ai/mcp-server](https://snapdub.ai/mcp-server).

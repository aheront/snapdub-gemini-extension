# SnapDub

SnapDub turns long videos into short vertical clips (9:16) with captions, ready for TikTok,
Instagram Reels, YouTube Shorts and LinkedIn. The `snapdub` MCP server exposes these tools:

- `create_video` - make clips from a video link (YouTube, Twitch, Kick, Rumble or Zoom). Optional:
  `clips`, `clip_length_seconds`, `captions`, `translate_to`, `template`. Spends SnapDub credits, so
  confirm the link with the user before calling it. Returns a video id and progress.
- `get_video` - status and progress of a video.
- `list_clips` - the finished clips of a video: title, virality score, length, download link.
- `list_videos` - the user's recent videos.
- `list_templates` - saved templates (caption style, branding) that `create_video` can apply.
- `whoami` - account, plan and remaining credits.
- `list_campaigns` - live clipping campaigns that pay per view.

Processing takes a few minutes for a short video and longer for a long stream. After
`create_video`, tell the user it is running and offer to check with `get_video`; when the status
is done, show the clips from `list_clips` as a table. Only report what the tools return.

The first call opens a browser to sign in to SnapDub (free account with starting credits).

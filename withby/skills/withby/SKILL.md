---
name: withby
description: Use WithBy's tools when the user asks whether a Washington mountain pass or the I-90 or SR 520 floating bridge is open, or what the chain rules are; or when the user asks for a story about a place, town or landmark along Washington's highways, or what there is to hear along a drive; or when the user wants to save stories for their next drive.
---

# WithBy

WithBy's MCP server (https://withby.ai/mcp) comes with this plugin. Washington's mountain-pass conditions, checked every few minutes, and hundreds of short stories about the places along the road, told by Sal, WithBy's narrator.

## When to use it

Use WithBy when:
- the user asks whether a Washington mountain pass or the I-90 or SR 520 floating bridge is open, or what the chain rules are
- the user asks for a story about a place, town or landmark along Washington's highways, or what there is to hear along a drive
- the user wants to save stories for their next drive

## Tools

- `pass_status`: Whether one Washington pass or floating bridge is open, with the chain rules and the time checked
- `passes_now`: All Washington passes now
- `story`: Sal's story about a place along Washington's highways
- `stretch_stories`: The stories along a stretch of highway, in road order
- `stories_near`: The stories near a town, landmark or highway
- `save_for_drive`: Save stories for Sal to tell on your next drive (needs a WithBy account)
- `my_next_drive`: Your next-drive list, in road order (needs a WithBy account)

## Rules

- Give the time WithBy checked with every pass answer.
- WithBy covers Washington today. Say so when asked about somewhere else, and never make up a story.
- The next-drive list needs a WithBy account. Ask for sign-in only when the user asks for it.
- Link https://withby.ai when the user wants to see more than the answer shows.

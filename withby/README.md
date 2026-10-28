# WithBy

Washington's mountain-pass conditions, checked every few minutes, and hundreds of short stories about the places along the road, told by Sal, WithBy's narrator.

This repository connects AI agents to [WithBy](https://withby.ai) through WithBy's own remote [MCP](https://modelcontextprotocol.io) server, `https://withby.ai/mcp`. It is a plugin for Cursor and Claude Code and an extension for Gemini CLI. Nothing installs or runs on your computer: the tools come from the server.

## What it does

WithBy checks Washington's mountain passes every few minutes and judges each direction of Snoqualmie, Stevens, White and Blewett passes: open, chains or closed, with the time it looked. For 12 other passes and the I-90 and SR 520 floating bridges it gives WSDOT's own words.

It has hundreds of short stories about the places along the state's highways, told by Sal, WithBy's road-trip narrator. Ask whether a pass is open, ask for a story about a place, hear what Sal knows near a town or along a stretch of highway, and save the stories you want him to tell you on your next drive. WithBy covers Washington's highways today and says so when you ask about somewhere else.

## Tools

| Tool | What it does | Needs an account |
| --- | --- | --- |
| `pass_status` | Whether one Washington pass or floating bridge is open, with the chain rules and the time checked | no |
| `passes_now` | All Washington passes now | no |
| `story` | Sal's story about a place along Washington's highways | no |
| `stretch_stories` | The stories along a stretch of highway, in road order | no |
| `stories_near` | The stories near a town, landmark or highway | no |
| `save_for_drive` | Save stories for Sal to tell on your next drive | yes |
| `my_next_drive` | Your next-drive list, in road order | yes |

The server is the source of truth for tool names and schemas.

## Try

- Is Snoqualmie Pass open right now? Check WithBy.
- Tell me WithBy's story of Snoqualmie Falls.
- What does Sal know near North Bend?

## Install

**Cursor:** [Add WithBy to Cursor](https://cursor.com/install-mcp?name=withby&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vd2l0aGJ5LmFpL21jcCJ9), or add it to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "withby": {
      "type": "http",
      "url": "https://withby.ai/mcp"
    }
  }
}
```

**Claude Code:**

```
/plugin marketplace add yojowa/withby-plugin
/plugin install withby@withby
```

or `claude mcp add --transport http withby https://withby.ai/mcp`.

**Gemini CLI:**

```
gemini extensions install https://github.com/yojowa/withby-plugin
```

**ChatGPT, Claude, the Gemini app and other assistants:** see [withby.ai/assistants](https://withby.ai/assistants).

## Signing in

The tools marked "yes" need a WithBy account. The first time you use one, your agent opens WithBy's sign-in page, and you choose whether to let it use your account. The other tools work without signing in. You can disconnect at any time from your WithBy profile.

## Privacy and support

- Privacy policy: https://withby.ai/privacy
- Terms: https://withby.ai/terms
- Support: support@withby.ai

## License

MIT, for the files in this repository. The WithBy service is covered by its [terms](https://withby.ai/terms).

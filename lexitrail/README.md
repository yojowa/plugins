# LexiTrail

Look up any Chinese word with its pinyin, meaning, HSK level, stroke order and sound, and keep track of the HSK words you are learning on LexiTrail.

This repository connects AI agents to [LexiTrail](https://lexitrail.com) through LexiTrail's own remote [MCP](https://modelcontextprotocol.io) server, `https://lexitrail.com/mcp`. It is a plugin for Cursor and Claude Code and an extension for Gemini CLI. Nothing installs or runs on your computer: the tools come from the server.

## What it does

LexiTrail is a Chinese vocabulary trainer built on the official HSK word lists. Ask about any word, in characters, pinyin or English (or Spanish, Indonesian, Thai or Vietnamese), and see it with its pinyin, its meanings, its HSK level, its strokes and a link to hear it on lexitrail.com. Ask what is in an HSK level or topic.

With a LexiTrail account, see how far along each HSK level you are and save words from your conversation into your reviews, so they come back when you are about to forget them.

## Tools

| Tool | What it does | Needs an account |
| --- | --- | --- |
| `look_up_word` | Find a Chinese word from its characters, its pinyin or a meaning: pinyin, meanings, HSK level | no |
| `stroke_data` | Stroke data for a word's characters, to draw them stroke by stroke | no |
| `hsk_words` | What is in an HSK level (1–6), an HSK 3.0 band or a topic | no |
| `my_progress` | Your LexiTrail progress by HSK level, and reviews due today | yes |
| `save_words` | Save up to 20 HSK words to your LexiTrail sets, so they come up in practice | yes |

The server is the source of truth for tool names and schemas.

## Try

- How do you write 'feedback' in Chinese?
- What's in HSK 3?
- What HSK level is 意见?

## Install

**Cursor:** [Add LexiTrail to Cursor](https://cursor.com/install-mcp?name=lexitrail&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vbGV4aXRyYWlsLmNvbS9tY3AifQ%3D%3D), or add it to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "lexitrail": {
      "type": "http",
      "url": "https://lexitrail.com/mcp"
    }
  }
}
```

**Claude Code:**

```
/plugin marketplace add yojowa/lexitrail-plugin
/plugin install lexitrail@lexitrail
```

or `claude mcp add --transport http lexitrail https://lexitrail.com/mcp`.

**Gemini CLI:**

```
gemini extensions install https://github.com/yojowa/lexitrail-plugin
```

**ChatGPT, Claude, the Gemini app and other assistants:** see [lexitrail.com/support](https://lexitrail.com/support).

## Signing in

The tools marked "yes" need a LexiTrail account. The first time you use one, your agent opens LexiTrail's sign-in page, and you choose whether to let it use your account. The other tools work without signing in. You can disconnect at any time from your LexiTrail profile.

## Privacy and support

- Privacy policy: https://lexitrail.com/privacy
- Terms: https://lexitrail.com/terms
- Support: support@lexitrail.com

## License

MIT, for the files in this repository. The LexiTrail service is covered by its [terms](https://lexitrail.com/terms).

# FamilyLore

Reads handwritten family letters in old scripts (Russian and Ukrainian cursive, German Kurrent and Sütterlin, Yiddish) and translates them, with notes on what they meant at the time.

This repository connects AI agents to [FamilyLore](https://familylore.ai) through FamilyLore's own remote [MCP](https://modelcontextprotocol.io) server, `https://familylore.ai/mcp`. It is a plugin for Cursor and Claude Code and an extension for Gemini CLI. Nothing installs or runs on your computer: the tools come from the server.

## What it does

FamilyLore reads the handwriting in old family letters, postcards and documents and translates it, with notes on the words, places and customs a reader today would miss. It reads the scripts families find hardest: pre-1918 Russian and Ukrainian cursive, German Kurrent and Sütterlin, and Yiddish.

Ask FamilyLore to read a page and send the photo through the link it gives you. About a minute and a half later the reading comes back: the text line by line in its own script, a translation into English, German or Russian, and notes on what the letter meant then. You can then ask about the letter, such as what a phrase meant or who someone was. The answer shows the lines it rests on, or says that the letter doesn't say.

Without an account you can look through sixteen real letters written between 1758 and 1943, each with its reading, and ask how a letter was written in Russian cursive, German Kurrent, Sütterlin, Hebrew cursive or American cursive.

## Tools

| Tool | What it does | Needs an account |
| --- | --- | --- |
| `real_letters` | Real letters, 1758–1943: sixteen handwritten letters, each with its reading | no |
| `script_guide` | How a letter was written in Russian cursive, Kurrent, Sütterlin, Hebrew cursive or American cursive | no |
| `read_letter` | Read a photographed page: the text in its own script, a translation and notes | yes |
| `upload_slot` | A one-time link to send the photo of a page | yes |
| `reading_status` | Where a page's reading is while it is read | yes |
| `get_reading` | The reading of a page in your account | yes |
| `my_letters` | The pages in your account, newest first | yes |
| `ask_letter` | Ask about one letter: what a phrase meant, who someone was | yes |
| `my_allowance` | How many pages your account has left to read | yes |

The server is the source of truth for tool names and schemas.

## Try

- Read my great-grandmother's letter with FamilyLore
- Show me a real letter written in Kurrent from FamilyLore
- How was the letter Ж written in old Russian cursive? Ask FamilyLore

## Install

**Cursor:** [Add FamilyLore to Cursor](https://cursor.com/install-mcp?name=familylore&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vZmFtaWx5bG9yZS5haS9tY3AifQ%3D%3D), or add it to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "familylore": {
      "type": "http",
      "url": "https://familylore.ai/mcp"
    }
  }
}
```

**Claude Code:**

```
/plugin marketplace add yojowa/familylore-plugin
/plugin install familylore@familylore
```

or `claude mcp add --transport http familylore https://familylore.ai/mcp`.

**Gemini CLI:**

```
gemini extensions install https://github.com/yojowa/familylore-plugin
```

**ChatGPT, Claude, the Gemini app and other assistants:** see [familylore.ai/assistants](https://familylore.ai/assistants).

## Signing in

The tools marked "yes" need a FamilyLore account. The first time you use one, your agent opens FamilyLore's sign-in page, and you choose whether to let it use your account. The other tools work without signing in. You can disconnect at any time from your FamilyLore profile.

## Privacy and support

- Privacy policy: https://familylore.ai/privacy
- Terms: https://familylore.ai/terms
- Support: support@familylore.ai

## License

MIT, for the files in this repository. The FamilyLore service is covered by its [terms](https://familylore.ai/terms).

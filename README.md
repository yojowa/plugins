# Yojowa plugins

Plugins for Cursor and Claude Code that connect AI agents to four products by Yojowa LLC. Each one uses the product's own remote MCP server, so nothing installs or runs on your computer.

| Product | What it does | Plugin |
| --- | --- | --- |
| [FamilyLore](https://familylore.ai) | Reads handwritten family letters in old scripts (Russian and Ukrainian cursive, German Kurrent and Sütterlin, Yiddish) and translates them, with notes on what they meant at the time. | [`familylore/`](familylore) · [own repo](https://github.com/yojowa/familylore-plugin) |
| [StockMap](https://stockmap.io) | Every night StockMap's model makes a call on over 4,000 US stocks and keeps a public record of how each call turned out. See a stock's call, the reasons for and against, its record, and the whole market as a map. | [`stockmap/`](stockmap) · [own repo](https://github.com/yojowa/stockmap-plugin) |
| [WithBy](https://withby.ai) | Washington's mountain-pass conditions, checked every few minutes, and hundreds of short stories about the places along the road, told by Sal, WithBy's narrator. | [`withby/`](withby) · [own repo](https://github.com/yojowa/withby-plugin) |

Each plugin also has its own repository, which adds a Gemini CLI extension.

## Install

**Cursor:** use each plugin's "Add to Cursor" link in its README.

**Claude Code:**

```
/plugin marketplace add yojowa/plugins
/plugin install stockmap@yojowa
```

## Support

support@yojowa.com

## License

MIT, for the files in this repository. Each service is covered by its own terms.

---
name: familylore
description: Use FamilyLore's tools when the user wants an old handwritten letter, postcard or document read or translated, especially in pre-1918 Russian or Ukrainian cursive, German Kurrent or Sütterlin, or Yiddish; or when the user asks how a letter of an old handwriting style was written, or wants to see a real old letter; or when the user asks about a letter they already read on FamilyLore.
---

# FamilyLore

FamilyLore's MCP server (https://familylore.ai/mcp) comes with this plugin. Reads handwritten family letters in old scripts (Russian and Ukrainian cursive, German Kurrent and Sütterlin, Yiddish) and translates them, with notes on what they meant at the time.

## When to use it

Use FamilyLore when:
- the user wants an old handwritten letter, postcard or document read or translated, especially in pre-1918 Russian or Ukrainian cursive, German Kurrent or Sütterlin, or Yiddish
- the user asks how a letter of an old handwriting style was written, or wants to see a real old letter
- the user asks about a letter they already read on FamilyLore

## Tools

- `real_letters`: Real letters, 1758–1943: sixteen handwritten letters, each with its reading
- `script_guide`: How a letter was written in Russian cursive, Kurrent, Sütterlin, Hebrew cursive or American cursive
- `read_letter`: Read a photographed page: the text in its own script, a translation and notes (needs a FamilyLore account)
- `upload_slot`: A one-time link to send the photo of a page (needs a FamilyLore account)
- `reading_status`: Where a page's reading is while it is read (needs a FamilyLore account)
- `get_reading`: The reading of a page in your account (needs a FamilyLore account)
- `my_letters`: The pages in your account, newest first (needs a FamilyLore account)
- `ask_letter`: Ask about one letter: what a phrase meant, who someone was (needs a FamilyLore account)
- `my_allowance`: How many pages your account has left to read (needs a FamilyLore account)

## Rules

- Reading a page needs a FamilyLore account. Ask for sign-in only when the user asks for a reading or for their own letters.
- Send the photo through the link `upload_slot` gives you, then follow the reading with `reading_status` until it is done.
- When you answer from a reading, quote the lines it rests on, and say so when the letter doesn't say.
- Link https://familylore.ai when the user wants to see more than the answer shows.

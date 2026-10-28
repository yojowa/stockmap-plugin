# StockMap

Every night StockMap's model makes a call on over 4,000 US stocks and keeps a public record of how each call turned out. See a stock's call, the reasons for and against, its record, and the whole market as a map.

This repository connects AI agents to [StockMap](https://stockmap.io) through StockMap's own remote [MCP](https://modelcontextprotocol.io) server, `https://stockmap.io/mcp`. It is a plugin for Cursor and Claude Code and an extension for Gemini CLI. Nothing installs or runs on your computer: the tools come from the server.

## What it does

StockMap runs a model over the US stock market every night. For each stock it makes a 14-day call, lists the insights for and against it in plain words, and grades every past call so you can see how often it was right on that stock.

Ask about a stock to see its call, reasons and record, or compare two to five side by side; open the market map to see every sector by the model's call; ask what changed last night. For crypto, ask why it is up or down today, whether it is altseason, or whether your coins beat Bitcoin. Signed in, keep watchlists and see what changed on them.

StockMap shows a model's track-recorded read. It is not financial advice and it does not trade.

## Tools

| Tool | What it does | Needs an account |
| --- | --- | --- |
| `stock_call` | The model's nightly 14-day call on one US stock, the reasons for and against, and its record | no |
| `compare_stocks` | Two to five US stocks side by side | no |
| `last_night` | What changed in the calls last night | no |
| `market_map` | The market's 11 sectors and which lead or lag | no |
| `sector` | One sector or industry | no |
| `crypto_today` | Why crypto is up or down today | no |
| `is_it_altseason` | How many top coins beat Bitcoin over the last 7 days | no |
| `crypto_stocks` | Which US crypto stocks the model leans on | no |
| `bitcoin_test` | Did your coins beat Bitcoin | no |
| `my_watchlists` | Your watchlists, with the calls that changed last night first | yes |
| `watch` | Add a US stock to a watchlist | yes |
| `unwatch` | Remove a US stock from your watchlists | yes |

The server is the source of truth for tool names and schemas.

## Try

- What does StockMap think of NVDA?
- Show me the stock market map
- What changed in StockMap's calls last night?

## Install

**Cursor:** [Add StockMap to Cursor](https://cursor.com/install-mcp?name=stockmap&config=eyJ0eXBlIjoiaHR0cCIsInVybCI6Imh0dHBzOi8vc3RvY2ttYXAuaW8vbWNwIn0%3D), or add it to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "stockmap": {
      "type": "http",
      "url": "https://stockmap.io/mcp"
    }
  }
}
```

**Claude Code:**

```
/plugin marketplace add yojowa/stockmap-plugin
/plugin install stockmap@stockmap
```

or `claude mcp add --transport http stockmap https://stockmap.io/mcp`.

**Gemini CLI:**

```
gemini extensions install https://github.com/yojowa/stockmap-plugin
```

**ChatGPT, Claude, the Gemini app and other assistants:** see [stockmap.io/assistants](https://stockmap.io/assistants).

## Signing in

The tools marked "yes" need a StockMap account. The first time you use one, your agent opens StockMap's sign-in page, and you choose whether to let it use your account. The other tools work without signing in. You can disconnect at any time from your StockMap profile.

## Privacy and support

- Privacy policy: https://stockmap.io/privacy
- Terms: https://stockmap.io/terms
- Support: support@stockmap.io

## License

MIT, for the files in this repository. The StockMap service is covered by its [terms](https://stockmap.io/terms).

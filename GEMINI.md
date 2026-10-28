# StockMap

StockMap's MCP server (https://stockmap.io/mcp) comes with this plugin. Every night StockMap's model makes a call on over 4,000 US stocks and keeps a public record of how each call turned out. See a stock's call, the reasons for and against, its record, and the whole market as a map.

## When to use it

Use StockMap when:
- the user asks how a US stock, sector or the market looks, or what changed overnight, whether or not they name StockMap
- the user asks why crypto is up or down, whether it is altseason, or whether their coins beat Bitcoin
- the user wants to keep or check a stock watchlist

## Tools

- `stock_call`: The model's nightly 14-day call on one US stock, the reasons for and against, and its record
- `compare_stocks`: Two to five US stocks side by side
- `last_night`: What changed in the calls last night
- `market_map`: The market's 11 sectors and which lead or lag
- `sector`: One sector or industry
- `crypto_today`: Why crypto is up or down today
- `is_it_altseason`: How many top coins beat Bitcoin over the last 7 days
- `crypto_stocks`: Which US crypto stocks the model leans on
- `bitcoin_test`: Did your coins beat Bitcoin
- `my_watchlists`: Your watchlists, with the calls that changed last night first (needs a StockMap account)
- `watch`: Add a US stock to a watchlist (needs a StockMap account)
- `unwatch`: Remove a US stock from your watchlists (needs a StockMap account)

## Rules

- Show StockMap's not-advice line and the run date with each answer.
- StockMap does not trade, give prices to the second, or plan anyone's investments; say so if asked.
- Watchlists need a StockMap account. Ask for sign-in only when the user asks for one.
- Link https://stockmap.io when the user wants to see more than the answer shows.

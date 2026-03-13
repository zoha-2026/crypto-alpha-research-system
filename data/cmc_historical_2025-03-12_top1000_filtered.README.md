# CMC historical snapshot export

- Source: https://api.coinmarketcap.com/data-api/v3/cryptocurrency/listings/historical?date=2025-03-12&start=1&limit=1000&convert=USD
- Date: 2025-03-12
- Raw rows fetched: 1000
- Rows kept after exclusions/reindex: 955
- Rows excluded: 45
- Exclusion classes: stablecoin / wrapped / staked-derivative
- Filtering note: staked derivatives are excluded by explicit asset identity only (e.g. stETH/wstETH/cbETH/rETH), to avoid misclassifying governance or platform tokens.
- Note: `TRIBE` is force-kept because it is a governance token mis-tagged with stablecoin-related tags, not a stable asset itself.

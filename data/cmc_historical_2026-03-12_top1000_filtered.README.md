# CMC historical snapshot export

- Source: https://api.coinmarketcap.com/data-api/v3/cryptocurrency/listings/historical?date=2026-03-12&start=1&limit=1000&convert=USD
- Date: 2026-03-12
- Raw rows fetched: 1000
- Rows kept after exclusions/reindex: 862
- Rows excluded: 138
- Exclusion classes: stablecoin / wrapped / staked-derivative
- Exclusion count by reason: stablecoin=70, wrapped=26, staked-derivative=42
- Filtering note: stablecoins are filtered by stablecoin tags plus historical explicit identities; wrapped assets are filtered by explicit wrapped identities, `Wrapped*` names, and obvious bridged assets such as `*Bridged` / `*BEP2`; staked derivatives are filtered by explicit asset identities plus obvious `Staked` / `Restaked` derivative names, while governance / service tokens like LDO / RPL / JTO are kept.
- Note: `TRIBE` is force-kept because it is a governance token mis-tagged with stablecoin-related tags, not a stable asset itself.

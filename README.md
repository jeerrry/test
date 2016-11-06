# test
### What we have accomplished so far

# Mission
Democratising finance by providing individual investors with professional data and analysis.
# Components
* A cross-platform app for __tracking__ investment performance.
* An dynamic database for __user contributed market data__.
* A data-driven social network where investors can __share__ performance, __find__ investment products and __promote__ asset management services.

# Market Outlook
* __Pain Point #1__ : Investors with multiple accounts have difficulties consolidating their data. They have to use an externaly application or spreadsheet for account aggregation.
* __Pian Point #2__ : Portfolio trackers by major websites like Yahoo and Google can not fulfill the needs of sophisticated personal investors. There's no web-based tool can tracks and aggregates multiple cross-asset portfolios.
* __Pain Point #3__ : Retail investors don't have access to professional performance and risk analysis. They will want it if the cost is low. 
* __Pain Point #4__ : No vendor can cover the market data needs for all investors. Investors always know better in certain areas.
* __Market Potential__ : China/Asia is having a boom in personal wealth. The region's under-developed wealth management infrastructure gives unique opportunities for Internet wealth management solutions. Think about Alibaba/Taobao at the dawn of e-commerce. A portfolio tracking platform is the gateway to this new field.

# Roadmap
## Minimum Viable Product (MVP)
__Highlights__ :
* __Cross-market portfolios__: Each portfolio can hold securities in multiple markets/currencies. FX impact in market values and PnL are handled as per industry practice. 
* __Portfolio aggregation__: Performance of sub-portfolios are aggregated to parents. A cascading tree-view
* __User data overrides__: User can override any prices from the system to for their own calculation, without affecting others.
* __Snapshot-based portfolio construction__: An existing portfolio can be replicated in minutes by inputting only the current holdings, regardless the number of past transactions. User can add transactions later and the portfolio seamlessly updates its historical performance. 
* Web app only.
* Use Firebase as back end database, all calculation done by front-end JS.
* Support multiple instruments: stocks, ETF, CFD, futures and spot FX.
* Track positions in different asset classes and currencies in one portfolio.
* Aggregate performance of multiple portfolios.
* Daily update  (end-of-day prices only).
* Overwrite market data with user's contribution, for own portfolio only.

## Further Developments
__Concept__ : __High__ function complexity, __High__ server burden, __Low__ user flexibility
* Android & iOS apps.
* Move middleware to NodeJS server.
* Allow user creating customised securities.
* Real-time price feeds.
* Performance attribution
* Risk analysis

# MVP Design
### Portfolio Table

### Performance Chart

#### MV Curve (Portfolio)
* __Curve:__ portfolio market value
* __Tooltip:__ date, MV, MV day change
* __Annotation__: external cashflows

#### MV Curve (Security)
* __Curve:__ position market value
* __Tooltip:__ date, MV, MV day change
* __Annotation__: transactions

#### PnL Curve (Portfolio)
* __Curve:__ portfolio PnL value _(relative vs absolute? $ vs %?)_
* __Tooltip:__ date, PnL, PnL day change
* __Annotation:__ external cashflows _(?)_

#### PnL Curve (Security)
* __Curve:__ position PnL value
* __Tooltip:__ date, PnL, PnL day change
* __Annotation:__ transactions

# Product Q&A
__How to tell users' real investment portfolios apart from dummies?__

We will aggrigate all portfolios of a user to calculate the total market value. User can tag certain portfolios as _dummy_ exclude them from the aggregation. If a user tags some of her portfolios as _dummy_, we are confident to assume the other portfolios are 'real' for this user.

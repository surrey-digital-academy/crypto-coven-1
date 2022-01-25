# Create Your NFT Collection Dashboard
This code template is designed to get your own customized NFT Collection Dashboard up and running **in just minutes!**.

In `src/config.js`, simply set your:
- NFT collection contract address
- Blockchain `chain_id` where the contract address is deployed
- Dashboard title and banner

That's it!

## Live Demo
Visit https://covalenthq.github.io/nft-dashboard-template/ for a live demo. 

* On GitHub, the code is open sourced and available at https://github.com/covalenthq/nft-dashboard-template/tree/main

* On our [**Replit page**](https://replit.com/@Covalent-Templates/NFT-Collection-Dashboard-Template?v=1), just press `Run` to see this NFT Collection Dashboard in action.

The live demo displays:
* An NFT collection dashboard page with a summary, a floor price graph and a preview of the first 5 NFTs in the collection 
* Ability to see where your specific collection ranks in the global view of all NFT collections on a specific blockchain
* Ability to select a specific NFT in your collection and see its metadata

## Fork and Customize
Fork and customize this NFT Collection template in just a few steps by updating the following code in `src/config.js`:

```
TEMPLATE: {
    // 1. Set your NFT collection contract address
    "collection_address": "0x9498274b8c82b4a3127d67839f2127f2ae9753f4",

    // 2. Set your blockchain chain ID where your NFT collection contract address is deployed (see below for value options)
    "block_chain_id": "137",

    // 3. Set the default title of your dashboard. If found, this template uses the NFT Collection name for the title.
    "title": "My NFT Collection",

    // 4. (Optional) Boolean for displaying the floor price chart
    "timeseries_chart": true,

    // 5. (Optional) Set your banner image
    "banner_picture": "https://www.superflexfitness.com/wp-content/uploads/2017/03/3D-banner-background.jpg",
  },
```

## Deploy to GitHub pages
This code template is designed to work seamlessly with GitHub pages. Simply do the following:

1. Update the `homepage` field in `package.json` with the URL of your GitHub project page for this template or a custom domain. 

2. Deploy the site by running `npm run deploy`

3. On GitHub, ensure your project's settings use the `gh-pages` branch. 

See https://create-react-app.dev/docs/deployment/#github-pages for details and if you run into any issues. 


## Covalent API Endpoints
The two Covalent API endpoints used in this code template include:

1. Detail view of a specific collection:

`/{chain_id}/nft_market_cap/{collection}`

This endpoint allows one to drill down into the details of a collection and the response object looks like the following:
```
{
  "data": {
    "updated_at": "2021-12-19T05:25:26.926980Z",
    "items": [
      {
        "chain_id": 1,
        "collection_name": "MyCryptoHeroes:Land",
        "collection_address": "0x617913dd43dbdf4236b85ec7bdf9adfd7e35b340",
        "collection_ticker_symbol": "MCHL",
        "volume_eth_24h": "0",
        "volume_quote_24h": 0.0,
        "average_volume_eth_24h": "0",
        "average_volume_quote_24h": 0.0,
        "eth_quote_rate": 3905.4487,
        "opening_date": "2020-09-29",
        "volume_eth_day": "500000000000000000",
        "volume_quote_day": 176.95366,
        "average_volume_eth_day": "500000000000000000",
        "average_volume_quote_day": 176.95366,
        "unique_token_ids_sold_count_day": 1,
        "eth_quote_rate_day": 353.90732,
        "quote_currency": "USD"
      },
```
Data for the detail view is at a day granularity. 


2. Global view of Market Cap per blockchain:

`/{chain_id}/nft_market_cap`

This endpoint provides a global view of multiple NFT collections from various marketplaces (from multiple chains) in a table that ranks them on their market cap.

The response object looks similar to the following:
```
{
  "data": {
    "updated_at": "2021-12-19T01:19:05Z",
    "items": [
      {
        "chain_id": 1,
        "collection_name": "Art Blocks",
        "collection_address": "0xa7d8d9ef8d8ce8992df33d8b8cf4aebabd5bd270",
        "volume_eth_24h": "200068300000000000000",
        "volume_quote_24h": 798097.3,
        "avg_volume_eth_24h": "1064193085106380000",
        "avg_volume_quote_24h": 4245.198,
        "contract_deployment_at": null,
        "market_cap_eth": "207008137260122000000000",
        "market_cap_quote": 825781180,
        "transaction_count_alltime": 121941,
        "unique_wallet_purchase_count_alltime": 22858,
        "unique_token_ids_sold_count_alltime": 65862,
        "max_price_eth": "2100000000000000000000",
        "max_price_quote": 8377161.0,
        "floor_price_eth": "955014280778427000",
        "floor_price_quote": 3809.6707,
        "eth_quote_rate": 3989.1243,
        "quote_currency": "USD",
        "opening_date": "2021-12-18"
      },
```

While a default `COVALENT_API_KEY` is used for this code template, it is recommended you register and use your own free API key from: https://www.covalenthq.com/platform

## Feedback and Support

If you have any questions, comments and feedback regarding this code template, please message us on Discord: https://covalenthq.com/discord

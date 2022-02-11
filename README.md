# libblkmakers
MIT-licensed C implementation of getblocktemplate
2022-2-09

New endpoint for Wallet:
POST /sapi/v1/asset/dust-btc to get assets that can be converted into BNB
2022-1-25

From January 28, 2022 4:00 AM UTC, You need to openEnable Spot & Margin Tradingpermission for the API key which requests these endpoints as following：
POST /sapi/v1/asset/dust Dust transfer
POST /sapi/v1/lending/daily/purchase Purchase Savings flexible product
POST /sapi/v1/lending/daily/redeem Redeem Savings flexible product
POST /sapi/v1/lending/customizedFixed/purchase Purchase Savings Fixed/Activity project
POST /sapi/v1/lending/positionChanged Change Savings Fixed/Activity position to Daily position
POST /sapi/v1/bswap/liquidityAdd Bswap add liquidity
POST /sapi/v1/bswap/liquidityRemove Bswap remove liquidity
POST /sapi/v1/bswap/swap Bswap swap
POST /sapi/v1/bswap/claimRewards Bswap claim rewards
2022-1-21

New endpoints for Binance Code:
POST /sapi/v1/giftcard/createCode to create a Binance Code.
POST /sapi/v1/giftcard/redeemCode to redeem a Binance Code.
GET /sapi/v1/giftcard/verify to verify a Binance Code.
2022-1-4

New endpoint for Mining:

GET /sapi/v1/mining/payment/uid to get Mining account earning.
New endpoints for BSwap:

GET /sapi/v1/bswap/unclaimedRewards to get unclaimed rewards record.
POST /sapi/v1/bswap/claimRewards to claim swap rewards or liquidity rewards.
GET /sapi/v1/bswap/claimedHistory to get history of claimed rewards.
2021-12-30

Update endpoint for Margin：

Removed out limit fromGET /sapi/v1/margin/interestRateHistory; The max interval between startTime and endTime is 30 days.
Update endpoint for Wallet：

As the Mining account is merged into Funding account, transfer types MAIN_MINING, MINING_MAIN, MINING_UMFUTURE, MARGIN_MINING, and MINING_MARGIN will be discontinued in Universal Transfer endpoint POST /sapi/v1/asset/transfer on January 05, 2022 08:00 AM UTC
2021-12-29

Removed out dated "Symbol Type" enum; added "Permissions" enum.
2021-12-24

Update endpoints for Sub-Account:
New parameterclientTranIdadded inPOST /sapi/v1/sub-account/universalTransfer and GET /sapi/v1/sub-account/universalTransfer to support custom transfer id
2021-12-03

New endpoints for Margin:

GET /sapi/v1/margin/crossMarginData to get cross margin fee data collection
GET /sapi/v1/margin/isolatedMarginData to get isolated margin fee data collection
GET /sapi/v1/margin/isolatedMarginTier to get isolated margin tier data collection
New endpoints for NFT:

GET /sapi/v1/nft/history/transactions to get NFT transaction history
GET /sapi/v1/nft/history/deposit to get NFT deposit history
GET /sapi/v1/nft/history/withdraw to get NFT withdraw history
GET /sapi/v1/nft/user/getAsset to get NFT asset
2021-11-30

New endpoint for Convert:

GET /sapi/v1/convert/tradeFlow to support user query convert trade history records
New endpoint for Rebate:

GET /sapi/v1/rebate/taxQuery to support user query spot rebate history records
2021-11-19

New endpoint for Pay:

GET /sapi/v1/pay/transactionsto support user query Pay trade history
Update endpoint for Wallet:

New fieldinfoadded inGET /sapi/v1/capital/withdraw/historyto show the reason for withdrawal failure
2021-11-18

The following updates will take effect on November 25, 2021 08:00 AM UTC

Update endpoint for Wallet：
GET /sapi/v1/accountSnapshot
The query time range of both endpoints are shortened to support data query within the last 6 months only, where startTime does not support selecting a timestamp beyond 6 months. If you do not specify startTime and endTime, the data of the last 7 days will be returned by default.

2021-11-17

The following endpoints will be discontinued on November 17, 2021 13:00 PM UTC:
POST /sapi/v1/account/apiRestrictions/ipRestriction to support user enable and disable IP restriction for an API Key
POST /sapi/v1/account/apiRestrictions/ipRestriction/ipList to support user add IP list for an API Key
GET /sapi/v1/account/apiRestrictions/ipRestriction to support user query IP restriction for an API Key
DELETE /sapi/v1/account/apiRestrictions/ipRestriction/ipList to support user delete IP list for an API Key
2021-11-16

New endpoints for Sub-Account:
POST /sapi/v1/sub-account/subAccountApi/ipRestriction to support master account enable and disable IP restriction for a sub-account API Key
POST /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList to support master account add IP list for a sub-account API Key
GET /sapi/v1/sub-account/subAccountApi/ipRestriction to support master account query IP restriction for a sub-account API Key
DELETE /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList to support master account delete IP list for a sub-account API Key
2021-11-09

New endpoints for Wallet:
POST /sapi/v1/account/apiRestrictions/ipRestriction to support user enable and disable IP restriction for an API Key
POST /sapi/v1/account/apiRestrictions/ipRestriction/ipList to support user add IP list for an API Key
GET /sapi/v1/account/apiRestrictions/ipRestriction to support user query IP restriction for an API Key
DELETE /sapi/v1/account/apiRestrictions/ipRestriction/ipList to support user delete IP list for an API Key
2021-11-08

New endpoint for Crypto Loans:
New endpointGET /sapi/v1/loan/incometo support user query crypto loans income history
2021-11-05

Update endpoint for Wallet:
New parameter walletTypeadded in POST /sapi/v1/capital/withdraw/apply to support user choose wallet type spot wallet and funding wallet when withdraw crypto.
2021-11-04

The following updates will take effect on November 11, 2021 08:00 AM UTC

Update endpoints for Wallet and Futures：
GET /sapi/v1/asset/transfer
GET /sapi/v1/futures/transfer
The query time range of both endpoints are shortened to support data query within the last 6 months only, where startTime does not support selecting a timestamp beyond 6 months. If you do not specify startTime and endTime, the data of the last 7 days will be returned by default.

2021-11-01

GET /api/v3/rateLimit/order added
The endpoint will display the user's current order count usage for all intervals.
This endpoint will have a request weight of 20.
2021-10-22

Update endpoint for Wallet:
New transfer types MAIN_FUNDING,FUNDING_MAIN,FUNDING_UMFUTURE,UMFUTURE_FUNDING,MARGIN_FUNDING,FUNDING_MARGIN,FUNDING_CMFUTUREand CMFUTURE_FUNDING added in Universal Transfer endpoint POST /sapi/v1/asset/transfer and GET /sapi/v1/asset/transfer to support transfer assets among funding account and other accounts
As the C2C account, Binance Payment, Binance Card and other business account are merged into a Funding account, transfer types MAIN_C2C,C2C_MAIN,C2C_UMFUTURE,C2C_MINING,UMFUTURE_C2C,MINING_C2C,MARGIN_C2C,C2C_MARGIN,MAIN_PAYand PAY_MAIN will be discontinued in Universal Transfer endpoint POST /sapi/v1/asset/transfer and GET /sapi/v1/asset/transfer on November 04, 2021 08:00 AM UTC
2021-10-14

Update the time range of the response data for the following margin account endpoints, startTime and endTime time span will not exceed 30 days, without time parameter sent the system will return the last 7 days of data by default, while the archived parameter is true, the system will return the last 7 days of data 6 months ago by default:
GET /sapi/v1/margin/transfer
GET /sapi/v1/margin/loan
GET /sapi/v1/margin/repay
GET /sapi/v1/margin/isolated/transfer
GET /sapi/v1/margin/interestHistory
2021-09-18

New endpoints for BSwap:
GET /sapi/v1/bswap/poolConfigure to get pool configure
GET /sapi/v1/bswap/addLiquidityPreview to get add liquidity preview
GET /sapi/v1/bswap/removeLiquidityPreview to get remove liquidity preview
2021-09-17

Add/api/*and/sapi/* limit introduction in General Info
2021-09-08

Add endpoints for enabled isolated margin account limit:

DELETE /sapi/v1/margin/isolated/account to disable isolated margin account for a specific symbol
POST /sapi/v1/margin/isolated/account to enable isolated margin account for a specific symbol
GET /sapi/v1/margin/isolated/accountLimit to query enabled isolated margin account limit
New field "enabled" in response of GET /sapi/v1/margin/isolated/account to check if the isolated margin account is enabled

2021-09-03

Update endpoint for Wallet:
New fields sameAddress,depositDust and specialWithdrawTipsadded in GET /sapi/v1/capital/config/getall sameAddress means if the coin needs to provide memo to withdraw depositDust means minimum creditable amount specialWithdrawTips means special tips for withdraw
New field confirmNoadded in GET /sapi/v1/capital/withdraw/history to support query confirm times for withdraw history
2021-08-27

Update endpoint for Wallet:
New parameter withdrawOrderIdadded in GET /sapi/v1/capital/withdraw/history to support user query withdraw history by withdrawOrderId
New field unlockConfirmadded in GET /sapi/v1/capital/deposit/hisrec to support query network confirm times for unlocking
2021-08-23

New endpoints for Margin Account OCO:
POST /sapi/v1/margin/order/oco
DELETE /sapi/v1/margin/orderList
GET /sapi/v1/margin/orderList
GET /sapi/v1/margin/allOrderList
GET /sapi/v1/margin/openOrderList
Same usage as spot account OCO

2021-08-20

Update endpoint for Wallet:
New parametersfromSymbol,toSymboland new transfer types ISOLATEDMARGIN_MARGIN, MARGIN_ISOLATEDMARGINand ISOLATEDMARGIN_ISOLATEDMARGIN added in POST /sapi/v1/asset/transfer and GET /sapi/v1/asset/transfer to support user transfer assets between Margin(cross) account and Margin(isolated) account
2021-08-12

GET api/v3/myTrades has a new optional field orderId
2021-08-05

New endpoint for C2C:
GET /sapi/v1/c2c/orderMatch/listUserOrderHistory to query user C2C trade history
2021-08-05

Update endpoints for Savings:
GET /sapi/v1/lending/union/purchaseRecord
GET /sapi/v1/lending/union/redemptionRecord
GET /sapi/v1/lending/union/interestHistory
The time between startTime and endTime cannot be longer than 30 days. If startTime and endTime are both not sent, then the last 30 days' data will be returned

2021-07-29

Update endpoint for Sub-Account:
GET /sapi/v1/sub-account/transfer/subUserHistory if startTimeandendTimeare not sent, the recent 30-day data will be returned by default
2021-07-27

New endpoint for Fiat:
GET /sapi/v1/fiat/orders to query user fiat deposit and withdraw history
GET /sapi/v1/fiat/payments to query user fiat payments history
2021-07-16

New endpoint for Wallet:
GET /sapi/v1/account/apiRestrictions to query user API Key permission
2021-07-09

New endpoint for Wallet:
POST /sapi/v1/asset/get-funding-asset to query funding wallet, includes Binance Pay, Binance Card, Binance Gift Card, Stock Token
2021-06-24

Update endpoints for Wallet:
GET /sapi/v1/capital/withdraw/history added default value 1000, max value 1000 for the parameterlimit
GET /sapi/v1/capital/deposit/hisrec added default value 1000, max value 1000 for the parameterlimit
2021-06-17

Update endpoint for Savings:
GET /sapi/v1/lending/daily/product/list to include new parameters current and size
2021-06-15

New endpoints for Sub-Account:
POST /sapi/v1/managed-subaccount/deposit to deposit assets into the managed sub-account (only for investor master account)
GET /sapi/v1/managed-subaccount/asset to query managed sub-account asset details (only for investor master account)
POST /sapi/v1/managed-subaccount/withdraw to withdrawal assets from the managed sub-account (only for investor master account)
2021-06-04

On August 01, 2021 02:00 AM UTC the WAPI endpoints will be discontinued:

GET /wapi/v3/systemStatus.html
POST /wapi/v3/withdraw.html
GET /wapi/v3/depositHistory.html
GET /wapi/v3/withdrawHistory.html
GET /wapi/v3/depositAddress.html
GET /wapi/v3/accountStatus.html
GET /wapi/v3/apiTradingStatus.html
GET /wapi/v3/userAssetDribbletLog.html
GET /wapi/v3/assetDetail.html
GET /wapi/v3/tradeFee.html
GET /wapi/v3/sub-account/list.html
GET /wapi/v3/sub-account/transfer/history.html
POST /wapi/v3/sub-account/transfer.html
GET /wapi/v3/sub-account/assets.html
The WAPI endpoints have been removed from Binance API Documentation.To ensure your trading strategies are not affected, all API users are encouraged to upgrade trading bots to SAPI endpoints as soon as possible.

2021-05-26

Update endpoint for Wallet:
New transfer types MAIN_PAY ,PAY_MAIN added in Universal Transfer endpoint POST /sapi/v1/asset/transfer and GET /sapi/v1/asset/transfer to support trasnfer assets between spot account and pay account
2021-05-12

Added Data Source in the documentation to explain where each endpoint is retrieving its data
Added field Data Source to each Spot API endpoint in the documentation
GET api/v3/exchangeInfo now supports single or multi-symbol query
2021-04-28

On May 15, 2021 08:00 UTC the SAPI Create Margin Account endpoint will be discontinued:

POST /sapi/v1/margin/isolated/create
Isolated Margin account creation and trade preparation can be completed directly through Isolated Margin funds transfer POST /sapi/v1/margin/isolated/transfer

2021-04-26

On April 28, 2021 00:00 UTC the weights to the following endpoints will be adjusted:

GET /api/v3/order weight increased to 2
GET /api/v3/openOrders weight increased to 3
GET /api/v3/allOrders weight increased to 10
GET /api/v3/orderList weight increased to 2
GET /api/v3/openOrderList weight increased to 3
GET /api/v3/account weight increased to 10
GET /api/v3/myTrades weight increased to 10
GET /api/v3/exchangeInfo weight increased to 10
2021-04-08

Update endpoint for Sub-Account:
GET /sapi/v1/sub-account/futures/accountSummary and GET /sapi/v2/sub-account/futures/accountSummary the unit of field asset changed to USD valued summary of sub-account assets
2021-04-02

New endpoints for Wallet:
GET /sapi/v1/system/status to query system status
GET /sapi/v1/account/status to query account status
GET /sapi/v1/account/apiTradingStatus to query account API trading status
GET /sapi/v1/asset/dribblet to query dust log
GET /sapi/v1/asset/assetDetail to query asset detail
GET /sapi/v1/asset/tradeFee to query trade fee
New endpoint for Sub-Account:
GET /sapi/v3/sub-account/assets to query sub-account assets
2021-04-01

Update endpoint for Sub-Account:
GET /sapi/v1/sub-account/transfer/subUserHistory new fields fromAccountType and toAccountType added in response
2021-03-31

Update endpoint for Sub-Account:
GET /wapi/v3/sub-account/transfer/history.html added new parameters fromEmail and toEmail, the original parameteremail is equal tofromEmailby default
2021-03-08

New endpoint for Sub-Account:
POST /sapi/v1/sub-account/virtualSubAccount to support create a virtual sub-account
GET /sapi/v1/sub-account/list to support query sub-account list
POST /sapi/v1/sub-account/blvt/enable to support enable blvt for sub-account
2021-03-05

New endpoints for Margin:
GET /sapi/v1/margin/interestRateHistory to support margin interest rate history query
2021-02-08

New endpoints for Futures:
GET /sapi/v2/futures/loan/wallet to support BUSD loan query
GET /sapi/v2/futures/loan/configs to support BUSD loan query
GET /sapi/v2/futures/loan/calcAdjustLevel to support BUSD loan
GET /sapi/v2/futures/loan/calcMaxAdjustAmount to support adjustment of BUSD loan
POST /sapi/v2/futures/loan/adjustCollateral to support adjustment of BUSD loan
Update endpoints for Futures
GET /sapi/v1/futures/loan/adjustCollateral/history new parameter and fields in response loanCoin for BUSD loan
GET /sapi/v1/futures/loan/liquidationHistory new parameter and fields in response loanCoin for BUSD loan
2021-02-04

New transfer types MARGIN_MINING ,MINING_MARGIN, MARGIN_C2C ,C2C_MARGIN, MARGIN_CMFUTURE, CMFUTURE_MARGIN added in Universal Transfer endpoint POST /sapi/v1/asset/transfer and GET /sapi/v1/asset/transfer.
2021-01-15

New endpoint DELETE /sapi/v1/margin/openOrders for Margin Trade
This will allow a user to cancel all open orders on a single symbol for margin account.
This endpoint will cancel all open orders including OCO orders for margin account.
2021-01-10

New parameter pageSize for Mining endpoint GET /sapi/v1/mining/payment/list
New fields in response to Mining endpoint GET /sapi/v1/mining/payment/list:

"type" for income type
"hashTransfer" for resale Hashrate
"transferAmount" for transferred Income
New Mining endpoints:

GET /sapi/v1/mining/payment/other
GET /sapi/v1/mining/hash-transfer/config/details
GET /sapi/v1/mining/hash-transfer/config/details/list
GET /sapi/v1/mining/hash-transfer/profit/details
POST /sapi/v1/mining/hash-transfer/config
POST /sapi/v1/mining/hash-transfer/config/cancel
2021-01-01

USER DATA STREAM

outboundAccountInfo has been removed.
2020-12-30

New endpoint for Wallet:
POST /sapi/v1/asset/transfer to support user universal transfer among Spot, Margin, Futures, C2C, MINING accounts.
GET /sapi/v1/asset/transfer to get user universal transfer history.
2020-12-22

New endpoint for Sub-Account:
GET /sapi/v1/sub-account/sub/transfer/history to get spot asset transfer history.
2020-12-11

Update endpoints for Futures Cross-Collateral:
GET /sapi/v1/futures/loan/wallet new fields in response interestFreeLimit for total interest free limit, interestFreeLimitUsed for interest free limit used.
GET /sapi/v1/futures/loan/interestHistory new fields in response interestFreeLimitUsed for interest free limit used.
2020-12-04

Update endpoint for BLVT:

GET /sapi/v1/blvt/tokenInfo new fields in response currentBaskets(include symbol, amount , notionalValue ),purchaseFeePct,dailyPurchaseLimit,redeemFeePct,dailyRedeemLimit.
New endpoint for BLVT:

GET /sapi/v1/blvt/userLimit to get BLVT user limit info.
2020-12-02

New endpoints for Sub-Account:
GET /sapi/v2/sub-account/futures/account to get detail on sub-account's USDT margined futures account and COIN margined futures account.
GET /sapi/v2/sub-account/futures/accountSummary to get summary of sub-account's USDT margined futures account and COIN margined futures account.
GET /sapi/v2/sub-account/futures/positionRisk to get position risk of sub-account's USDT margined futures account and COIN margined futures account.
2020-12-01

Update Margin Trade Endpoint:
POST /sapi/v1/margin/order new parameter quoteOrderQty allow a user to specify the total quoteOrderQty spent or received in the MARKET order.
2020-11-27

New API clusters have been added in order to improve performance.

Users can access any of the following API clusters, in addition to api.binance.com

If there are any performance issues with accessing api.binance.com please try any of the following instead:

https://api1.binance.com/api/v3/*
https://api2.binance.com/api/v3/*
https://api3.binance.com/api/v3/*
2020-11-16

Updated endpoints for Margin, new parameter archived to query data from 6 months ago:
GET /sapi/v1/margin/loan
GET /sapi/v1/margin/repay
GET /sapi/v1/margin/interestHistory
2020-11-13

New endpoints for Sub-Account:
POST /sapi/v1/sub-account/universalTransfer to transfer spot and futures asset between master account and sub accounts.
GET /sapi/v1/sub-account/universalTransfer to search transfer records.
2020-11-10

New endpoint to toggle BNB Burn:
POST /sapi/v1/bnbBurn to toggle BNB Burn on spot trade and margin interest.
GET /sapi/v1/bnbBurn to get BNB Burn status.
2020-11-09

New field tranId is available from endpoints:
GET /sapi/v1/sub-account/futures/internalTransfer
GET /sapi/v1/sub-account/transfer/subUserHistory
2020-11-03

Update endpoints for Futures Cross-Collateral:

GET /sapi/v1/futures/loan/repay/history new fields in response repayType(NORMAL for normal repayment, COLLATERAL for collateral repayment), price (collateral repayment rate), repayCollateral(collateral amount for collateral repayment).
GET /sapi/v1/futures/loan/wallet new fields in response totalInterest (total interest for cross-collateral), principalForInterest(cross-collateral principal for interest), interest(cross-collateral interest).
GET /sapi/v1/futures/loan/configs new fields in response interestRate (interest rate for cross-collateral), interestGracePeriod (interest grace period for cross-collateral).
New endpoints for Futures Cross-Collateral:

GET /sapi/v1/futures/loan/collateralRepayLimit to check the maximum and minimum limit when repay with collateral.
GET /sapi/v1/futures/loan/collateralRepay to get quote for collateral repayment.
POST /sapi/v1/futures/loan/collateralRepay to repay with collateral.
GET /sapi/v1/futures/loan/collateralRepayResult to check collateral repayment result.
GET /sapi/v1/futures/loan/interestHistory to get cross-collateral interest history.
2020-10-14

Update endpoints for Futures Cross-Collateral:
POST /sapi/v1/futures/loan/borrow and GET /sapi/v1/futures/loan/borrow/history new field borrowId in response for ID of Cross-Collateral borrow operation.
POST /sapi/v1/futures/loan/repay and GET /sapi/v1/futures/loan/repay/history new field repayId in response for ID of Cross-Collateral repay operation.
2020-10-10

New type added in the endpoint POST /sapi/v1/sub-account/futures/transferto support transfer asset from subaccount's spot account to its COIN-margined futures account and transfer asset from subaccount's COIN-margined futures account to its spot account.
2020-09-30

Update endpoints for Margin Account:
GET /sapi/v1/margin/maxBorrowable new field borrowLimit in response for account borrow limit.
2020-09-28

New endpoints for Binance Savings:
POST /sapi/v1/lending/positionChanged to change fixed/activity position to daily position.
New parameter ACTIVITY replace REGULARin the following Binance Savings endpoints:
GET /sapi/v1/lending/project/list
POST /sapi/v1/lending/customizedFixed/purchase
GET /sapi/v1/lending/project/position/list
GET /sapi/v1/lending/union/purchaseRecord
GET /sapi/v1/lending/union/interestHistory
2020-09-23

New SAPI endpoints for BSwap:
GET /sapi/v1/bswap/pools to list all swap pools.
GET /sapi/v1/bswap/liquidity to get liquidity information of a pool.
POST /sapi/v1/bswap/liquidityAdd to add liquidity.
POST /sapi/v1/bswap/liquidityRemove to remove liquidity.
GET /sapi/v1/bswap/liquidityOps to get liquidity operation record.
GET /sapi/v1/bswap/quote to request quotes.
POST /sapi/v1/bswap/swap to swap.
GET /sapi/v1/bswap/swap to get swap history.
2020-09-16

New SAPI endpoints for BLVT:

GET /sapi/v1/blvt/tokenInfo to get BLVT info.
POST /sapi/v1/blvt/subscribe (HMAC SHA256) to subscribe BLVT.
GET /sapi/v1/blvt/subscribe/record (HMAC SHA256) to get subscription record。
POST /sapi/v1/blvt/redeem (HMAC SHA256) to redeem BLVT.
GET /sapi/v1/blvt/redeem/record (HMAC SHA256 to get redemption record.
The BLVT NAV system is working relatively with Binance Futures, so some endpoints are based on futures system:

New endpoint to get historical BLVT Kline.
New WebSocket streams for BLVT Info and BLVT NAV Kline:
2020-09-09

USER DATA STREAM

outboundAccountInfo has been deprecated.
outboundAccountInfo will be removed in the future. (Exact date unknown) Please use outboundAccountPosition instead.
outboundAccountInfo will now only show the balance of non-zero assets and assets that have been reduced to 0.
2020-09-03

New endpoint POST /sapi/v1/sub-account/futures/internalTransfer to transfer futures asset between master account and subaccount.
New endpointGET /sapi/v1/sub-account/futures/internalTransfer to get futures transfer history of subaccount.
2020-09-01

New parameter masterAccountTotalAsset added in the endpoint GET /sapi/v1/sub-account/spotSummary to get BTC valued asset summary of master account.
2020-08-27

New endpoint GET /sapi/v1/sub-account/spotSummary to get BTC valued asset summary of subaccout.
2020-08-26

New parameter symbols added in the endpoint GET /sapi/v1/margin/isolated/account.
2020-07-28

ISOLATED MARGIN

New parameters "isIsolated" and "symbol" added for isolated margin in the following endpoints:

POST /sapi/v1/margin/loan
POST /sapi/v1/margin/repay
New parameter "isIsolated" and new response field "isIsolated" added for isolated margin in the following endpoints:

POST /sapi/v1/margin/order
DELETE /sapi/v1/margin/order
GET /sapi/v1/margin/order
GET /sapi/v1/margin/openOrders
GET /sapi/v1/margin/allOrders
GET /sapi/v1/margin/myTrades
New parameter "isolatedSymbol" and new response field "isolatedSymbol" added for isolated margin in the following endpoints:

GET /sapi/v1/margin/loan
GET /sapi/v1/margin/repay
GET /sapi/v1/margin/interestHistory
New parameter "isolatedSymbol" and new response field "isIsolated" added for isolated margin in the following endpoint GET /sapi/v1/margin/forceLiquidationRec

New parameter "isolatedSymbol" added for isolated margin in the following endpoints:

GET /sapi/v1/margin/maxBorrowable
GET /sapi/v1/margin/maxTransferable
New endpoints for isolated margin:

POST /sapi/v1/margin/isolated/create
POST /sapi/v1/margin/isolated/transfer
GET /sapi/v1/margin/isolated/transfer
GET /sapi/v1/margin/isolated/account
GET /sapi/v1/margin/isolated/pair
GET /sapi/v1/margin/isolated/allPairs
New endpoints for listenKey management of isolated margin account:

POST /sapi/v1/userDataStream/isolated
PUT /sapi/v1/userDataStream/isolated
DELETE /sapi/v1/userDataStream/isolated
2020-07-20

The max value of parameter "limit" in GET /sapi/v1/margin/allOrders has been changed as 500.
2020-07-17

There is now a request limit specifically for the sapi/v1/margin/allOrders endpoint at 60 raw requests per minute for a single IP address.
2020-07-13

New SAPI Endpoints for futures Cross-Collateral:
POST /sapi/v1/futures/loan/borrow
GET /sapi/v1/futures/loan/borrow/history
POST /sapi/v1/futures/loan/repay
GET /sapi/v1/futures/loan/repay/history
GET /sapi/v1/futures/loan/wallet
GET /sapi/v1/futures/loan/configs
GET /sapi/v1/futures/loan/calcAdjustLevel
GET /sapi/v1/futures/loan/calcMaxAdjustAmount
POST /sapi/v1/futures/loan/adjustCollateral
GET /sapi/v1/futures/loan/adjustCollateral/history
GET /sapi/v1/futures/loan/liquidationHistory
2020-06-28

SAPI Endpoints for futures:
POST /sapi/v1/futures/transfer
GET /sapi/v1/futures/transfer
2020-05-06

New endpoints for Mining:
GET /sapi/v1/mining/pub/algoList
GET /sapi/v1/mining/pub/coinList
GET /sapi/v1/mining/worker/detail
GET /sapi/v1/mining/worker/list
GET /sapi/v1/mining/payment/list
GET /sapi/v1/mining/statistics/user/status
GET /sapi/v1/mining/statistics/user/list
2020-05-03

New request limit for some margin endpoints
Changes on these endpoints:
POST /sapi/v1/margin/transfer
POST /sapi/v1/margin/loan
POST /sapi/v1/margin/repay
Limit to 1 every 2 seconds。
Request beyond the limit will receive HTTP status code 429。
2020-05-01

From 2020-05-01 UTC 00:00, all symbols will have a limit of 200 open orders using the MAX_NUM_ORDERS filter.
No existing orders will be removed or canceled.
Accounts that have 200 or more open orders on a symbol will not be able to place new orders on that symbol until the open order count is below 200.
OCO orders count as 2 open orders before the LIMIT order is touched or the STOP_LOSS (or STOP_LOSS_LIMIT) order is triggered; once this happens the other order is canceled and will no longer count as an open order.
2020-04-25

SPOT API

New field permissions
Defines the trading permissions that are allowed on accounts and symbols.
permissions is an enum array; values:
SPOT
MARGIN
permissions will replace isSpotTradingAllowed and isMarginTradingAllowed on GET api/v3/exchangeInfo in future API versions (v4+).
For an account to trade on a symbol, the account and symbol must share at least 1 permission in common.
Updates to GET api/v3/exchangeInfo
New field permissions added.
New field quoteAssetPrecision added; a duplicate of the quotePrecision field. quotePrecision will be removed in future API versions (v4+).
Updates to GET api/v3/account
New field permissions added.
New endpoint DELETE api/v3/openOrders
This will allow a user to cancel all open orders on a single symbol.
This endpoint will cancel all open orders including OCO orders.
Orders can be canceled via the API on symbols in the BREAK or HALT status.
USER DATA STREAM

OutboundAccountInfo has new field P which shows the trading permissions of the account.
2020-04-23

WEB SOCKET STREAM

WebSocket connections have a limit of 5 incoming messages per second. A message is considered:
A PING frame
A PONG frame
A JSON control message (e.g. subscribe, unsubscribe)
A connection that goes beyond the limit will be disconnected; IPs that are repeatedly disconnected may be banned.
A single connection can listen to a maximum of 1024 streams.
2020-04-16

New fields in response to endpointGET /sapi/v1/lending/daily/token/position：

todayPurchasedAmount for user's purchased amount today
New lending endpoints for customized fixed projects:

GET /sapi/v1/lending/project/list
POST /sapi/v1/lending/customizedFixed/purchase
GET /sapi/v1/lending/project/position/list
2020-04-02

New fields in response to endpointGET /sapi/v1/capital/config/getall：
minConfirm for min number for balance confirmation
unLockConfirm for confirmation number for balance unlock
2020-03-24

MAX_POSITION filter added.

This filter defines the allowed maximum position an account can have on the base asset of a symbol. An account's position defined as the sum of the account's:
free balance of the base asset
locked balance of the base asset
sum of the qty of all open BUY orders
BUY orders will be rejected if the account's position is greater than the maximum position allowed.
2020-03-13

New parameter transactionFeeFlag is available in endpoint:
POST /sapi/v1/capital/withdraw/apply and
POST /wapi/v3/withdraw.html
2020-02-05

New sub account endpoints:
POST /sapi/v1/sub-account/futures/transfer to transfer between futures and spot accout of sub-account.
POST /sapi/v1/sub-account/margin/transfer to transfer between margin and spot accout of sub-account.
POST /sapi/v1/sub-account/transfer/subToSub to transfer to another account by sub-account.
POST /sapi/v1/sub-account/transfer/subToMaster to transfer to same master by sub-account.
GET /sapi/v1/sub-account/transfer/subUserHistory to get transfer history of sub-account.
2020-01-15

New parameter withdrawOrderId for client customized withdraw id for endpoint POST /wapi/v3/withdraw.html.

New field withdrawOrderId in response to GET /wapi/v3/withdrawHistory.html

2019-12-25

New endpoints for Binance Savings:

GET /sapi/v1/lending/daily/product/list
GET /sapi/v1/lending/daily/userLeftQuota
POST /sapi/v1/lending/daily/purchase
GET /sapi/v1/lending/daily/userRedemptionQuota
POST /sapi/v1/lending/daily/redeem
GET /sapi/v1/lending/daily/token/position
GET /sapi/v1/lending/union/account
GET /sapi/v1/lending/union/purchaseRecord
GET /sapi/v1/lending/union/redemptionRecord
GET /sapi/v1/lending/union/interestHistory
Added time interval limit in
GET /sapi/v1/capital/withdraw/history,
GET /wapi/v3/withdrawHistory.html,
GET /sapi/v1/capital/deposit/hisrec and
GET /wapi/v3/depositHistory.html:

The default startTime is 90 days from current time, and the default endTime is current time.
Please notice the default startTime and endTime to make sure that time interval is within 0-90 days.
If both startTime and endTime are sent, time between startTime and endTime must be less than 90 days.
2019-12-18

New endpoint to get daily snapshot of account:
GET /sapi/v1/accountSnapshot
2019-11-30

Added parameter sideEffectType in POST /sapi/v1/margin/order (HMAC SHA256) with enums:

NO_SIDE_EFFECT for normal trade order;
MARGIN_BUY for margin trade order;
AUTO_REPAY for making auto repayment after order filled.
New field marginBuyBorrowAmount and marginBuyBorrowAsset in FULL response to POST /sapi/v1/margin/order (HMAC SHA256)

2019-11-28

New SAPI endpont to disable fast withdraw switch:
POST /sapi/v1/account/disableFastWithdrawSwitch (HMAC SHA256)
New SAPI endpont to enable fast withdraw switch:
POST /sapi/v1/account/enableFastWithdrawSwitch (HMAC SHA256)
2019-11-22

Quote Order Qty Market orders have been enabled on all symbols.
Quote Order Qty MARKET orders allow a user to specify the total quoteOrderQty spent or received in the MARKET order.
Quote Order Qty MARKET orders will not break LOT_SIZE filter rules; the order will execute a quantity that will have the notional value as close as possible to quoteOrderQty.
Using BNBBTC as an example:
On the BUY side, the order will buy as many BNB as quoteOrderQty BTC can.
On the SELL side, the order will sell as much BNB as needed to receive quoteOrderQty BTC.
2019-11-19

GET /sapi/v1/sub-account/margin/account has new field: marginTradeCoeffVo which contains
forceLiquidationBar for liquidation margin ratio
marginCallBar for margin call margin ratio
normalBar for initial margin ratio
2019-11-13

Rest API

api/v3/exchangeInfo has new fields:
quoteOrderQtyMarketAllowed
baseCommissionPrecision
quoteCommissionPrecision
MARKET orders have a new optional field: quoteOrderQty used to specify the quote quantity to BUY or SELL. This cannot be used in combination with quantity.
The exact timing that quoteOrderQty MARKET orders will be enabled is TBD. There will be a separate announcement and further details at that time.
All order query endpoints will return a new field origQuoteOrderQty in the JSON payload. (e.g. GET api/v3/allOrders)
    {
      "code": -1128,
      "msg": "Combination of optional parameters invalid. Recommendation: 'stopLimitTimeInForce' should also be sent."
    }
Updated error messages for -1128

Sending an OCO with a stopLimitPrice but without a stopLimitTimeInForce will return the error:
Updated error messages for -1003 to specify the limit is referring to the request weight, not to the number of requests.

Deprecation of v1 endpoints:

By end of Q1 2020, the following endpoints will be removed from the API. The documentation has been updated to use the v3 versions of these endpoints.

GET api/v1/depth
GET api/v1/historicalTrades
GET api/v1/aggTrades
GET api/v1/klines
GET api/v1/ticker/24hr
GET api/v1/ticker/price
GET api/v1/exchangeInfo
POST api/v1/userDataStream
PUT api/v1/userDataStream
GET api/v1/ping
GET api/v1/time
GET api/v1/ticker/bookTicker
These endpoints however, will NOT be migrated to v3. Please use the following endpoints instead moving forward.

Old V1 Endpoints	New V3 Endpoints
GET api/v1/ticker/allPrices	GET api/v3/ticker/price
GET api/v1/ticker/allBookTickers	GET api/v3/ticker/bookTicker
USER DATA STREAM

Changes toexecutionReport event

If the C field is empty, it will now properly return null, instead of "null".
New field Q which represents the quoteOrderQty.
balanceUpdate event type added

This event occurs when funds are deposited or withdrawn from your account.
WEB SOCKET STREAM

WSS now supports live subscribing/unsubscribing to streams.
2019-11-08

New sapi for subaccount management on margin and futures:
GET /sapi/v1/sub-account/status (HMAC SHA256)
POST /sapi/v1/sub-account/margin/enable (HMAC SHA256)
GET /sapi/v1/sub-account/margin/account (HMAC SHA256)
GET /sapi/v1/sub-account/margin/accountSummary (HMAC SHA256)
POST /sapi/v1/sub-account/futures/enable (HMAC SHA256)
GET /sapi/v1/sub-account/futures/account (HMAC SHA256)
GET /sapi/v1/sub-account/futures/accountSummary (HMAC SHA256)
GET /sapi/v1/sub-account/futures/positionRisk (HMAC SHA256)
2019-11-04

New sapi endpoints for subaccount wallet.
GET /sapi/v1/capital/deposit/subAddress (HMAC SHA256)): fetch subaccount deposit address.
GET /sapi/v1/capital/deposit/subHisrec (HMAC SHA256)): fetch subaccount deposit history.
2019-10-29

New sapi endpoints for wallet.
POST /sapi/v1/capital/withdraw/apply (HMAC SHA256): withdraw.
Get /sapi/v1/capital/withdraw/history (HMAC SHA256): fetch withdraw history with network.
2019-10-14

New sapi endpoints for wallet.
GET /sapi/v1/capital/config/getall (HMAC SHA256): get all coins' information for user.
GET /sapi/v1/capital/deposit/hisrec (HMAC SHA256): fetch deposit history with network.
GET /sapi/v1/capital/deposit/address (HMAC SHA256): fetch deposit address with network.
2019-10-11

Added parameter network in POST /wapi/v3/withdraw.html so that asset can be withdrawed with specific network.
2019-09-09

New WebSocket streams for bookTickers added: <symbol>@bookTicker and !bookTicker.
2019-09-03

Faster order book data with 100ms updates: <symbol>@depth@100ms and <symbol>@depth#@100ms
Added "Update Speed:" to Websocket Market Streams
Removed deprecated v1 endpoints as per previous announcement:
GET api/v1/order
GET api/v1/openOrders
POST api/v1/order
DELETE api/v1/order
GET api/v1/allOrders
GET api/v1/account
GET api/v1/myTrades
2019-08-16

GET api/v1/depth limit of 10000 has been temporarily removed

In Q4 2017, the following endpoints were deprecated and removed from the API documentation. They have been permanently removed from the API as of this version. We apologize for the omission from the original changelog:

GET api/v1/order
GET api/v1/openOrders
POST api/v1/order
DELETE api/v1/order
GET api/v1/allOrders
GET api/v1/account
GET api/v1/myTrades
Streams, endpoints, parameters, payloads, etc. described in the documents in this repository are considered official and supported. The use of any other streams, endpoints, parameters, or payloads, etc. is not supported; use them at your own risk and with no guarantees.

2019-09-15

Rest API

New order type: OCO ("One Cancels the Other")

An OCO has 2 orders: (also known as legs in financial terms)
STOP_LOSS or STOP_LOSS_LIMIT leg
LIMIT_MAKER leg
Price Restrictions:
SELL Orders : Limit Price > Last Price > Stop Price
BUY Orders : Limit Price < Last Price < Stop Price
As stated, the prices must "straddle" the last traded price on the symbol. EX: If the last price is 10:
A SELL OCO must have the limit price greater than 10, and the stop price less than 10.
A BUY OCO must have a limit price less than 10, and the stop price greater than 10.
Quantity Restrictions:
Both legs must have the same quantity.
ICEBERG quantities however, do not have to be the same.
Execution Order:
If the LIMIT_MAKER is touched, the limit maker leg will be executed first BEFORE canceling the Stop Loss Leg.
if the Market Price moves such that the STOP_LOSS or STOP_LOSS_LIMIT will trigger, the Limit Maker leg will be cancelled BEFORE executing the STOP_LOSS Leg.
Cancelling an OCO
Cancelling either order leg will cancel the entire OCO.
The entire OCO can be canceled via the orderListId or the listClientOrderId.
New Enums for OCO:
ListStatusType
RESPONSE - used when ListStatus is responding to a failed action. (either order list placement or cancellation)
EXEC_STARTED - used when an order list has been placed or there is an update to a list's status.
ALL_DONE - used when an order list has finished executing and is no longer active.
ListOrderStatus
EXECUTING - used when an order list has been placed or there is an update to a list's status.
ALL_DONE - used when an order list has finished executing and is no longer active.
REJECT - used when ListStatus is responding to a failed action. (either order list placement or cancellation)
ContingencyType
OCO - specifies the type of order list.
New Endpoints:
POST api/v3/order/oco
DELETE api/v3/orderList
GET api/v3/orderList
recvWindow cannot exceed 60000.

New intervalLetter values for headers:

SECOND => S
MINUTE => M
HOUR => H
DAY => D
New Headers X-MBX-USED-WEIGHT-(intervalNum)(intervalLetter) will give your current used request weight for the (intervalNum)(intervalLetter) rate limiter. For example, if there is a one minute request rate weight limiter set, you will get a X-MBX-USED-WEIGHT-1M header in the response. The legacy header X-MBX-USED-WEIGHT will still be returned and will represent the current used weight for the one minute request rate weight limit.

New Header X-MBX-ORDER-COUNT-(intervalNum)(intervalLetter)that is updated on any valid order placement and tracks your current order count for the interval; rejected/unsuccessful orders are not guaranteed to have X-MBX-ORDER-COUNT-** headers in the response.

Eg. X-MBX-ORDER-COUNT-1S for "orders per 1 second" and X-MBX-ORDER-COUNT-1D for orders per "one day"
GET api/v1/depth now supports limit 5000 and 10000; weights are 50 and 100 respectively.

GET api/v1/exchangeInfo has a new parameter ocoAllowed.

USER DATA STREAM

executionReport event now contains "g" which has the orderListId; it will be set to -1 for non-OCO orders.
New Event Type listStatus; listStatus is sent on an update to any OCO order.
New Event Type outboundAccountPosition; outboundAccountPosition is sent any time an account's balance changes and contains the assets that could have changed by the event that generated the balance change (a deposit, withdrawal, trade, order placement, or cancelation).
NEW ERRORS

-1131 BAD_RECV_WINDOW
recvWindow must be less than 60000
-1099 Not found, authenticated, or authorized
This replaces error code -1999
NEW -2011 ERRORS

OCO_BAD_ORDER_PARAMS
A parameter for one of the orders is incorrect.
OCO_BAD_PRICES
The relationship of the prices for the orders is not correct.
UNSUPPORTED_ORD_OCO
OCO orders are not supported for this symbol.
2019-03-12

Rest API

X-MBX-USED-WEIGHT header added to Rest API responses.
Retry-After header added to Rest API 418 and 429 responses.
When canceling the Rest API can now return errorCode -1013 OR -2011 if the symbol's status isn't TRADING.
api/v1/depth no longer has the ignored and empty [].
api/v3/myTrades now returns quoteQty; the price * qty of for the trade.
Websocket streams

<symbol>@depth and <symbol>@depthX streams no longer have the ignored and empty [].
System improvements

Matching Engine stability/reliability improvements.
Rest API performance improvements.
2018-11-13

Rest API

Can now cancel orders through the Rest API during a trading ban.
New filters: PERCENT_PRICE, MARKET_LOT_SIZE, MAX_NUM_ICEBERG_ORDERS.
Added RAW_REQUESTS rate limit. Limits based on the number of requests over X minutes regardless of weight.
/api/v3/ticker/price increased to weight of 2 for a no symbol query.
/api/v3/ticker/bookTicker increased weight of 2 for a no symbol query.
DELETE /api/v3/order will now return an execution report of the final state of the order.
MIN_NOTIONAL filter has two new parameters: applyToMarket (whether or not the filter is applied to MARKET orders) and avgPriceMins (the number of minutes over which the price averaged for the notional estimation).
intervalNum added to /api/v1/exchangeInfo limits. intervalNum describes the amount of the interval. For example: intervalNum 5, with interval minute, means "every 5 minutes".
Explanation for the average price calculation:

(qty * price) of all trades / sum of qty of all trades over previous 5 minutes.

If there is no trade in the last 5 minutes, it takes the first trade that happened outside of the 5min window. For example if the last trade was 20 minutes ago, that trade's price is the 5 min average.

If there is no trade on the symbol, there is no average price and market orders cannot be placed. On a new symbol with applyToMarket enabled on the MIN_NOTIONAL filter, market orders cannot be placed until there is at least 1 trade.

The current average price can be checked here: https://api.binance.com/api/v3/avgPrice?symbol=<symbol> For example: https://api.binance.com/api/v3/avgPrice?symbol=BNBUSDT

User data stream

Last quote asset transacted quantity (as variable Y) added to execution reports. Represents the lastPrice * lastQty (L * l).
2018-07-18

Rest API

New filter: ICEBERG_PARTS
POST api/v3/order new defaults for newOrderRespType. ACK, RESULT, or FULL; MARKET and LIMIT order types default to FULL, all other orders default to ACK.
POST api/v3/order RESULT and FULL responses now have cummulativeQuoteQty
GET api/v3/openOrders with no symbol weight reduced to 40.
GET api/v3/ticker/24hr with no symbol weight reduced to 40.
Max amount of trades from GET /api/v1/trades increased to 1000.
Max amount of trades from GET /api/v1/historicalTrades increased to 1000.
Max amount of aggregate trades from GET /api/v1/aggTrades increased to 1000.
Max amount of aggregate trades from GET /api/v1/klines increased to 1000.
Rest API Order lookups now return updateTime which represents the last time the order was updated; time is the order creation time.
Order lookup endpoints will now return cummulativeQuoteQty. If cummulativeQuoteQty is < 0, it means the data isn't available for this order at this time.
REQUESTS rate limit type changed to REQUEST_WEIGHT. This limit was always logically request weight and the previous name for it caused confusion.
User data stream

cummulativeQuoteQty field added to order responses and execution reports (as variable Z). Represents the cummulative amount of the quote that has been spent (with a BUY order) or received (with a SELL order). Historical orders will have a value < 0 in this field indicating the data is not available at this time. cummulativeQuoteQty divided by cummulativeQty will give the average price for an order.
O (order creation time) added to execution reports
2018-01-23

GET /api/v1/historicalTrades weight decreased to 5
GET /api/v1/aggTrades weight decreased to 1
GET /api/v1/klines weight decreased to 1
GET /api/v1/ticker/24hr all symbols weight decreased to number of trading symbols / 2
GET /api/v3/allOrders weight decreased to 5
GET /api/v3/myTrades weight decreased to 5
GET /api/v3/account weight decreased to 5
GET /api/v1/depth limit=500 weight decreased to 5
GET /api/v1/depth limit=1000 weight decreased to 10
-1003 error message updated to direct users to websockets
2018-01-20

GET /api/v1/ticker/24hr single symbol weight decreased to 1
GET /api/v3/openOrders all symbols weight decreased to number of trading symbols / 2
GET /api/v3/allOrders weight decreased to 15
GET /api/v3/myTrades weight decreased to 15
GET /api/v3/order weight decreased to 1
myTrades will now return both sides of a self-trade/wash-trade
2018-01-14

GET /api/v1/aggTrades weight changed to 2
GET /api/v1/klines weight changed to 2
GET /api/v3/order weight changed to 2
GET /api/v3/allOrders weight changed to 20
GET /api/v3/account weight changed to 20
GET /api/v3/myTrades weight changed to 20
GET /api/v3/historicalTrades weight changed to 20
Introduction

API Key Setup
Some endpoints will require an API Key. Please refer to this page regarding API key creation.
Once API key is created, it is recommended to set IP restrictions on the key for security reasons.
Never share your API key/secret key to ANYONE.
 If the API keys were accidentally shared, please delete them immediately and create a new key.
API Key Restrictions
After creating the API key, the default restrictions is Enable Reading.
To enable withdrawals via the API, the API key restriction needs to be modified through the Binance UI.
Enabling Accounts
Spot Account

A SPOT account is provided by default upon creation of a Binance Account.

Margin Account

To enable a MARGIN account for Margin Trading, please refer to the Margin Trading Guide

Spot Testnet

Users can use the SPOT Testnet to practice SPOT trading.

Currently, this is only available via the API.

Please refer to the SPOT Testnet page for more information and how to set up the Testnet API key.

API Library
Python connector

This is a lightweight library that works as a connector to Binance public API, written in Python.

https://github.com/binance/binance-connector-python

Node.js connector

This is a lightweight library that works as a connector to Binance public API, written for Node.js users.

https://github.com/binance/binance-connector-node

Ruby connector

This is a lightweight library that works as a connector to Binance public API, written for Ruby users.

https://github.com/binance/binance-connector-ruby

DotNET connector

This is a lightweight library that works as a connector to Binance public API, written for C# users.

https://github.com/binance/binance-connector-dotnet

Java connector

This is a lightweight library that works as a connector to Binance public API, written for Java users.

https://github.com/binance/binance-connector-java

Postman Collections

There is now a Postman collection containing the API endpoints for quick and easy use.

This is recommended for new users who want to get a quick-start into using the API.

For more information please refer to this page: Binance API Postman

Swagger

A YAML file with OpenAPI specification on the RESTful API is available to be used, as well as a Swagger UI page for the consulting.

https://github.com/binance/binance-api-swagger

Contact Us
Binance API Telegram Group
For any questions in sudden drop in performance with the API and/or Websockets.
For any general questions about the API not covered in the documentation.
Binance Developers
For any questions on your code implementation with the API and/or Websockets.
Binance Customer Support
For cases such as missing funds, help with 2FA, etc.
General Info

General API Information
The base endpoint is: https://api.binance.com
If there are performance issues with the endpoint above, these API clusters are also available:
https://api1.binance.com
https://api2.binance.com
https://api3.binance.com
All endpoints return either a JSON object or array.
Data is returned in ascending order. Oldest first, newest last.
All time and timestamp related fields are in milliseconds.
HTTP Return Codes

HTTP 4XX return codes are used for malformed requests; the issue is on the sender's side.
HTTP 403 return code is used when the WAF Limit (Web Application Firewall) has been violated.
HTTP 429 return code is used when breaking a request rate limit.
HTTP 418 return code is used when an IP has been auto-banned for continuing to send requests after receiving 429 codes.
HTTP 5XX return codes are used for internal errors; the issue is on Binance's side. It is important to NOT treat this as a failure operation; the execution status is UNKNOWN and could have been a success.
Error Codes and Messages

If there is an error, the API will return an error with a message of the reason.
The error payload on API and SAPI is as follows:
{
  "code": -1121,
  "msg": "Invalid symbol."
}
Specific error codes and messages defined in Error Codes.
General Information on Endpoints

For GET endpoints, parameters must be sent as a query string.
For POST, PUT, and DELETE endpoints, the parameters may be sent as a query string or in the request body with content type application/x-www-form-urlencoded. You may mix parameters between both the query string and request body if you wish to do so.
Parameters may be sent in any order.
If a parameter sent in both the query string and request body, the query string parameter will be used.
LIMITS
General Info on Limits

The following intervalLetter values for headers:
SECOND => S
MINUTE => M
HOUR => H
DAY => D
intervalNum describes the amount of the interval. For example, intervalNum 5 with intervalLetter M means "Every 5 minutes".
The /api/v3/exchangeInfo rateLimits array contains objects related to the exchange's RAW_REQUESTS, REQUEST_WEIGHT, and ORDERS rate limits. These are further defined in the ENUM definitions section under Rate limiters (rateLimitType).
A 429 will be returned when either rate limit is violated.
IP Limits

Every request will contain X-MBX-USED-WEIGHT-(intervalNum)(intervalLetter) in the response headers which has the current used weight for the IP for all request rate limiters defined.
Each route has a weight which determines for the number of requests each endpoint counts for. Heavier endpoints and endpoints that do operations on multiple symbols will have a heavier weight.
When a 429 is received, it's your obligation as an API to back off and not spam the API.
Repeatedly violating rate limits and/or failing to back off after receiving 429s will result in an automated IP ban (HTTP status 418).
IP bans are tracked and scale in duration for repeat offenders, from 2 minutes to 3 days.
A Retry-After header is sent with a 418 or 429 responses and will give the number of seconds required to wait, in the case of a 429, to prevent a ban, or, in the case of a 418, until the ban is over.
The limits on the API are based on the IPs, not the API keys.
 We recommend using the websocket for getting data as much as possible, as this will not count to the request rate limit.
Order Rate Limits

Every successful order response will contain a X-MBX-ORDER-COUNT-(intervalNum)(intervalLetter) header which has the current order count for the account for all order rate limiters defined.
When the order count exceeds the limit, you will receive a 429 error without the Retry-After header. Please check the Order Rate Limit rules using GET api/v3/exchangeInfo and wait for reactivation accordingly.
Rejected/unsuccessful orders are not guaranteed to have X-MBX-ORDER-COUNT-** headers in the response.
The order rate limit is counted against each account.
Websocket Limits

WebSocket connections have a limit of 5 incoming messages per second. A message is considered:
A PING frame
A PONG frame
A JSON controlled message (e.g. subscribe, unsubscribe)
A connection that goes beyond the limit will be disconnected; IPs that are repeatedly disconnected may be banned.
A single connection can listen to a maximum of 1024 streams.
/api/ and /sapi/ Limit Introduction

The /api/* and /sapi/* endpoints adopt either of two access limiting rules, IP limits or UID (account) limits.

Endpoints related to /api/*:

According to the two modes of IP and UID (account) limit, each are independent.
Endpoints share the 1200 per minute limit based on IP.
Responses contain the header X-MBX-USED-WEIGHT-(intervalNum)(intervalLetter), defining the weight used by the current IP.
Successful order responses contain the header X-MBX-ORDER-COUNT-(intervalNum)(intervalLetter), defining the order limit used by the UID.
Endpoints related to /sapi/*:

Endpoints are marked according to IP or UID limit and their corresponding weight value.
Each endpoint with IP limits has an independent 12000 per minute limit.
Each endpoint with UID limits has an independent 180000 per minute limit.
Responses from endpoints with IP limits contain the header X-SAPI-USED-IP-WEIGHT-1M, defining the weight used by the current IP.
Responses from endpoints with UID limits contain the header X-SAPI-USED-UID-WEIGHT-1M, defining the weight used by the current UID.
Data Sources
The API system is asynchronous, so some delay in the response is normal and expected.
Each endpoint has a data source indicating where the data is being retrieved, and thus which endpoints have the most up-to-date response.
These are the three sources, ordered by which is has the most up-to-date response to the one with potential delays in updates.

Matching Engine - the data is from the matching Engine
Memory - the data is from a server's local or external memory
Database - the data is taken directly from a database
 Some endpoints can have more than 1 data source. (e.g. Memory => Database) 
This means that the endpoint will check the first Data Source, and if it cannot find the value it's looking for it will check the next one.
Endpoint security type
Each endpoint has a security type that determines how you will interact with it. This is stated next to the NAME of the endpoint.
If no security type is stated, assume the security type is NONE.
API-keys are passed into the Rest API via the X-MBX-APIKEY header.
API-keys and secret-keys are case sensitive.
API-keys can be configured to only access certain types of secure endpoints. For example, one API-key could be used for TRADE only, while another API-key can access everything except for TRADE routes.
By default, API-keys can access all secure routes.
Security Type	Description
NONE	Endpoint can be accessed freely.
TRADE	Endpoint requires sending a valid API-Key and signature.
MARGIN	Endpoint requires sending a valid API-Key and signature.
USER_DATA	Endpoint requires sending a valid API-Key and signature.
USER_STREAM	Endpoint requires sending a valid API-Key.
MARKET_DATA	Endpoint requires sending a valid API-Key.
TRADE, MARGIN and USER_DATA endpoints are SIGNED endpoints.
SIGNED (TRADE, USER_DATA, AND MARGIN) Endpoint security
SIGNED endpoints require an additional parameter, signature, to be sent in the query string or request body.
Endpoints use HMAC SHA256 signatures. The HMAC SHA256 signature is a keyed HMAC SHA256 operation. Use your secretKey as the key and totalParams as the value for the HMAC operation.
The signature is not case sensitive.
totalParams is defined as the query string concatenated with the request body.
Timing security

A SIGNED endpoint also requires a parameter, timestamp, to be sent which should be the millisecond timestamp of when the request was created and sent.
An additional parameter, recvWindow, may be sent to specify the number of milliseconds after timestamp the request is valid for. If recvWindow is not sent, it defaults to 5000.
The logic is as follows:
  if (timestamp < (serverTime + 1000) && (serverTime - timestamp) <= recvWindow)
  {
    // process request
  } 
  else 
  {
    // reject request
  }
Serious trading is about timing. Networks can be unstable and unreliable, which can lead to requests taking varying amounts of time to reach the servers. With recvWindow, you can specify that the request must be processed within a certain number of milliseconds or be rejected by the server.

 It is recommended to use a small recvWindow of 5000 or less! The max cannot go beyond 60,000!
SIGNED Endpoint Examples for POST /api/v3/order

Here is a step-by-step example of how to send a vaild signed payload from the Linux command line using echo, openssl, and curl.

Key	Value
apiKey	vmPUZE6mv9SD5VNHk4HlWFsOr6aKE2zvsw0MuIgwCIPy6utIco14y7Ju91duEh8A
secretKey	NhqPtmdSJYdKjVHjA7PZj4Mge3R5YNiP1e3UZjInClVN65XAbvqqM6A7H5fATj0j
Parameter	Value
symbol	LTCBTC
side	BUY
type	LIMIT
timeInForce	GTC
quantity	1
price	0.1
recvWindow	5000
timestamp	1499827319559
Example 1: As a request body

Example 1
HMAC SHA256 signature:
    $ echo -n "symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559" | openssl dgst -sha256 -hmac "NhqPtmdSJYdKjVHjA7PZj4Mge3R5YNiP1e3UZjInClVN65XAbvqqM6A7H5fATj0j"
    (stdin)= c8db56825ae71d6d79447849e617115f4a920fa2acdcab2b053c4b2838bd6b71
curl command:
    (HMAC SHA256)
    $ curl -H "X-MBX-APIKEY: vmPUZE6mv9SD5VNHk4HlWFsOr6aKE2zvsw0MuIgwCIPy6utIco14y7Ju91duEh8A" -X POST 'https://api.binance.com/api/v3/order' -d 'symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559&signature=c8db56825ae71d6d79447849e617115f4a920fa2acdcab2b053c4b2838bd6b71'

requestBody:
symbol=LTCBTC
&side=BUY
&type=LIMIT
&timeInForce=GTC
&quantity=1
&price=0.1
&recvWindow=5000
&timestamp=1499827319559

Example 2: As a query string

Example 2
HMAC SHA256 signature:
    $ echo -n "symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559" | openssl dgst -sha256 -hmac "NhqPtmdSJYdKjVHjA7PZj4Mge3R5YNiP1e3UZjInClVN65XAbvqqM6A7H5fATj0j"
    (stdin)= c8db56825ae71d6d79447849e617115f4a920fa2acdcab2b053c4b2838bd6b71

curl command:
    (HMAC SHA256)
   $ curl -H "X-MBX-APIKEY: vmPUZE6mv9SD5VNHk4HlWFsOr6aKE2zvsw0MuIgwCIPy6utIco14y7Ju91duEh8A" -X POST 'https://api.binance.com/api/v3/order?symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559&signature=c8db56825ae71d6d79447849e617115f4a920fa2acdcab2b053c4b2838bd6b71'

queryString:
symbol=LTCBTC
&side=BUY
&type=LIMIT
&timeInForce=GTC
&quantity=1
&price=0.1
&recvWindow=5000
&timestamp=1499827319559

Example 3: Mixed query string and request body

Example 3
HMAC SHA256 signature:
   $ echo -n "symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTCquantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559" | openssl dgst -sha256 -hmac "NhqPtmdSJYdKjVHjA7PZj4Mge3R5YNiP1e3UZjInClVN65XAbvqqM6A7H5fATj0j"
    (stdin)= 0fd168b8ddb4876a0358a8d14d0c9f3da0e9b20c5d52b2a00fcf7d1c602f9a77

curl command:
    (HMAC SHA256)
    $ curl -H "X-MBX-APIKEY: vmPUZE6mv9SD5VNHk4HlWFsOr6aKE2zvsw0MuIgwCIPy6utIco14y7Ju91duEh8A" -X POST 'https://api.binance.com/api/v3/order?symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC' -d 'quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559&signature=0fd168b8ddb4876a0358a8d14d0c9f3da0e9b20c5d52b2a00fcf7d1c602f9a77'
queryString:
symbol=LTCBTC&side=BUY&type=LIMIT&timeInForce=GTC

requestBody:
quantity=1&price=0.1&recvWindow=5000&timestamp=1499827319559

Note that the signature is different in example 3. There is no & between "GTC" and "quantity=1".

Public API Definitions
Terminology

These terms will be used throughout the documentation, so it is recommended especially for new users to read to help their understanding of the API.

base asset refers to the asset that is the quantity of a symbol. For the symbol BTCUSDT, BTC would be the base asset.
quote asset refers to the asset that is the price of a symbol. For the symbol BTCUSDT, USDT would be the quote asset.
ENUM definitions

Symbol status (status):

PRE_TRADING
TRADING
POST_TRADING
END_OF_DAY
HALT
AUCTION_MATCH
BREAK
Account and Symbol Permissions (permissions):

SPOT
MARGIN
LEVERAGED
TRD_GRP_002
Order status (status):

Status	Description
NEW	The order has been accepted by the engine.
PARTIALLY_FILLED	A part of the order has been filled.
FILLED	The order has been completed.
CANCELED	The order has been canceled by the user.
PENDING_CANCEL	Currently unused
REJECTED	The order was not accepted by the engine and not processed.
EXPIRED	The order was canceled according to the order type's rules (e.g. LIMIT FOK orders with no fill, LIMIT IOC or MARKET orders that partially fill) or by the exchange, (e.g. orders canceled during liquidation, orders canceled during maintenance)
OCO Status (listStatusType):

Status	Description
RESPONSE	This is used when the ListStatus is responding to a failed action. (E.g. Orderlist placement or cancellation)
EXEC_STARTED	The order list has been placed or there is an update to the order list status.
ALL_DONE	The order list has finished executing and thus no longer active.
OCO Order Status (listOrderStatus):

Status	Description
EXECUTING	Either an order list has been placed or there is an update to the status of the list.
ALL_DONE	An order list has completed execution and thus no longer active.
REJECT	The List Status is responding to a failed action either during order placement or order canceled.)
ContingencyType

OCO
Order types (orderTypes, type):

More information on how the order types definitions can be found here: Types of Orders

LIMIT
MARKET
STOP_LOSS
STOP_LOSS_LIMIT
TAKE_PROFIT
TAKE_PROFIT_LIMIT
LIMIT_MAKER
Order Response Type (newOrderRespType):

ACK
RESULT
FULL
Order side (side):

BUY
SELL
Time in force (timeInForce):

This sets how long an order will be active before expiration.

Status	Description
GTC	Good Til Canceled 
An order will be on the book unless the order is canceled.
IOC	Immediate Or Cancel 
An order will try to fill the order as much as it can before the order expires.
FOK	Fill or Kill 
An order will expire if the full order cannot be filled upon execution.
Kline/Candlestick chart intervals:

m -> minutes; h -> hours; d -> days; w -> weeks; M -> months

1m
3m
5m
15m
30m
1h
2h
4h
6h
8h
12h
1d
3d
1w
1M
Rate limiters (rateLimitType)

REQUEST_WEIGHT
    {
      "rateLimitType": "REQUEST_WEIGHT",
      "interval": "MINUTE",
      "intervalNum": 1,
      "limit": 1200
    }
ORDERS
    {
      "rateLimitType": "ORDERS",
      "interval": "SECOND",
      "intervalNum": 10,
      "limit": 100
    },
    {
      "rateLimitType": "ORDERS",
      "interval": "DAY",
      "intervalNum": 1,
      "limit": 200000
    }
RAW_REQUESTS
    {
      "rateLimitType": "RAW_REQUESTS",
      "interval": "MINUTE",
      "intervalNum": 5,
      "limit": 5000
    }
REQUEST_WEIGHT

ORDERS

RAW_REQUESTS

Rate limit intervals (interval)

SECOND
MINUTE
DAY
Filters
Filters define trading rules on a symbol or an exchange. Filters come in two forms: symbol filters and exchange filters.

Symbol Filters

PRICE_FILTER

ExchangeInfo format:
  {
    "filterType": "PRICE_FILTER",
    "minPrice": "0.00000100",
    "maxPrice": "100000.00000000",
    "tickSize": "0.00000100"
  }
The PRICE_FILTER defines the price rules for a symbol. There are 3 parts:

minPrice defines the minimum price/stopPrice allowed; disabled on minPrice == 0.
maxPrice defines the maximum price/stopPrice allowed; disabled on maxPrice == 0.
tickSize defines the intervals that a price/stopPrice can be increased/decreased by; disabled on tickSize == 0.
Any of the above variables can be set to 0, which disables that rule in the price filter. In order to pass the price filter, the following must be true for price/stopPrice of the enabled rules:

price >= minPrice
price <= maxPrice
(price-minPrice) % tickSize == 0
PERCENT_PRICE

ExchangeInfo format:
  {
    "filterType": "PERCENT_PRICE",
    "multiplierUp": "1.3000",
    "multiplierDown": "0.7000",
    "avgPriceMins": 5
  }
The PERCENT_PRICE filter defines valid range for a price based on the average of the previous trades. avgPriceMins is the number of minutes the average price is calculated over. 0 means the last price is used.

In order to pass the percent price, the following must be true for price:

price <= weightedAveragePrice * multiplierUp
price >= weightedAveragePrice * multiplierDown
LOT_SIZE

ExchangeInfo format:
  {
    "filterType": "LOT_SIZE",
    "minQty": "0.00100000",
    "maxQty": "100000.00000000",
    "stepSize": "0.00100000"
  }
The LOT_SIZE filter defines the quantity (aka "lots" in auction terms) rules for a symbol. There are 3 parts:

minQty defines the minimum quantity/icebergQty allowed.
maxQty defines the maximum quantity/icebergQty allowed.
stepSize defines the intervals that a quantity/icebergQty can be increased/decreased by.
In order to pass the lot size, the following must be true for quantity/icebergQty:

quantity >= minQty
quantity <= maxQty
(quantity-minQty) % stepSize == 0
MIN_NOTIONAL

ExchangeInfo format:
  {
    "filterType": "MIN_NOTIONAL",
    "minNotional": "0.00100000",
    "applyToMarket": true,
    "avgPriceMins": 5
  }
The MIN_NOTIONAL filter defines the minimum notional value allowed for an order on a symbol. An order's notional value is the price * quantity. If the order is an Algo order (e.g. STOP_LOSS_LIMIT), then the notional value of the stopPrice * quantity will also be evaluated. If the order is an Iceberg Order, then the notional value of the price * icebergQty will also be evaluated. applyToMarket determines whether or not the MIN_NOTIONAL filter will also be applied to MARKET orders. Since MARKET orders have no price, the average price is used over the last avgPriceMins minutes. avgPriceMins is the number of minutes the average price is calculated over. 0 means the last price is used.

ICEBERG_PARTS

ExchangeInfo format:
  {
    "filterType": "ICEBERG_PARTS",
    "limit": 10
  }
The ICEBERG_PARTS filter defines the maximum parts an iceberg order can have. The number of ICEBERG_PARTS is defined as CEIL(qty / icebergQty).

MARKET_LOT_SIZE

ExchangeInfo format:
  {
    "filterType": "MARKET_LOT_SIZE",
    "minQty": "0.00100000",
    "maxQty": "100000.00000000",
    "stepSize": "0.00100000"
  }
The MARKET_LOT_SIZE filter defines the quantity (aka "lots" in auction terms) rules for MARKET orders on a symbol. There are 3 parts:

minQty defines the minimum quantity allowed.
maxQty defines the maximum quantity allowed.
stepSize defines the intervals that a quantity can be increased/decreased by.
In order to pass the market lot size, the following must be true for quantity:

quantity >= minQty
quantity <= maxQty
(quantity-minQty) % stepSize == 0
MAX_NUM_ORDERS

ExchangeInfo format:
  {
    "filterType": "MAX_NUM_ORDERS",
    "maxNumOrders": 25
  }
The MAX_NUM_ORDERS filter defines the maximum number of orders an account is allowed to have open on a symbol. Note that both "algo" orders and normal orders are counted for this filter.

MAX_NUM_ALGO_ORDERS

ExchangeInfo format:
  {
    "filterType": "MAX_NUM_ALGO_ORDERS",
    "maxNumAlgoOrders": 5
  }
The MAX_NUM_ALGO_ORDERS filter defines the maximum number of "algo" orders an account is allowed to have open on a symbol. "Algo" orders are STOP_LOSS, STOP_LOSS_LIMIT, TAKE_PROFIT, and TAKE_PROFIT_LIMIT orders.

MAX_NUM_ICEBERG_ORDERS

The MAX_NUM_ICEBERG_ORDERS filter defines the maximum number of ICEBERG orders an account is allowed to have open on a symbol. An ICEBERG order is any order where the icebergQty is > 0.

ExchangeInfo format:
  {
    "filterType": "MAX_NUM_ICEBERG_ORDERS",
    "maxNumIcebergOrders": 5
  }
MAX_POSITION

The MAX_POSITION filter defines the allowed maximum position an account can have on the base asset of a symbol. An account's position defined as the sum of the account's:

free balance of the base asset
locked balance of the base asset
sum of the qty of all open BUY orders
BUY orders will be rejected if the account's position is greater than the maximum position allowed.

ExchangeInfo format:
{
  "filterType":"MAX_POSITION",
  "maxPosition":"10.00000000"
}
Exchange Filters

EXCHANGE_MAX_NUM_ORDERS

ExchangeInfo format:
  {
    "filterType": "EXCHANGE_MAX_NUM_ORDERS",
    "maxNumOrders": 1000
  }
The EXCHANGE_MAX_NUM_ORDERS filter defines the maximum number of orders an account is allowed to have open on the exchange. Note that both "algo" orders and normal orders are counted for this filter.

EXCHANGE_MAX_NUM_ALGO_ORDERS

ExchangeInfo format:
  {
    "filterType": "EXCHANGE_MAX_NUM_ALGO_ORDERS",
    "maxNumAlgoOrders": 200
  }
The EXCHANGE_MAX_NUM_ALGO_ORDERS filter defines the maximum number of "algo" orders an account is allowed to have open on the exchange. "Algo" orders are STOP_LOSS, STOP_LOSS_LIMIT, TAKE_PROFIT, and TAKE_PROFIT_LIMIT orders.

Wallet Endpoints

System Status (System)
Response
{ 
    "status": 0,              // 0: normal，1：system maintenance
    "msg": "normal"           // "normal", "system_maintenance"
}
GET /sapi/v1/system/status

Fetch system status.

Weight(IP): 1

All Coins' Information (USER_DATA)
Get information of coins (available for deposit and withdraw) for user.

Response:
[
    {
        "coin": "BTC",
        "depositAllEnable": true,
        "free": "0.08074558",
        "freeze": "0.00000000",
        "ipoable": "0.00000000",
        "ipoing": "0.00000000",
        "isLegalMoney": false,
        "locked": "0.00000000",
        "name": "Bitcoin",
        "networkList": [
            {
                "addressRegex": "^(bnb1)[0-9a-z]{38}$",
                "coin": "BTC",
                "depositDesc": "Wallet Maintenance, Deposit Suspended", // shown only when "depositEnable" is false.
                "depositEnable": false,
                "isDefault": false,        
                "memoRegex": "^[0-9A-Za-z\\-_]{1,120}$",
                "minConfirm": 1,  // min number for balance confirmation
                "name": "BEP2",
                "network": "BNB",            
                "resetAddressStatus": false,
                "specialTips": "Both a MEMO and an Address are required to successfully deposit your BEP2-BTCB tokens to Binance.",
                "unLockConfirm": 0,  // confirmation number for balance unlock 
                "withdrawDesc": "Wallet Maintenance, Withdrawal Suspended", // shown only when "withdrawEnable" is false.
                "withdrawEnable": false,
                "withdrawFee": "0.00000220",
                "withdrawIntegerMultiple": "0.00000001",
                "withdrawMax": "9999999999.99999999",
                "withdrawMin": "0.00000440",
                "sameAddress": true  // If the coin needs to provide memo to withdraw
            },
            {
                "addressRegex": "^[13][a-km-zA-HJ-NP-Z1-9]{25,34}$|^(bc1)[0-9A-Za-z]{39,59}$",
                "coin": "BTC",
                "depositEnable": true,
                "isDefault": true,
                "memoRegex": "",
                "minConfirm": 1, 
                "name": "BTC",
                "network": "BTC",
                "resetAddressStatus": false,
                "specialTips": "",
                "unLockConfirm": 2,
                "withdrawEnable": true,
                "withdrawFee": "0.00050000",
                "withdrawIntegerMultiple": "0.00000001",
                "withdrawMax": "750",
                "withdrawMin": "0.00100000",
                "sameAddress": false
            }
        ],
        "storage": "0.00000000",
        "trading": true,
        "withdrawAllEnable": true,
        "withdrawing": "0.00000000"
    }
]
GET /sapi/v1/capital/config/getall (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Daily Account Snapshot (USER_DATA)
Response:
{
   "code":200, // 200 for success; others are error codes
   "msg":"", // error message
   "snapshotVos":[
      {
         "data":{
            "balances":[
               {
                  "asset":"BTC",
                  "free":"0.09905021",
                  "locked":"0.00000000"
               },
               {
                  "asset":"USDT",
                  "free":"1.89109409",
                  "locked":"0.00000000"
               }
            ],
            "totalAssetOfBtc":"0.09942700"
         },
         "type":"spot",
         "updateTime":1576281599000
      }
   ]
}

OR
{
   "code":200, // 200 for success; others are error codes
   "msg":"", // error message
   "snapshotVos":[
      {
         "data":{
            "marginLevel":"2748.02909813",
            "totalAssetOfBtc":"0.00274803",
            "totalLiabilityOfBtc":"0.00000100",
            "totalNetAssetOfBtc":"0.00274750",
            "userAssets":[
               {
                  "asset":"XRP",
                  "borrowed":"0.00000000",
                  "free":"1.00000000",
                  "interest":"0.00000000",
                  "locked":"0.00000000",
                  "netAsset":"1.00000000"
               }
            ]
         },
         "type":"margin",
         "updateTime":1576281599000
      }
   ]
}
OR
{
   "code":200, // 200 for success; others are error codes
   "msg":"", // error message
   "snapshotVos":[
      {
         "data":{
            "assets":[
               {
                  "asset":"USDT",
                  "marginBalance":"118.99782335",
                  "walletBalance":"120.23811389"
               }
            ],
            "position":[
               {
                  "entryPrice":"7130.41000000",
                  "markPrice":"7257.66239673",
                  "positionAmt":"0.01000000",
                  "symbol":"BTCUSDT",
                  "unRealizedProfit":"1.24029054"  // Only show the value at the time of opening the position
               }
            ]
         },
         "type":"futures",
         "updateTime":1576281599000
      }
   ]
}
GET /sapi/v1/accountSnapshot (HMAC SHA256)

Weight(IP): 2400

Parameters:

Name	Type	Mandatory	Description
type	STRING	YES	"SPOT", "MARGIN", "FUTURES"
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	min 5, max 30, default 5
recvWindow	LONG	NO	
timestamp	LONG	YES	
The query time period must be less then 30 days
Support query within the last 6 months only
If startTimeand endTime not sent, return records of the last 7 days by default
Disable Fast Withdraw Switch (USER_DATA)
Response:
{}
POST /sapi/v1/account/disableFastWithdrawSwitch (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Caution:

This request will disable fastwithdraw switch under your account. 
You need to enable "trade" option for the api key which requests this endpoint.

Enable Fast Withdraw Switch (USER_DATA)
Response:
{}
POST /sapi/v1/account/enableFastWithdrawSwitch (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
This request will enable fastwithdraw switch under your account. 
You need to enable "trade" option for the api key which requests this endpoint.
When Fast Withdraw Switch is on, transferring funds to a Binance account will be done instantly. There is no on-chain transaction, no transaction ID and no withdrawal fee.
Withdraw(USER_DATA)
Response:
{
    "id":"7213fea8e94b4a5593d507237e5a555b"
}
POST /sapi/v1/capital/withdraw/apply (HMAC SHA256)

Submit a withdraw request.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
withdrawOrderId	STRING	NO	client id for withdraw
network	STRING	NO	
address	STRING	YES	
addressTag	STRING	NO	Secondary address identifier for coins like XRP,XMR etc.
amount	DECIMAL	YES	
transactionFeeFlag	BOOLEAN	NO	When making internal transfer, true for returning the fee to the destination account; false for returning the fee back to the departure account. Default false.
name	STRING	NO	Description of the address. Space in name should be encoded into %20.
walletType	INTEGER	NO	The wallet type for withdraw，0-spot wallet ，1-funding wallet.Default spot wallet
recvWindow	LONG	NO	
timestamp	LONG	YES	
If network not send, return with default network of the coin.
You can get network and isDefault in networkList of a coin in the response of Get /sapi/v1/capital/config/getall (HMAC SHA256).
Deposit History(supporting network) (USER_DATA)
Response:
[
    {
        "amount":"0.00999800",
        "coin":"PAXG",
        "network":"ETH",
        "status":1,
        "address":"0x788cabe9236ce061e5a892e1a59395a81fc8d62c",
        "addressTag":"",
        "txId":"0xaad4654a3234aa6118af9b4b335f5ae81c360b2394721c019b5d1e75328b09f3",
        "insertTime":1599621997000,
        "transferType":0,
        "unlockConfirm":"12/12",  // confirm times for unlocking
        "confirmTimes":"12/12"
    },
    {
        "amount":"0.50000000",
        "coin":"IOTA",
        "network":"IOTA",
        "status":1,
        "address":"SIZ9VLMHWATXKV99LH99CIGFJFUMLEHGWVZVNNZXRJJVWBPHYWPPBOSDORZ9EQSHCZAMPVAPGFYQAUUV9DROOXJLNW",
        "addressTag":"",
        "txId":"ESBFVQUTPIWQNJSPXFNHNYHSQNTGKRVKPRABQWTAXCDWOAKDKYWPTVG9BGXNVNKTLEJGESAVXIKIZ9999",
        "insertTime":1599620082000,
        "transferType":0,
        "unlockConfirm":"1/12",
        "confirmTimes":"1/1"
    }
]
GET /sapi/v1/capital/deposit/hisrec (HMAC SHA256)

Fetch deposit history.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
coin	STRING	NO	
status	INT	NO	0(0:pending,6: credited but cannot withdraw, 1:success)
startTime	LONG	NO	Default: 90 days from current timestamp
endTime	LONG	NO	Default: present timestamp
offset	INT	NO	Default:0
limit	INT	NO	Default:1000, Max:1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Please notice the default startTime and endTime to make sure that time interval is within 0-90 days.
If both startTime and endTime are sent, time between startTime and endTime must be less than 90 days.
Withdraw History (supporting network) (USER_DATA)
Response:
[
    {
        "address": "0x94df8b352de7f46f64b01d3666bf6e936e44ce60",
        "amount": "8.91000000",
        "applyTime": "2019-10-12 11:12:02",
        "coin": "USDT",
        "id": "b6ae22b3aa844210a7041aee7589627c",
        "withdrawOrderId": "WITHDRAWtest123", // will not be returned if there's no withdrawOrderId for this withdraw.
        "network": "ETH", 
        "transferType": 0,   // 1 for internal transfer, 0 for external transfer   
        "status": 6,
        "transactionFee": "0.004",
        "confirmNo":3,  // confirm times for withdraw
        "info":"The address is not valid. Please confirm with the recipient", // reason for withdrawal failure
        "txId": "0xb5ef8c13b968a406cc62a93a8bd80f9e9a906ef1b3fcf20a2e48573c17659268"
    },
    {
        "address": "1FZdVHtiBqMrWdjPyRPULCUceZPJ2WLCsB",
        "amount": "0.00150000",
        "applyTime": "2019-09-24 12:43:45",
        "coin": "BTC",
        "id": "156ec387f49b41df8724fa744fa82719",
        "network": "BTC",
        "status": 6,
        "transactionFee": "0.004",
        "transferType": 0,   // 1 for internal transfer, 0 for external transfer   
        "confirmNo":2,
        "info":"",
        "txId": "60fd9007ebfddc753455f95fafa808c4302c836e4d1eebc5a132c36c1d8ac354"
    }
]
GET /sapi/v1/capital/withdraw/history (HMAC SHA256)

Fetch withdraw history.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
coin	STRING	NO	
withdrawOrderId	STRING	NO	
status	INT	NO	0(0:Email Sent,1:Cancelled 2:Awaiting Approval 3:Rejected 4:Processing 5:Failure 6:Completed)
offset	INT	NO	
limit	INT	NO	Default: 1000, Max: 1000
startTime	LONG	NO	Default: 90 days from current timestamp
endTime	LONG	NO	Default: present timestamp
recvWindow	LONG	NO	
timestamp	LONG	YES	
network may not be in the response for old withdraw.
Please notice the default startTime and endTime to make sure that time interval is within 0-90 days.
If both startTime and endTime are sent, time between startTime and endTime must be less than 90 days.
Deposit Address (supporting network) (USER_DATA)
Response:
{
    "address": "1HPn8Rx2y6nNSfagQBKy27GB99Vbzg89wv",
    "coin": "BTC",
    "tag": "",
    "url": "https://btc.com/1HPn8Rx2y6nNSfagQBKy27GB99Vbzg89wv"
}
GET /sapi/v1/capital/deposit/address (HMAC SHA256)

Fetch deposit address with network.

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
network	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
If network is not send, return with default network of the coin.
You can get network and isDefault in networkList in the response of Get /sapi/v1/capital/config/getall (HMAC SHA256).
Account Status (USER_DATA)
Response:
{
    "data": "Normal"
}
GET /sapi/v1/account/status

Fetch account status detail.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Account API Trading Status (USER_DATA)
Response:
{
    "data": {          // API trading status detail
            "isLocked": false,   // API trading function is locked or not
            "plannedRecoverTime": 0,  // If API trading function is locked, this is the planned recover time
            "triggerCondition": { 
                    "GCR": 150,  // Number of GTC orders
                    "IFER": 150, // Number of FOK/IOC orders
                    "UFR": 300   // Number of orders
            },
            "updateTime": 1547630471725   
    }
}
GET /sapi/v1/account/apiTradingStatus (HMAC SHA256)

Fetch account api trading status detail.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
DustLog(USER_DATA)
Response
{
        "total": 8,   //Total counts of exchange
        "userAssetDribblets": [
            {
                "operateTime": 1615985535000,
                "totalTransferedAmount": "0.00132256",   // Total transfered BNB amount for this exchange.
                "totalServiceChargeAmount": "0.00002699",    //Total service charge amount for this exchange.
                "transId": 45178372831,
                "userAssetDribbletDetails": [           //Details of  this exchange.
                    {
                        "transId": 4359321,
                        "serviceChargeAmount": "0.000009",
                        "amount": "0.0009",
                        "operateTime": 1615985535000,
                        "transferedAmount": "0.000441",
                        "fromAsset": "USDT"
                    },
                    {
                        "transId": 4359321,
                        "serviceChargeAmount": "0.00001799",
                        "amount": "0.0009",
                        "operateTime": 1615985535000,
                        "transferedAmount": "0.00088156",
                        "fromAsset": "ETH"
                    }
                ]
            },
            {
                "operateTime":1616203180000,
                "totalTransferedAmount": "0.00058795",
                "totalServiceChargeAmount": "0.000012",
                "transId": 4357015,
                "userAssetDribbletDetails": [       
                    {
                        "transId": 4357015,
                        "serviceChargeAmount": "0.00001",
                        "amount": "0.001",
                        "operateTime": 1616203180000,
                        "transferedAmount": "0.00049",
                        "fromAsset": "USDT"
                    },
                    {
                        "transId": 4357015,
                        "serviceChargeAmount": "0.000002",         
                        "amount": "0.0001",
                        "operateTime": 1616203180000,
                        "transferedAmount": "0.00009795",
                        "fromAsset": "ETH"
                    }
                ]
            }
        ]
    }
}
GET /sapi/v1/asset/dribblet (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	NO	
endTime	LONG	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Only return last 100 records
Only return records after 2020/12/01
Get Assets That Can Be Converted Into BNB (USER_DATA)
Response
{
    "details": [
        {
            "asset": "ADA",         
            "assetFullName": "ADA", 
            "amountFree": "6.21",   //Convertible amount
            "toBTC": "0.00016848",  //BTC amount
            "toBNB": "0.01777302",  //BNB amount（Not deducted commission fee）
            "toBNBOffExchange": "0.01741756", //BNB amount（Deducted commission fee）
            "exchange": "0.00035546" //Commission fee
        }
    ],
    "totalTransferBtc": "0.00016848",
    "totalTransferBNB": "0.01777302",
    "dribbletPercentage": "0.02"     //Commission fee
}  
POST /sapi/v1/asset/dust-btc (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Dust Transfer (USER_DATA)
Response:
{
    "totalServiceCharge":"0.02102542",
    "totalTransfered":"1.05127099",
    "transferResult":[
        {
            "amount":"0.03000000",
            "fromAsset":"ETH",
            "operateTime":1563368549307,
            "serviceChargeAmount":"0.00500000",
            "tranId":2970932918,
            "transferedAmount":"0.25000000"
        },
        {
            "amount":"0.09000000",
            "fromAsset":"LTC",
            "operateTime":1563368549404,
            "serviceChargeAmount":"0.01548000",
            "tranId":2970932918,
            "transferedAmount":"0.77400000"
        },
        {
            "amount":"248.61878453",
            "fromAsset":"TRX",
            "operateTime":1563368549489,
            "serviceChargeAmount":"0.00054542",
            "tranId":2970932918,
            "transferedAmount":"0.02727099"
        }
    ]
}
POST /sapi/v1/asset/dust (HMAC SHA256)

Convert dust assets to BNB.

Weight(UID): 10

Parameters:

Name	Type	Mandatory	Description
asset	ARRAY	YES	The asset being converted. For example: asset=BTC&asset=USDT
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Asset Dividend Record (USER_DATA)
Response:
{
    "rows":[
        {
            "id":1637366104,
            "amount":"10.00000000",
            "asset":"BHFT",
            "divTime":1563189166000,
            "enInfo":"BHFT distribution",
            "tranId":2968885920
        },
        {
            "id":1631750237,
            "amount":"10.00000000",
            "asset":"BHFT",
            "divTime":1563189165000,
            "enInfo":"BHFT distribution",
            "tranId":2968885920
        }
    ],
    "total":2
}
GET /sapi/v1/asset/assetDividend (HMAC SHA256)

Query asset dividend record.

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 20, max 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
Asset Detail (USER_DATA)
Response:
{
        "CTR": {
            "minWithdrawAmount": "70.00000000", //min withdraw amount
            "depositStatus": false,//deposit status (false if ALL of networks' are false)
            "withdrawFee": 35, // withdraw fee
            "withdrawStatus": true, //withdraw status (false if ALL of networks' are false)
            "depositTip": "Delisted, Deposit Suspended" //reason
        },
        "SKY": {
            "minWithdrawAmount": "0.02000000",
            "depositStatus": true,
            "withdrawFee": 0.01,
            "withdrawStatus": true
        }   
}
GET /sapi/v1/asset/assetDetail (HMAC SHA256)

Fetch details of assets supported on Binance.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Please get network and other deposit or withdraw details from GET /sapi/v1/capital/config/getall.
Trade Fee (USER_DATA)
Response:
[
    {
        "symbol": "ADABNB",
        "makerCommission": "0.001",
        "takerCommission": "0.001"
    },
    {
        "symbol": "BNBBTC",
        "makerCommission": "0.001",
        "takerCommission": "0.001"
    }
]
GET /sapi/v1/asset/tradeFee (HMAC SHA256)

Fetch trade fee

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
User Universal Transfer (USER_DATA)
Response:
{
    "tranId":13526853623
}

POST /sapi/v1/asset/transfer (HMAC SHA256)

You need to enable Permits Universal Transfer option for the API Key which requests this endpoint.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
type	ENUM	YES	
asset	STRING	YES	
amount	DECIMAL	YES	
fromSymbol	STRING	NO	
toSymbol	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
fromSymbol must be sent when type are ISOLATEDMARGIN_MARGIN and ISOLATEDMARGIN_ISOLATEDMARGIN
toSymbol must be sent when type are MARGIN_ISOLATEDMARGIN and ISOLATEDMARGIN_ISOLATEDMARGIN

ENUM of transfer types:

MAIN_UMFUTURE Spot account transfer to USDⓈ-M Futures account
MAIN_CMFUTURE Spot account transfer to COIN-M Futures account
MAIN_MARGIN Spot account transfer to Margin（cross）account
UMFUTURE_MAIN USDⓈ-M Futures account transfer to Spot account
UMFUTURE_MARGIN USDⓈ-M Futures account transfer to Margin（cross）account
CMFUTURE_MAIN COIN-M Futures account transfer to Spot account
CMFUTURE_MARGIN COIN-M Futures account transfer to Margin(cross) account
MARGIN_MAIN Margin（cross）account transfer to Spot account
MARGIN_UMFUTURE Margin（cross）account transfer to USDⓈ-M Futures
MARGIN_CMFUTURE Margin（cross）account transfer to COIN-M Futures
ISOLATEDMARGIN_MARGIN Isolated margin account transfer to Margin(cross) account
MARGIN_ISOLATEDMARGIN Margin(cross) account transfer to Isolated margin account
ISOLATEDMARGIN_ISOLATEDMARGIN Isolated margin account transfer to Isolated margin account
MAIN_FUNDING Spot account transfer to Funding account
FUNDING_MAIN Funding account transfer to Spot account
FUNDING_UMFUTURE Funding account transfer to UMFUTURE account
UMFUTURE_FUNDING UMFUTURE account transfer to Funding account
MARGIN_FUNDING MARGIN account transfer to Funding account
FUNDING_MARGIN Funding account transfer to Margin account
FUNDING_CMFUTURE Funding account transfer to CMFUTURE account
CMFUTURE_FUNDING CMFUTURE account transfer to Funding account
Query User Universal Transfer History (USER_DATA)
Response:
{
    "total":2,
    "rows":[
        {
            "asset":"USDT",
            "amount":"1",
            "type":"MAIN_UMFUTURE",
            "status": "CONFIRMED",
            "tranId": 11415955596,
            "timestamp":1544433328000
        },
        {
            "asset":"USDT",
            "amount":"2",
            "type":"MAIN_UMFUTURE",
            "status": "CONFIRMED",
            "tranId": 11366865406,
            "timestamp":1544433328000
        }
    ]
}
GET /sapi/v1/asset/transfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
type	ENUM	YES	
startTime	LONG	NO	
endTime	LONG	NO	
current	INT	NO	Default 1
size	INT	NO	Default 10, Max 100
fromSymbol	STRING	NO	
toSymbol	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
fromSymbol must be sent when type are ISOLATEDMARGIN_MARGIN and ISOLATEDMARGIN_ISOLATEDMARGIN
toSymbol must be sent when type are MARGIN_ISOLATEDMARGIN and ISOLATEDMARGIN_ISOLATEDMARGIN
Support query within the last 6 months only
If startTimeand endTime not sent, return records of the last 7 days by default
Funding Wallet (USER_DATA)
Response
[
    {
        "asset": "USDT",
        "free": "1",    // avalible balance
        "locked": "0",  // locked asset
        "freeze": "0",  // freeze asset
        "withdrawing": "0",  
        "btcValuation": "0.00000091"  
    }
]
POST /sapi/v1/asset/get-funding-asset (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
needBtcValuation	STRING	NO	true or false
recvWindow	LONG	NO	
timestamp	LONG	YES	
Currently supports querying the following business assets：Binance Pay, Binance Card, Binance Gift Card, Stock Token
Get API Key Permission (USER_DATA)
Response
{
   "ipRestrict": false,
   "createTime": 1623840271000,   
   "enableWithdrawals": false,   // This option allows you to withdraw via API. You must apply the IP Access Restriction filter in order to enable withdrawals
   "enableInternalTransfer": true,  // This option authorizes this key to transfer funds between your master account and your sub account instantly
   "permitsUniversalTransfer": true,  // Authorizes this key to be used for a dedicated universal transfer API to transfer multiple supported currencies. Each business's own transfer API rights are not affected by this authorization
   "enableVanillaOptions": false,  //  Authorizes this key to Vanilla options trading
   "enableReading": true,
   "enableFutures": false,  //  API Key created before your futures account opened does not support futures API service
   "enableMargin": false,   //  This option can be adjusted after the Cross Margin account transfer is completed
   "enableSpotAndMarginTrading": false, // Spot and margin trading
   "tradingAuthorityExpirationTime": 1628985600000  // Expiration time for spot and margin trading permission
}
GET /sapi/v1/account/apiRestrictions (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Sub-Account Endpoints

The endpoints documented in this section are for Corporate Accounts.
To become a corporate account, please refer to this document: Corporate Account Application
Create a Virtual Sub-account(For Master Account)
Response:
{
    "email":"addsdd_virtual@aasaixwqnoemail.com"
}
POST /sapi/v1/sub-account/virtualSubAccount (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
subAccountString	STRING	YES	Please input a string. We will create a virtual email using that string for you to register
recvWindow	LONG	NO	
timestamp	LONG	YES	
This request will generate a virtual sub account under your master account.
You need to enable "trade" option for the API Key which requests this endpoint.
Query Sub-account List (For Master Account)
Response:
{
    "subAccounts":[
        {
            "email":"testsub@gmail.com",
            "isFreeze":false,
            "createTime":1544433328000
        },
        {
            "email":"virtual@oxebmvfonoemail.com",
            "isFreeze":false,
            "createTime":1544433328000
        }
    ]
}
GET /sapi/v1/sub-account/list (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	NO	Sub-account email
isFreeze	STRING	NO	true or false
page	INT	NO	Default value: 1
limit	INT	NO	Default value: 1, Max value: 200
recvWindow	LONG	NO	
timestamp	LONG	YES	
Query Sub-account Spot Asset Transfer History (For Master Account)
Response:
[
    {
        "from":"aaa@test.com",
        "to":"bbb@test.com",
        "asset":"BTC",
        "qty":"10",
        "status": "SUCCESS",
        "tranId": 6489943656,
        "time":1544433328000
    },
    {
        "from":"bbb@test.com",
        "to":"ccc@test.com",
        "asset":"ETH",
        "qty":"2",
        "status": "SUCCESS",
        "tranId": 6489938713,
        "time":1544433328000
    }
]
GET /sapi/v1/sub-account/sub/transfer/history (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
fromEmail	STRING	NO	Sub-account email
toEmail	STRING	NO	Sub-account email
startTime	LONG	NO	
endTime	LONG	NO	
page	INT	NO	Default value: 1
limit	INT	NO	Default value: 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
fromEmail and toEmail cannot be sent at the same time.
Return fromEmail equal master account email by default.
Query Sub-account Futures Asset Transfer History (For Master Account)
Response
{
    "success":true,
    "futuresType": 2,
    "transfers":[
        {
            "from":"aaa@test.com",
            "to":"bbb@test.com",
            "asset":"BTC",
            "qty":"1",
            "tranId":11897001102,
            "time":1544433328000
        },
        {
            "from":"bbb@test.com",
            "to":"ccc@test.com",
            "asset":"ETH",
            "qty":"2",
            "tranId":11631474902,
            "time":1544433328000
        }
    ]
}
GET /sapi/v1/sub-account/futures/internalTransfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
futuresType	LONG	YES	1:USDT-margined Futures，2: Coin-margined Futures
startTime	LONG	NO	Default return the history with in 100 days
endTime	LONG	NO	Default return the history with in 100 days
page	INT	NO	Default value: 1
limit	INT	NO	Default value: 50, Max value: 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
Sub-account Futures Asset Transfer (For Master Account)
Response
{
    "success":true,
    "txnId":"2934662589"
}

POST /sapi/v1/sub-account/futures/internalTransfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
fromEmail	STRING	YES	Sender email
toEmail	STRING	YES	Recipient email
futuresType	LONG	YES	1:USDT-margined Futures，2: Coin-margined Futures
asset	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Master account can transfer max 2000 times a minute
Query Sub-account Assets (For Master Account)
Response:
{
    "balances":[
        {
            "asset":"ADA",
            "free":10000,
            "locked":0
        },
        {
            "asset":"BNB",
            "free":10003,
            "locked":0
        },
        {
            "asset":"BTC",
            "free":11467.6399,
            "locked":0
        },
        {
            "asset":"ETH",
            "free":10004.995,
            "locked":0
        },
        {
            "asset":"USDT",
            "free":11652.14213,
            "locked":0
        }
    ]
}
GET /sapi/v3/sub-account/assets (HMAC SHA256)

Fetch sub-account assets

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Query Sub-account Spot Assets Summary (For Master Account)
Response:
{
    "totalCount":2,
    "masterAccountTotalAsset": "0.23231201",
    "spotSubUserAssetBtcVoList":[
        {
            "email":"sub123@test.com",
            "totalAsset":"9999.00000000"
        },
        {
            "email":"test456@test.com",
            "totalAsset":"0.00000000"
        }
    ]
}
Get BTC valued asset summary of subaccounts.

GET /sapi/v1/sub-account/spotSummary (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	NO	Sub account email
page	LONG	NO	default 1
size	LONG	NO	default 10, max 20
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Sub-account Deposit Address (For Master Account)
Response:
{
    "address":"TDunhSa7jkTNuKrusUTU1MUHtqXoBPKETV",
    "coin":"USDT",
    "tag":"",
    "url":"https://tronscan.org/#/address/TDunhSa7jkTNuKrusUTU1MUHtqXoBPKETV"
}
GET /sapi/v1/capital/deposit/subAddress (HMAC SHA256)

Fetch sub-account deposit address

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub account email
coin	STRING	YES	
network	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Sub-account Deposit History (For Master Account)
Response:
[
    {
        "amount":"0.00999800",
        "coin":"PAXG",
        "network":"ETH",
        "status":1,
        "address":"0x788cabe9236ce061e5a892e1a59395a81fc8d62c",
        "addressTag":"",
        "txId":"0xaad4654a3234aa6118af9b4b335f5ae81c360b2394721c019b5d1e75328b09f3",
        "insertTime":1599621997000,
        "transferType":0,
        "confirmTimes":"12/12"
    },
    {
        "amount":"0.50000000",
        "coin":"IOTA",
        "network":"IOTA",
        "status":1,
        "address":"SIZ9VLMHWATXKV99LH99CIGFJFUMLEHGWVZVNNZXRJJVWBPHYWPPBOSDORZ9EQSHCZAMPVAPGFYQAUUV9DROOXJLNW",
        "addressTag":"",
        "txId":"ESBFVQUTPIWQNJSPXFNHNYHSQNTGKRVKPRABQWTAXCDWOAKDKYWPTVG9BGXNVNKTLEJGESAVXIKIZ9999",
        "insertTime":1599620082000,
        "transferType":0,
        "confirmTimes":"1/1"
    }
]
GET /sapi/v1/capital/deposit/subHisrec (HMAC SHA256)

Fetch sub-account deposit history

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub account email
coin	STRING	NO	
status	INT	NO	0(0:pending,6: credited but cannot withdraw, 1:success)
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	
offset	INT	NO	default:0
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Sub-account's Status on Margin/Futures (For Master Account)
Response
[
    {
        "email":"123@test.com",      // user email
        "isSubUserEnabled": true,    // true or false
        "isUserActive": true,        // true or false
        "insertTime": 1570791523523,  // sub account create time
        "isMarginEnabled": true,     // true or false for margin
        "isFutureEnabled": true,      // true or false for futures.
        "mobile": 1570791523523      // user mobile number
    }
]
GET /sapi/v1/sub-account/status (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
email	STRING	NO	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
If no email sent, all sub-accounts' information will be returned.
Enable Margin for Sub-account (For Master Account)
Response
{

    "email":"123@test.com",
    "isMarginEnabled": true

}
POST /sapi/v1/sub-account/margin/enable (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Detail on Sub-account's Margin Account (For Master Account)
Response
{
      "email":"123@test.com",
      "marginLevel": "11.64405625",
      "totalAssetOfBtc": "6.82728457",
      "totalLiabilityOfBtc": "0.58633215",
      "totalNetAssetOfBtc": "6.24095242",
      "marginTradeCoeffVo": 
            {
                "forceLiquidationBar": "1.10000000",  // Liquidation margin ratio
                "marginCallBar": "1.50000000",        // Margin call margin ratio
                "normalBar": "2.00000000"             // Initial margin ratio
            },
      "marginUserAssetVoList": [
          {
              "asset": "BTC",
              "borrowed": "0.00000000",
              "free": "0.00499500",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00499500"
          },
          {
              "asset": "BNB",
              "borrowed": "201.66666672",
              "free": "2346.50000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "2144.83333328"
          },
          {
              "asset": "ETH",
              "borrowed": "0.00000000",
              "free": "0.00000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00000000"
          },
          {
              "asset": "USDT",
              "borrowed": "0.00000000",
              "free": "0.00000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00000000"
          }
      ]
}
GET /sapi/v1/sub-account/margin/account (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Summary of Sub-account's Margin Account (For Master Account)
Response
{
    "totalAssetOfBtc": "4.33333333", 
    "totalLiabilityOfBtc": "2.11111112", 
    "totalNetAssetOfBtc": "2.22222221",
    "subAccountList":[
        {
            "email":"123@test.com",
            "totalAssetOfBtc": "2.11111111",
            "totalLiabilityOfBtc": "1.11111111",
            "totalNetAssetOfBtc": "1.00000000"
        },
        { 
            "email":"345@test.com",
            "totalAssetOfBtc": "2.22222222", 
            "totalLiabilityOfBtc": "1.00000001", 
            "totalNetAssetOfBtc": "1.22222221"
        }
    ]
}
GET /sapi/v1/sub-account/margin/accountSummary (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Enable Futures for Sub-account (For Master Account)
Response
{

    "email":"123@test.com",
    "isFuturesEnabled": true  // true or false

}
POST /sapi/v1/sub-account/futures/enable (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Detail on Sub-account's Futures Account (For Master Account)
Response

{
    "email": "abc@test.com",
    "asset": "USDT",
    "assets":[
        {
            "asset": "USDT",
            "initialMargin": "0.00000000",
            "maintenanceMargin": "0.00000000",
            "marginBalance": "0.88308000",
            "maxWithdrawAmount": "0.88308000",
            "openOrderInitialMargin": "0.00000000",
            "positionInitialMargin": "0.00000000",
            "unrealizedProfit": "0.00000000",
            "walletBalance": "0.88308000"
         }
    ],
    "canDeposit": true,
    "canTrade": true,
    "canWithdraw": true,
    "feeTier": 2,
    "maxWithdrawAmount": "0.88308000",
    "totalInitialMargin": "0.00000000",
    "totalMaintenanceMargin": "0.00000000",
    "totalMarginBalance": "0.88308000",
    "totalOpenOrderInitialMargin": "0.00000000",
    "totalPositionInitialMargin": "0.00000000",
    "totalUnrealizedProfit": "0.00000000",
    "totalWalletBalance": "0.88308000",
    "updateTime": 1576756674610
 }

GET /sapi/v1/sub-account/futures/account (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Summary of Sub-account's Futures Account (For Master Account)
Response
{
    "totalInitialMargin": "9.83137400", 
    "totalMaintenanceMargin": "0.41568700", 
    "totalMarginBalance": "23.03235621", 
    "totalOpenOrderInitialMargin": "9.00000000",
    "totalPositionInitialMargin": "0.83137400",
    "totalUnrealizedProfit": "0.03219710",
    "totalWalletBalance": "22.15879444",
    "asset": "USD",  // The sum of BUSD and USDT
    "subAccountList":[
        {
            "email": "123@test.com",
            "totalInitialMargin": "9.00000000", 
            "totalMaintenanceMargin": "0.00000000", 
            "totalMarginBalance": "22.12659734", 
            "totalOpenOrderInitialMargin": "9.00000000",
            "totalPositionInitialMargin": "0.00000000",
            "totalUnrealizedProfit": "0.00000000",
            "totalWalletBalance": "22.12659734",
            "asset": "USD" //The sum of BUSD and USDT
        },
        { 
            "email": "345@test.com",
            "totalInitialMargin": "0.83137400", 
            "totalMaintenanceMargin": "0.41568700", 
            "totalMarginBalance": "0.90575887", 
            "totalOpenOrderInitialMargin": "0.00000000",
            "totalPositionInitialMargin": "0.83137400",
            "totalUnrealizedProfit": "0.03219710",
            "totalWalletBalance": "0.87356177",
            "asset": "USD"
        }
    ]
}

GET /sapi/v1/sub-account/futures/accountSummary (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Futures Position-Risk of Sub-account (For Master Account)
Response
[
    {
        "entryPrice": "9975.12000",
        "leverage": "50",              // current initial leverage
        "maxNotional": "1000000",      // notional value limit of current initial leverage
        "liquidationPrice": "7963.54",
        "markPrice": "9973.50770517",
        "positionAmount": "0.010",
        "symbol": "BTCUSDT",
        "unrealizedProfit": "-0.01612295"
    }
]
GET /sapi/v1/sub-account/futures/positionRisk (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
recvWindow	LONG	NO	
timestamp	LONG	YES	
Futures Transfer for Sub-account (For Master Account)
Response
{
    "txnId":"2966662589"
}
POST /sapi/v1/sub-account/futures/transfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
asset	STRING	YES	The asset being transferred, e.g., USDT
amount	DECIMAL	YES	The amount to be transferred
type	INT	YES	1: transfer from subaccount's spot account to its USDT-margined futures account 2: transfer from subaccount's USDT-margined futures account to its spot account 3: transfer from subaccount's spot account to its COIN-margined futures account 4:transfer from subaccount's COIN-margined futures account to its spot account
recvWindow	LONG	NO	
timestamp	LONG	YES	
Margin Transfer for Sub-account (For Master Account)
Response
{
    "txnId":"2966662589"
}
POST /sapi/v1/sub-account/margin/transfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
asset	STRING	YES	The asset being transferred, e.g., BTC
amount	DECIMAL	YES	The amount to be transferred
type	INT	YES	1: transfer from subaccount's spot account to margin account 2: transfer from subaccount's margin account to its spot account
recvWindow	LONG	NO	
timestamp	LONG	YES	
Transfer to Sub-account of Same Master (For Sub-account)
Response
{
    "txnId":"2966662589"
}
POST /sapi/v1/sub-account/transfer/subToSub (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
toEmail	STRING	YES	Sub-account email
asset	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Transfer to Master (For Sub-account)
Response
{
    "txnId":"2966662589"
}
POST /sapi/v1/sub-account/transfer/subToMaster (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Sub-account Transfer History (For Sub-account)
Response
[
  {
    "counterParty":"master",
    "email":"master@test.com",
    "type":1,  // 1 for transfer in, 2 for transfer out
    "asset":"BTC",
    "qty":"1",
    "fromAccountType":"SPOT",
    "toAccountType":"SPOT",
    "status":"SUCCESS",
    "tranId":11798835829,
    "time":1544433325000
  },
  {
    "counterParty":"subAccount",
    "email":"sub2@test.com",
    "type":1,                                 
    "asset":"ETH",
    "qty":"2",
    "fromAccountType":"SPOT",
    "toAccountType":"SPOT",
    "status":"SUCCESS",
    "tranId":11798829519,
    "time":1544433326000
  }
]
GET /sapi/v1/sub-account/transfer/subUserHistory (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	If not sent, result of all assets will be returned
type	INT	NO	1: transfer in, 2: transfer out
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
If type is not sent, the records of type 2: transfer out will be returned by default.
If startTime and endTime are not sent, the recent 30-day data will be returned.
Universal Transfer (For Master Account)
Response
{
    "tranId":11945860693,
    "clientTranId":"test"
}
POST /sapi/v1/sub-account/universalTransfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
fromEmail	STRING	NO	
toEmail	STRING	NO	
fromAccountType	STRING	YES	"SPOT","USDT_FUTURE","COIN_FUTURE"
toAccountType	STRING	YES	"SPOT","USDT_FUTURE","COIN_FUTURE"
clientTranId	STRING	NO	Must be unique
asset	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to enable "internal transfer" option for the api key which requests this endpoint.
Transfer from master account by default if fromEmail is not sent.
Transfer to master account by default if toEmail is not sent.
Transfer between futures accounts is not supported.
Query Universal Transfer History (For Master Account)
Response
{
    "result": [
        {
            "tranId": 92275823339,
            "fromEmail": "abctest@gmail.com",
            "toEmail": "deftest@gmail.com",
            "asset": "BNB",
            "amount": "0.01",
            "createTimeStamp": 1640317374000,
            "fromAccountType": "USDT_FUTURE",
            "toAccountType": "SPOT",
            "status": "SUCCESS",
            "clientTranId": "test"
        }
    ],
    "totalCount": 1
}
GET /sapi/v1/sub-account/universalTransfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
fromEmail	STRING	NO	
toEmail	STRING	NO	
clientTranId	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
page	INT	NO	Default 1
limit	INT	NO	Default 500, Max 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
fromEmail and toEmail cannot be sent at the same time.
Return fromEmail equal master account email by default.
Only get the latest history of past 30 days.
Get Detail on Sub-account's Futures Account V2 (For Master Account)
Response
USDT Margined Futures：

{
    "futureAccountResp": {
    "email": "abc@test.com",
    "assets":[
        {
            "asset": "USDT",
            "initialMargin": "0.00000000",
            "maintenanceMargin": "0.00000000",
            "marginBalance": "0.88308000",
            "maxWithdrawAmount": "0.88308000",
            "openOrderInitialMargin": "0.00000000",
            "positionInitialMargin": "0.00000000",
            "unrealizedProfit": "0.00000000",
            "walletBalance": "0.88308000"
         }
    ],
    "canDeposit": true,
    "canTrade": true,
    "canWithdraw": true,
    "feeTier": 2,
    "maxWithdrawAmount": "0.88308000",
    "totalInitialMargin": "0.00000000",
    "totalMaintenanceMargin": "0.00000000",
    "totalMarginBalance": "0.88308000",
    "totalOpenOrderInitialMargin": "0.00000000",
    "totalPositionInitialMargin": "0.00000000",
    "totalUnrealizedProfit": "0.00000000",
    "totalWalletBalance": "0.88308000",
    "updateTime": 1576756674610
 }
}
COIN Margined Futures：

{
    "deliveryAccountResp": {
        "email": "abc@test.com",
        "assets":[
            {
                "asset": "BTC",
                "initialMargin": "0.00000000",
                "maintenanceMargin": "0.00000000",
                "marginBalance": "0.88308000",
                "maxWithdrawAmount": "0.88308000",
                "openOrderInitialMargin": "0.00000000",
                "positionInitialMargin": "0.00000000",
                "unrealizedProfit": "0.00000000",
                "walletBalance": "0.88308000"
             }
        ],
        "canDeposit": true,
        "canTrade": true,
        "canWithdraw": true,
        "feeTier": 2,
        "updateTime": 1598959682001
    }
 }

GET /sapi/v2/sub-account/futures/account (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
futuresType	INT	YES	1:USDT Margined Futures, 2:COIN Margined Futures
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Summary of Sub-account's Futures Account V2 (For Master Account)
Response
USDT Margined Futures：
{
  "futureAccountSummaryResp": {
    "totalInitialMargin": "9.83137400", 
    "totalMaintenanceMargin": "0.41568700", 
    "totalMarginBalance": "23.03235621", 
    "totalOpenOrderInitialMargin": "9.00000000",
    "totalPositionInitialMargin": "0.83137400",
    "totalUnrealizedProfit": "0.03219710",
    "totalWalletBalance": "22.15879444",
    "asset": "USD",  //The sum of BUSD and USDT
    "subAccountList":[
        {
            "email": "123@test.com",
            "totalInitialMargin": "9.00000000", 
            "totalMaintenanceMargin": "0.00000000", 
            "totalMarginBalance": "22.12659734", 
            "totalOpenOrderInitialMargin": "9.00000000",
            "totalPositionInitialMargin": "0.00000000",
            "totalUnrealizedProfit": "0.00000000",
            "totalWalletBalance": "22.12659734",
            "asset": "USD"  //The sum of BUSD and USDT
        },
        { 
            "email": "345@test.com",
            "totalInitialMargin": "0.83137400", 
            "totalMaintenanceMargin": "0.41568700",
            "totalMarginBalance": "0.90575887",
            "totalOpenOrderInitialMargin": "0.00000000",
            "totalPositionInitialMargin": "0.83137400",
            "totalUnrealizedProfit": "0.03219710",
            "totalWalletBalance": "0.87356177",
            "asset": "USD"
        }
    ]
  }
}
COIN Margined Futures：
{
  "deliveryAccountSummaryResp": {
    "totalMarginBalanceOfBTC": "25.03221121", 
    "totalUnrealizedProfitOfBTC": "0.12233410",
    "totalWalletBalanceOfBTC": "22.15879444",
    "asset": "BTC",
    "subAccountList":[
        {
            "email": "123@test.com",
            "totalMarginBalance": "22.12659734", 
            "totalUnrealizedProfit": "0.00000000",
            "totalWalletBalance": "22.12659734",
            "asset": "BTC"
        },
        { 
            "email": "345@test.com",
            "totalMarginBalance": "0.90575887",
            "totalUnrealizedProfit": "0.03219710",
            "totalWalletBalance": "0.87356177",
            "asset": "BTC"
        }
    ]
  }
}
GET /sapi/v2/sub-account/futures/accountSummary (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
futuresType	INT	YES	1:USDT Margined Futures, 2:COIN Margined Futures
page	INT	NO	default:1
limit	INT	NO	default:10, max:20
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Futures Position-Risk of Sub-account V2 (For Master Account)
Response
USDT Margined Futures：
{
  "futurePositionRiskVos": [
     {
        "entryPrice": "9975.12000",
        "leverage": "50",              // current initial leverage
        "maxNotional": "1000000",      // notional value limit of current initial leverage
        "liquidationPrice": "7963.54",
        "markPrice": "9973.50770517",
        "positionAmount": "0.010",
        "symbol": "BTCUSDT",
        "unrealizedProfit": "-0.01612295"
     }
   ]
}
COIN Margined Futures：
{
  "deliveryPositionRiskVos": [
     {
        "entryPrice": "9975.12000",
        "markPrice": "9973.50770517",
        "leverage": "20",          
        "isolated": "false",                
        "isolatedWallet": "9973.50770517",
        "isolatedMargin": "0.00000000",
        "isAutoAddMargin": "false",
        "positionSide": "BOTH",
        "positionAmount": "1.230",
        "symbol": "BTCUSD_201225",
        "unrealizedProfit": "-0.01612295"
     }
   ]
}
GET /sapi/v2/sub-account/futures/positionRisk (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
futuresType	INT	YES	1:USDT Margined Futures, 2:COIN Margined Futures
recvWindow	LONG	NO	
timestamp	LONG	YES	
Enable Leverage Token for Sub-account (For Master Account)
Response
{
    "email":"123@test.com",
    "enableBlvt":true
}
POST /sapi/v1/sub-account/blvt/enable (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
enableBlvt	BOOLEAN	YES	Only true for now
recvWindow	LONG	NO	
timestamp	LONG	YES	
Enable or Disable IP Restriction for a Sub-account API Key (For Master Account)
Response:
{
    "ipRestrict": "true",  
    "ipList": [
        "0.0.0.0", // 0.0.0.0 is just an initial state reference (no extra meaning).You can use `POST /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList` to add an IP whitelist
    ],
    "updateTime": 1636369557189,
    "apiKey": "k5V49ldtn4tszj6W3hystegdfvmGbqDzjmkCtpTvC0G74WhK7yd4rfCTo4lShf"
}

POST /sapi/v1/sub-account/subAccountApi/ipRestriction (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
subAccountApiKey	STRING	YES	
ipRestrict	BOOLEAN	YES	true or false
recvWindow	LONG	NO	
timestamp	LONG	YES	
Add IP List for a Sub-account API Key (For Master Account)
Response:
{
    "ip": "8.34.21.101,5.24.40.1"，
    "updateTime": 1636369557189,
    "apiKey": "k5V49ldtn4tszj6W3hystegdfvmGbqDzjmkCtpTvC0G74WhK7yd4rfCTo4lShf"
}

POST /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList (HMAC SHA256)

Before the usage of this endpoint, please ensure POST /sapi/v1/sub-account/subAccountApi/ipRestriction was used to enable the IP restriction

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
subAccountApiKey	STRING	YES	
ipAddress	STRING	YES	Can be added in batches, separated by commas. Max 30 for an API key
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get IP Restriction for a Sub-account API Key (For Master Account)
Response:
{
    "ipRestrict": "true",
    "ipList": [
        "69.210.67.14",
        "8.34.21.10"
    ],
    "updateTime": 1636371437000,
    "apiKey": "k5V49ldtn4tszj6W3hystegdfvmGbqDzjmkCtpTvC0G74WhK7yd4rfCTo4lShf"
}
GET /sapi/v1/sub-account/subAccountApi/ipRestriction (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
subAccountApiKey	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Delete IP List for a Sub-account API Key (For Master Account)
Response:
{
    "ipRestrict": "true",
    "ipList": [
        "69.210.67.14",
    ],
    "updateTime": 1636371437000,
    "apiKey": "k5V49ldtn4tszj6W3hystegdfvmGbqDzjmkCtpTvC0G74WhK7yd4rfCTo4lShf"
}
DELETE /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	Sub-account email
subAccountApiKey	STRING	YES	
ipAddress	STRING	YES	Can be added in batches, separated by commas
recvWindow	LONG	NO	
timestamp	LONG	YES	
Deposit assets into the managed sub-account（For Investor Master Account）
Response
{
    "tranId":66157362489
}
POST /sapi/v1/managed-subaccount/deposit (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
toEmail	STRING	YES	
asset	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Query managed sub-account asset details（For Investor Master Account）
Response
[
  {
     "coin": "INJ",                
     "name": "Injective Protocol", 
     "totalBalance": "0",          
     "availableBalance": "0",      
     "inOrder": "0",                
     "btcValue": "0"               
  },
  {
     "coin": "FILDOWN",
     "name": "FILDOWN",
     "totalBalance": "0",
     "availableBalance": "0",
     "inOrder": "0",
     "btcValue": "0"
  }
]
GET /sapi/v1/managed-subaccount/asset (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
email	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Withdrawl assets from the managed sub-account（For Investor Master Account）
Response
{
    "tranId":66157362489
}
POST /sapi/v1/managed-subaccount/withdraw (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
fromEmail	STRING	YES	
asset	STRING	YES	
amount	DECIMAL	YES	
transferDate	LONG	NO	Withdrawals is automatically occur on the transfer date(UTC0). If a date is not selected, the withdrawal occurs right now
recvWindow	LONG	NO	
timestamp	LONG	YES	
Market Data Endpoints

Test Connectivity
Response:
{}
GET /api/v3/ping

Test connectivity to the Rest API.

Weight(IP): 1

Parameters:

NONE

Data Source: Memory

Check Server Time
Response:
{
  "serverTime": 1499827319559
}
GET /api/v3/time

Test connectivity to the Rest API and get the current server time.

Weight(IP): 1

Parameters:

NONE

Data Source: Memory

Exchange Information
Response:
{
  "timezone": "UTC",
  "serverTime": 1565246363776,
  "rateLimits": [
    {
      //These are defined in the `ENUM definitions` section under `Rate Limiters (rateLimitType)`.
      //All limits are optional
    }
  ],
  "exchangeFilters": [
    //These are the defined filters in the `Filters` section.
    //All filters are optional.
  ],
  "symbols": [
    {
      "symbol": "ETHBTC",
      "status": "TRADING",
      "baseAsset": "ETH",
      "baseAssetPrecision": 8,
      "quoteAsset": "BTC",
      "quotePrecision": 8,
      "quoteAssetPrecision": 8,
      "orderTypes": [
        "LIMIT",
        "LIMIT_MAKER",
        "MARKET",
        "STOP_LOSS",
        "STOP_LOSS_LIMIT",
        "TAKE_PROFIT",
        "TAKE_PROFIT_LIMIT"
      ],
      "icebergAllowed": true,
      "ocoAllowed": true,
      "isSpotTradingAllowed": true,
      "isMarginTradingAllowed": true,
      "filters": [
        //These are defined in the Filters section.
        //All filters are optional
      ],
      "permissions": [
         "SPOT",
         "MARGIN"
      ]
    }
  ]
}
GET /api/v3/exchangeInfo

Current exchange trading rules and symbol information

Weight(IP): 10

Parameters:

There are 3 possible options:

Options	Example
No parameter	curl -X GET "https://api.binance.com/api/v3/exchangeInfo"
symbol	curl -X GET "https://api.binance.com/api/v3/exchangeInfo?symbol=BNBBTC"
symbols	curl -X GET "https://api.binance.com/api/v3/exchangeInfo?symbols=%5B%22BNBBTC%22,%22BTCUSDT%22%5D" or curl -g GET 'https://api.binance.com/api/v3/exchangeInfo?symbols=["BTCUSDT","BNBBTC"]'
If any symbol provided in either symbol or symbols do not exist, the endpoint will throw an error.

Data Source: Memory

Order Book
Response:
{
  "lastUpdateId": 1027024,
  "bids": [
    [
      "4.00000000",     // PRICE
      "431.00000000"    // QTY
    ]
  ],
  "asks": [
    [
      "4.00000200",
      "12.00000000"
    ]
  ]
}
GET /api/v3/depth

Weight(IP):

Adjusted based on the limit:

Limit	Weight
5, 10, 20, 50, 100	1
500	5
1000	10
5000	50
Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
limit	INT	NO	Default 100; max 5000. Valid limits:[5, 10, 20, 50, 100, 500, 1000, 5000]
Data Source: Memory

Recent Trades List
Response:
[
  {
    "id": 28457,
    "price": "4.00000100",
    "qty": "12.00000000",
    "quoteQty": "48.000012",
    "time": 1499865549590,
    "isBuyerMaker": true,
    "isBestMatch": true
  }
]
GET /api/v3/trades

Get recent trades.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
limit	INT	NO	Default 500; max 1000.
Data Source: Memory

Old Trade Lookup (MARKET_DATA)
Response:
[
  {
    "id": 28457,
    "price": "4.00000100",
    "qty": "12.00000000",
    "quoteQty": "48.000012",
    "time": 1499865549590, // Trade executed timestamp, as same as `T` in the stream
    "isBuyerMaker": true,
    "isBestMatch": true
  }
]
GET /api/v3/historicalTrades

Get older market trades.

Weight(IP): 5

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
limit	INT	NO	Default 500; max 1000.
fromId	LONG	NO	Trade id to fetch from. Default gets most recent trades.
Data Source: Database

Compressed/Aggregate Trades List
Response:
[
  {
    "a": 26129,         // Aggregate tradeId
    "p": "0.01633102",  // Price
    "q": "4.70443515",  // Quantity
    "f": 27781,         // First tradeId
    "l": 27781,         // Last tradeId
    "T": 1498793709153, // Timestamp
    "m": true,          // Was the buyer the maker?
    "M": true           // Was the trade the best price match?
  }
]
GET /api/v3/aggTrades

Get compressed, aggregate trades. Trades that fill at the time, from the same order, with the same price will have the quantity aggregated.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
fromId	LONG	NO	id to get aggregate trades from INCLUSIVE.
startTime	LONG	NO	Timestamp in ms to get aggregate trades from INCLUSIVE.
endTime	LONG	NO	Timestamp in ms to get aggregate trades until INCLUSIVE.
limit	INT	NO	Default 500; max 1000.
If startTime and endTime are sent, time between startTime and endTime must be less than 1 hour.
If fromId, startTime, and endTime are not sent, the most recent aggregate trades will be returned.
Data Source: Database

Kline/Candlestick Data
Response:
[
  [
    1499040000000,      // Open time
    "0.01634790",       // Open
    "0.80000000",       // High
    "0.01575800",       // Low
    "0.01577100",       // Close
    "148976.11427815",  // Volume
    1499644799999,      // Close time
    "2434.19055334",    // Quote asset volume
    308,                // Number of trades
    "1756.87402397",    // Taker buy base asset volume
    "28.46694368",      // Taker buy quote asset volume
    "17928899.62484339" // Ignore.
  ]
]
GET /api/v3/klines

Kline/candlestick bars for a symbol.
Klines are uniquely identified by their open time.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
interval	ENUM	YES	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 500; max 1000.
If startTime and endTime are not sent, the most recent klines are returned.
Data Source: Database

Current Average Price
Response:
{
  "mins": 5,
  "price": "9.35751834"
}
GET /api/v3/avgPrice

Current average price for a symbol.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
Data Source: Memory

24hr Ticker Price Change Statistics
Response:
{
  "symbol": "BNBBTC",
  "priceChange": "-94.99999800",
  "priceChangePercent": "-95.960",
  "weightedAvgPrice": "0.29628482",
  "prevClosePrice": "0.10002000",
  "lastPrice": "4.00000200",
  "lastQty": "200.00000000",
  "bidPrice": "4.00000000",
  "bidQty": "100.00000000",
  "askPrice": "4.00000200",
  "askQty": "100.00000000",
  "openPrice": "99.00000000",
  "highPrice": "100.00000000",
  "lowPrice": "0.10000000",
  "volume": "8913.30000000",
  "quoteVolume": "15.30000000",
  "openTime": 1499783499040,
  "closeTime": 1499869899040,
  "firstId": 28385,   // First tradeId
  "lastId": 28460,    // Last tradeId
  "count": 76         // Trade count
}
OR
[
  {
    "symbol": "BNBBTC",
    "priceChange": "-94.99999800",
    "priceChangePercent": "-95.960",
    "weightedAvgPrice": "0.29628482",
    "prevClosePrice": "0.10002000",
    "lastPrice": "4.00000200",
    "lastQty": "200.00000000",
    "bidPrice": "4.00000000",
    "bidQty": "100.00000000",
    "askPrice": "4.00000200",
    "askQty": "100.00000000",
    "openPrice": "99.00000000",
    "highPrice": "100.00000000",
    "lowPrice": "0.10000000",
    "volume": "8913.30000000",
    "quoteVolume": "15.30000000",
    "openTime": 1499783499040,
    "closeTime": 1499869899040,
    "firstId": 28385,   // First tradeId
    "lastId": 28460,    // Last tradeId
    "count": 76         // Trade count
  }
]
GET /api/v3/ticker/24hr

24 hour rolling window price change statistics. Careful when accessing this with no symbol.

Weight(IP):

1 for a single symbol;
40 when the symbol parameter is omitted;

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
If the symbol is not sent, tickers for all symbols will be returned in an array.
Data Source: Memory

Symbol Price Ticker
Response:
{
  "symbol": "LTCBTC",
  "price": "4.00000200"
}
OR
[
  {
    "symbol": "LTCBTC",
    "price": "4.00000200"
  },
  {
    "symbol": "ETHBTC",
    "price": "0.07946600"
  }
]
GET /api/v3/ticker/price

Latest price for a symbol or symbols.

Weight(IP):

1 for a single symbol;
2 when the symbol parameter is omitted;

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
If the symbol is not sent, prices for all symbols will be returned in an array.
Data Source: Memory

Symbol Order Book Ticker
Response:
{
  "symbol": "LTCBTC",
  "bidPrice": "4.00000000",
  "bidQty": "431.00000000",
  "askPrice": "4.00000200",
  "askQty": "9.00000000"
}
OR
[
  {
    "symbol": "LTCBTC",
    "bidPrice": "4.00000000",
    "bidQty": "431.00000000",
    "askPrice": "4.00000200",
    "askQty": "9.00000000"
  },
  {
    "symbol": "ETHBTC",
    "bidPrice": "0.07946700",
    "bidQty": "9.00000000",
    "askPrice": "100000.00000000",
    "askQty": "1000.00000000"
  }
]
GET /api/v3/ticker/bookTicker

Best price/qty on the order book for a symbol or symbols.

Weight(IP):

1 for a single symbol;
2 when the symbol parameter is omitted;

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
If the symbol is not sent, bookTickers for all symbols will be returned in an array.
Data Source: Memory

Websocket Market Streams

The base endpoint is: wss://stream.binance.com:9443
Streams can be accessed either in a single raw stream or in a combined stream
Raw streams are accessed at /ws/<streamName>
Combined streams are accessed at /stream?streams=<streamName1>/<streamName2>/<streamName3>
Combined stream events are wrapped as follows: {"stream":"<streamName>","data":<rawPayload>}
All symbols for streams are lowercase
A single connection to stream.binance.com is only valid for 24 hours; expect to be disconnected at the 24 hour mark
The websocket server will send a ping frame every 3 minutes. If the websocket server does not receive a pong frame back from the connection within a 10 minute period, the connection will be disconnected. Unsolicited pong frames are allowed.
Live Subscribing/Unsubscribing to streams
The following data can be sent through the websocket instance in order to subscribe/unsubscribe from streams. Examples can be seen below.
The id used in the JSON payloads is an unsigned INT used as an identifier to uniquely identify the messages going back and forth.
In the response, if the result received is null this means the request sent was a success.
Subscribe to a stream

Response
  {
    "result": null,  
    "id": 1
  }
Request

{
"method": "SUBSCRIBE",
"params":
[
"btcusdt@aggTrade",
"btcusdt@depth"
],
"id": 1
}

Unsubscribe to a stream

Response
  {
    "result": null,
    "id": 312
  }
Request
{
"method": "UNSUBSCRIBE",
"params":
[
"btcusdt@depth"
],
"id": 312
}

Listing Subscriptions

Response
  {
    "result": [
      "btcusdt@aggTrade"
    ],
    "id": 3
  }
Request
{
"method": "LIST_SUBSCRIPTIONS",
"id": 3
}

Setting Properties

Currently, the only property can be set is to set whether combined stream payloads are enabled or not. The combined property is set to false when connecting using /ws/ ("raw streams") and true when connecting using /stream/.

Response
{
  "result": null,
  "id": 5
}
Request
{
"method": "SET_PROPERTY",
"params":
[
"combined",
true
],
"id": 5
}

Retrieving Properties

Response
  {
    "result": true, // Indicates that combined is set to true.
    "id": 2
  }
Request
{
"method": "GET_PROPERTY",
"params":
[
"combined"
],
"id": 2
}

Error Messages

Error Message	Description
{"code": 0, "msg": "Unknown property", "id": '%s'}	Parameter used in the SET_PROPERTY or GET_PROPERTY was invalid
{"code": 1, "msg": "Invalid value type: expected Boolean", "id": '%s'}	Value should only be true or false
{"code": 2, "msg": "Invalid request: property name must be a string"}	Property name provided was invalid
{"code": 2, "msg": "Invalid request: request ID must be an unsigned integer"}	Parameter id had to be provided or the value provided in the id parameter is an unsupported type
{"code": 2, "msg": "Invalid request: unknown variant %s, expected one of SUBSCRIBE, UNSUBSCRIBE, LIST_SUBSCRIPTIONS, SET_PROPERTY, GET_PROPERTY at line 1 column 28"}	Possible typo in the provided method or provided method was neither of the expected values
{"code": 2, "msg": "Invalid request: too many parameters"}	Unnecessary parameters provided in the data
{"code": 2, "msg": "Invalid request: property name must be a string"}	Property name was not provided
{"code": 2, "msg": "Invalid request: missing field method at line 1 column 73"}	method was not provided in the data
{"code":3,"msg":"Invalid JSON: expected value at line %s column %s"}	JSON data sent has incorrect syntax.
Aggregate Trade Streams
Payload:
{
  "e": "aggTrade",  // Event type
  "E": 123456789,   // Event time
  "s": "BNBBTC",    // Symbol
  "a": 12345,       // Aggregate trade ID
  "p": "0.001",     // Price
  "q": "100",       // Quantity
  "f": 100,         // First trade ID
  "l": 105,         // Last trade ID
  "T": 123456785,   // Trade time
  "m": true,        // Is the buyer the market maker?
  "M": true         // Ignore
}
The Aggregate Trade Streams push trade information that is aggregated for a single taker order.

Stream Name: <symbol>@aggTrade

Update Speed: Real-time

Trade Streams
Payload:
{
  "e": "trade",     // Event type
  "E": 123456789,   // Event time
  "s": "BNBBTC",    // Symbol
  "t": 12345,       // Trade ID
  "p": "0.001",     // Price
  "q": "100",       // Quantity
  "b": 88,          // Buyer order ID
  "a": 50,          // Seller order ID
  "T": 123456785,   // Trade time
  "m": true,        // Is the buyer the market maker?
  "M": true         // Ignore
}
The Trade Streams push raw trade information; each trade has a unique buyer and seller.

Stream Name: <symbol>@trade

Update Speed: Real-time

Kline/Candlestick Streams
Payload:
{
  "e": "kline",     // Event type
  "E": 123456789,   // Event time
  "s": "BNBBTC",    // Symbol
  "k": {
    "t": 123400000, // Kline start time
    "T": 123460000, // Kline close time
    "s": "BNBBTC",  // Symbol
    "i": "1m",      // Interval
    "f": 100,       // First trade ID
    "L": 200,       // Last trade ID
    "o": "0.0010",  // Open price
    "c": "0.0020",  // Close price
    "h": "0.0025",  // High price
    "l": "0.0015",  // Low price
    "v": "1000",    // Base asset volume
    "n": 100,       // Number of trades
    "x": false,     // Is this kline closed?
    "q": "1.0000",  // Quote asset volume
    "V": "500",     // Taker buy base asset volume
    "Q": "0.500",   // Taker buy quote asset volume
    "B": "123456"   // Ignore
  }
}
The Kline/Candlestick Stream push updates to the current klines/candlestick every second.

Stream Name: <symbol>@kline_<interval>

Update Speed: 2000ms

Kline/Candlestick chart intervals:

m -> minutes; h -> hours; d -> days; w -> weeks; M -> months

1m
3m
5m
15m
30m
1h
2h
4h
6h
8h
12h
1d
3d
1w
1M
Individual Symbol Mini Ticker Stream
Payload:
  {
    "e": "24hrMiniTicker",  // Event type
    "E": 123456789,         // Event time
    "s": "BNBBTC",          // Symbol
    "c": "0.0025",          // Close price
    "o": "0.0010",          // Open price
    "h": "0.0025",          // High price
    "l": "0.0010",          // Low price
    "v": "10000",           // Total traded base asset volume
    "q": "18"               // Total traded quote asset volume
  }
24hr rolling window mini-ticker statistics. These are NOT the statistics of the UTC day, but a 24hr rolling window for the previous 24hrs.

Stream Name: <symbol>@miniTicker

Update Speed: 1000ms

All Market Mini Tickers Stream
Payload:
[
  {
    // Same as <symbol>@miniTicker payload
  }
]
24hr rolling window mini-ticker statistics for all symbols that changed in an array. These are NOT the statistics of the UTC day, but a 24hr rolling window for the previous 24hrs. Note that only tickers that have changed will be present in the array.

Stream Name: !miniTicker@arr

Update Speed: 1000ms

Individual Symbol Ticker Streams
Payload:
{
  "e": "24hrTicker",  // Event type
  "E": 123456789,     // Event time
  "s": "BNBBTC",      // Symbol
  "p": "0.0015",      // Price change
  "P": "250.00",      // Price change percent
  "w": "0.0018",      // Weighted average price
  "x": "0.0009",      // First trade(F)-1 price (first trade before the 24hr rolling window)
  "c": "0.0025",      // Last price
  "Q": "10",          // Last quantity
  "b": "0.0024",      // Best bid price
  "B": "10",          // Best bid quantity
  "a": "0.0026",      // Best ask price
  "A": "100",         // Best ask quantity
  "o": "0.0010",      // Open price
  "h": "0.0025",      // High price
  "l": "0.0010",      // Low price
  "v": "10000",       // Total traded base asset volume
  "q": "18",          // Total traded quote asset volume
  "O": 0,             // Statistics open time
  "C": 86400000,      // Statistics close time
  "F": 0,             // First trade ID
  "L": 18150,         // Last trade Id
  "n": 18151          // Total number of trades
}
24hr rolling window ticker statistics for a single symbol. These are NOT the statistics of the UTC day, but a 24hr rolling window for the previous 24hrs.

Stream Name: <symbol>@ticker

Update Speed: 1000ms

All Market Tickers Stream
Payload:
[
  {
    // Same as <symbol>@ticker payload
  }
]
24hr rolling window ticker statistics for all symbols that changed in an array. These are NOT the statistics of the UTC day, but a 24hr rolling window for the previous 24hrs. Note that only tickers that have changed will be present in the array.

Stream Name: !ticker@arr

Update Speed: 1000ms

Individual Symbol Book Ticker Streams
Payload:
{
  "u":400900217,     // order book updateId
  "s":"BNBUSDT",     // symbol
  "b":"25.35190000", // best bid price
  "B":"31.21000000", // best bid qty
  "a":"25.36520000", // best ask price
  "A":"40.66000000"  // best ask qty
}
Pushes any update to the best bid or ask's price or quantity in real-time for a specified symbol.

Stream Name: <symbol>@bookTicker

Update Speed: Real-time

All Book Tickers Stream
Payload:
{
  // Same as <symbol>@bookTicker payload
}
Pushes any update to the best bid or ask's price or quantity in real-time for all symbols.

Stream Name: !bookTicker

Update Speed: Real-time

Partial Book Depth Streams
Payload:
{
  "lastUpdateId": 160,  // Last update ID
  "bids": [             // Bids to be updated
    [
      "0.0024",         // Price level to be updated
      "10"              // Quantity
    ]
  ],
  "asks": [             // Asks to be updated
    [
      "0.0026",         // Price level to be updated
      "100"             // Quantity
    ]
  ]
}
Top bids and asks, Valid are 5, 10, or 20.

Stream Names: <symbol>@depth<levels> OR <symbol>@depth<levels>@100ms.

Update Speed: 1000ms or 100ms

Diff. Depth Stream
Payload:
{
  "e": "depthUpdate", // Event type
  "E": 123456789,     // Event time
  "s": "BNBBTC",      // Symbol
  "U": 157,           // First update ID in event
  "u": 160,           // Final update ID in event
  "b": [              // Bids to be updated
    [
      "0.0024",       // Price level to be updated
      "10"            // Quantity
    ]
  ],
  "a": [              // Asks to be updated
    [
      "0.0026",       // Price level to be updated
      "100"           // Quantity
    ]
  ]
}
Stream Name: <symbol>@depth OR <symbol>@depth@100ms

Update Speed: 1000ms or 100ms

Order book price and quantity depth updates used to locally manage an order book.

How to manage a local order book correctly
Open a stream to wss://stream.binance.com:9443/ws/bnbbtc@depth.
Buffer the events you receive from the stream.
Get a depth snapshot from https://api.binance.com/api/v3/depth?symbol=BNBBTC&limit=1000 .
Drop any event where u is <= lastUpdateId in the snapshot.
The first processed event should have U <= lastUpdateId+1 AND u >= lastUpdateId+1.
While listening to the stream, each new event's U should be equal to the previous event's u+1.
The data in each event is the absolute quantity for a price level.
If the quantity is 0, remove the price level.
Receiving an event that removes a price level that is not in your local order book can happen and is normal.
Spot Account/Trade

Test New Order (TRADE)
Response:
{}
POST /api/v3/order/test (HMAC SHA256)

Test new order creation and signature/recvWindow long. Creates and validates a new order but does not send it into the matching engine.

Weight: 1

Parameters:

Same as POST /api/v3/order

Data Source: Memory

New Order (TRADE)
Response ACK:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "orderListId": -1, //Unless OCO, value will be -1
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "transactTime": 1507725176595
}
Response RESULT:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "orderListId": -1, //Unless OCO, value will be -1
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "transactTime": 1507725176595,
  "price": "0.00000000",
  "origQty": "10.00000000",
  "executedQty": "10.00000000",
  "cummulativeQuoteQty": "10.00000000",
  "status": "FILLED",
  "timeInForce": "GTC",
  "type": "MARKET",
  "side": "SELL"
}
Response FULL:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "orderListId": -1, //Unless OCO, value will be -1
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "transactTime": 1507725176595,
  "price": "0.00000000",
  "origQty": "10.00000000",
  "executedQty": "10.00000000",
  "cummulativeQuoteQty": "10.00000000",
  "status": "FILLED",
  "timeInForce": "GTC",
  "type": "MARKET",
  "side": "SELL",
  "fills": [
    {
      "price": "4000.00000000",
      "qty": "1.00000000",
      "commission": "4.00000000",
      "commissionAsset": "USDT",
      "tradeId": 56
    },
    {
      "price": "3999.00000000",
      "qty": "5.00000000",
      "commission": "19.99500000",
      "commissionAsset": "USDT",
      "tradeId": 57
    },
    {
      "price": "3998.00000000",
      "qty": "2.00000000",
      "commission": "7.99600000",
      "commissionAsset": "USDT",
      "tradeId": 58
    },
    {
      "price": "3997.00000000",
      "qty": "1.00000000",
      "commission": "3.99700000",
      "commissionAsset": "USDT",
      "tradeId": 59
    },
    {
      "price": "3995.00000000",
      "qty": "1.00000000",
      "commission": "3.99500000",
      "commissionAsset": "USDT",
      "tradeId": 60
    }
  ]
}
POST /api/v3/order (HMAC SHA256)

Send in a new order.

Weight(UID): 1 Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
side	ENUM	YES	
type	ENUM	YES	
timeInForce	ENUM	NO	
quantity	DECIMAL	NO	
quoteOrderQty	DECIMAL	NO	
price	DECIMAL	NO	
newClientOrderId	STRING	NO	A unique id among open orders. Automatically generated if not sent.
stopPrice	DECIMAL	NO	Used with STOP_LOSS, STOP_LOSS_LIMIT, TAKE_PROFIT, and TAKE_PROFIT_LIMIT orders.
icebergQty	DECIMAL	NO	Used with LIMIT, STOP_LOSS_LIMIT, and TAKE_PROFIT_LIMIT to create an iceberg order.
newOrderRespType	ENUM	NO	Set the response JSON. ACK, RESULT, or FULL; MARKET and LIMIT order types default to FULL, all other orders default to ACK.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Additional mandatory parameters based on type:

Type	Additional mandatory parameters
LIMIT	timeInForce, quantity, price
MARKET	quantity or quoteOrderQty
STOP_LOSS	quantity, stopPrice
STOP_LOSS_LIMIT	timeInForce, quantity, price, stopPrice
TAKE_PROFIT	quantity, stopPrice
TAKE_PROFIT_LIMIT	timeInForce, quantity, price, stopPrice
LIMIT_MAKER	quantity, price
Other info:

LIMIT_MAKER are LIMIT orders that will be rejected if they would immediately match and trade as a taker.
STOP_LOSS and TAKE_PROFIT will execute a MARKET order when the stopPrice is reached.
Any LIMIT or LIMIT_MAKER type order can be made an iceberg order by sending an icebergQty.
Any order with an icebergQty MUST have timeInForce set to GTC.
MARKET orders using the quantity field specifies the amount of the base asset the user wants to buy or sell at the market price.
For example, sending a MARKET order on BTCUSDT will specify how much BTC the user is buying or selling.
MARKET orders using quoteOrderQty specifies the amount the user wants to spend (when buying) or receive (when selling) the quote asset; the correct quantity will be determined based on the market liquidity and quoteOrderQty.
Using BTCUSDT as an example:
On the BUY side, the order will buy as many BTC as quoteOrderQty USDT can.
On the SELL side, the order will sell as much BTC needed to receive quoteOrderQty USDT.
MARKET orders using quoteOrderQty will not break LOT_SIZE filter rules; the order will execute a quantity that will have the notional value as close as possible to quoteOrderQty.
same newClientOrderId can be accepted only when the previous one is filled, otherwise the order will be rejected.
Trigger order price rules against market price for both MARKET and LIMIT versions:

Price above market price: STOP_LOSS BUY, TAKE_PROFIT SELL
Price below market price: STOP_LOSS SELL, TAKE_PROFIT BUY
Data Source: Matching Engine

Cancel Order (TRADE)
Response:
{
  "symbol": "LTCBTC",
  "origClientOrderId": "myOrder1",
  "orderId": 4,
  "orderListId": -1, //Unless part of an OCO, the value will always be -1.
  "clientOrderId": "cancelMyOrder1",
  "price": "2.00000000",
  "origQty": "1.00000000",
  "executedQty": "0.00000000",
  "cummulativeQuoteQty": "0.00000000",
  "status": "CANCELED",
  "timeInForce": "GTC",
  "type": "LIMIT",
  "side": "BUY"
}
DELETE /api/v3/order (HMAC SHA256)

Cancel an active order.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
orderId	LONG	NO	
origClientOrderId	STRING	NO	
newClientOrderId	STRING	NO	Used to uniquely identify this cancel. Automatically generated by default.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Either orderId or origClientOrderId must be sent.

Data Source: Matching Engine

Cancel all Open Orders on a Symbol (TRADE)
Response:
[
  {
    "symbol": "BTCUSDT",
    "origClientOrderId": "E6APeyTJvkMvLMYMqu1KQ4",
    "orderId": 11,
    "orderListId": -1,
    "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
    "price": "0.089853",
    "origQty": "0.178622",
    "executedQty": "0.000000",
    "cummulativeQuoteQty": "0.000000",
    "status": "CANCELED",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY"
  },
  {
    "symbol": "BTCUSDT",
    "origClientOrderId": "A3EF2HCwxgZPFMrfwbgrhv",
    "orderId": 13,
    "orderListId": -1,
    "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
    "price": "0.090430",
    "origQty": "0.178622",
    "executedQty": "0.000000",
    "cummulativeQuoteQty": "0.000000",
    "status": "CANCELED",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY"
  },
  {
    "orderListId": 1929,
    "contingencyType": "OCO",
    "listStatusType": "ALL_DONE",
    "listOrderStatus": "ALL_DONE",
    "listClientOrderId": "2inzWQdDvZLHbbAmAozX2N",
    "transactionTime": 1585230948299,
    "symbol": "BTCUSDT",
    "orders": [
      {
        "symbol": "BTCUSDT",
        "orderId": 20,
        "clientOrderId": "CwOOIPHSmYywx6jZX77TdL"
      },
      {
        "symbol": "BTCUSDT",
        "orderId": 21,
        "clientOrderId": "461cPg51vQjV3zIMOXNz39"
      }
    ],
    "orderReports": [
      {
        "symbol": "BTCUSDT",
        "origClientOrderId": "CwOOIPHSmYywx6jZX77TdL",
        "orderId": 20,
        "orderListId": 1929,
        "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
        "price": "0.668611",
        "origQty": "0.690354",
        "executedQty": "0.000000",
        "cummulativeQuoteQty": "0.000000",
        "status": "CANCELED",
        "timeInForce": "GTC",
        "type": "STOP_LOSS_LIMIT",
        "side": "BUY",
        "stopPrice": "0.378131",
        "icebergQty": "0.017083"
      },
      {
        "symbol": "BTCUSDT",
        "origClientOrderId": "461cPg51vQjV3zIMOXNz39",
        "orderId": 21,
        "orderListId": 1929,
        "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
        "price": "0.008791",
        "origQty": "0.690354",
        "executedQty": "0.000000",
        "cummulativeQuoteQty": "0.000000",
        "status": "CANCELED",
        "timeInForce": "GTC",
        "type": "LIMIT_MAKER",
        "side": "BUY",
        "icebergQty": "0.639962"
      }
    ]
  }
]
DELETE /api/v3/openOrders

Cancels all active orders on a symbol.
This includes OCO orders.

Weight(IP): 1

Parameters

Name	Type	Mandatory	Description
symbol	STRING	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Matching Engine

Query Order (USER_DATA)
Response:
{
  "symbol": "LTCBTC",
  "orderId": 1,
  "orderListId": -1, //Unless OCO, value will be -1
  "clientOrderId": "myOrder1",
  "price": "0.1",
  "origQty": "1.0",
  "executedQty": "0.0",
  "cummulativeQuoteQty": "0.0",
  "status": "NEW",
  "timeInForce": "GTC",
  "type": "LIMIT",
  "side": "BUY",
  "stopPrice": "0.0",
  "icebergQty": "0.0",
  "time": 1499827319559,
  "updateTime": 1499827319559,
  "isWorking": true,
  "origQuoteOrderQty": "0.000000"
}
GET /api/v3/order (HMAC SHA256)

Check an order's status.

Weight(IP): 2

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
orderId	LONG	NO	
origClientOrderId	STRING	NO	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Notes:

Either orderId or origClientOrderId must be sent.
For some historical orders cummulativeQuoteQty will be < 0, meaning the data is not available at this time.
Data Source: Database

Current Open Orders (USER_DATA)
Response:
[
  {
    "symbol": "LTCBTC",
    "orderId": 1,
    "orderListId": -1, //Unless OCO, the value will always be -1
    "clientOrderId": "myOrder1",
    "price": "0.1",
    "origQty": "1.0",
    "executedQty": "0.0",
    "cummulativeQuoteQty": "0.0",
    "status": "NEW",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY",
    "stopPrice": "0.0",
    "icebergQty": "0.0",
    "time": 1499827319559,
    "updateTime": 1499827319559,
    "isWorking": true,
    "origQuoteOrderQty": "0.000000"
  }
]
GET /api/v3/openOrders (HMAC SHA256)

Get all open orders on a symbol. Careful when accessing this with no symbol.

Weight(IP): 3 for a single symbol; 40 when the symbol parameter is omitted;

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If the symbol is not sent, orders for all symbols will be returned in an array.
Data Source: Database

All Orders (USER_DATA)
Response:
[
  {
    "symbol": "LTCBTC",
    "orderId": 1,
    "orderListId": -1, //Unless OCO, the value will always be -1
    "clientOrderId": "myOrder1",
    "price": "0.1",
    "origQty": "1.0",
    "executedQty": "0.0",
    "cummulativeQuoteQty": "0.0",
    "status": "NEW",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY",
    "stopPrice": "0.0",
    "icebergQty": "0.0",
    "time": 1499827319559,
    "updateTime": 1499827319559,
    "isWorking": true,
    "origQuoteOrderQty": "0.000000"
  }
]
GET /api/v3/allOrders (HMAC SHA256)

Get all account orders; active, canceled, or filled.

Weight(IP): 10 with symbol

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
orderId	LONG	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 500; max 1000.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Notes:

If orderId is set, it will get orders >= that orderId. Otherwise most recent orders are returned.
For some historical orders cummulativeQuoteQty will be < 0, meaning the data is not available at this time.
If startTime and/or endTime provided, orderId is not required.
Data Source: Database

New OCO (TRADE)
Response:
{
  "orderListId": 0,
  "contingencyType": "OCO",
  "listStatusType": "EXEC_STARTED",
  "listOrderStatus": "EXECUTING",
  "listClientOrderId": "JYVpp3F0f5CAG15DhtrqLp",
  "transactionTime": 1563417480525,
  "symbol": "LTCBTC",
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "clientOrderId": "Kk7sqHb9J6mJWTMDVW7Vos"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "clientOrderId": "xTXKaGYd4bluPVp78IVRvl"
    }
  ],
  "orderReports": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "orderListId": 0,
      "clientOrderId": "Kk7sqHb9J6mJWTMDVW7Vos",
      "transactTime": 1563417480525,
      "price": "0.000000",
      "origQty": "0.624363",
      "executedQty": "0.000000",
      "cummulativeQuoteQty": "0.000000",
      "status": "NEW",
      "timeInForce": "GTC",
      "type": "STOP_LOSS",
      "side": "BUY",
      "stopPrice": "0.960664"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "orderListId": 0,
      "clientOrderId": "xTXKaGYd4bluPVp78IVRvl",
      "transactTime": 1563417480525,
      "price": "0.036435",
      "origQty": "0.624363",
      "executedQty": "0.000000",
      "cummulativeQuoteQty": "0.000000",
      "status": "NEW",
      "timeInForce": "GTC",
      "type": "LIMIT_MAKER",
      "side": "BUY"
    }
  ]
}
POST /api/v3/order/oco (HMAC SHA256)

Send in a new OCO

Weight(UID): 2 Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
listClientOrderId	STRING	NO	A unique Id for the entire orderList
side	ENUM	YES	
quantity	DECIMAL	YES	
limitClientOrderId	STRING	NO	A unique Id for the limit order
price	DECIMAL	YES	
limitIcebergQty	DECIMAL	NO	
stopClientOrderId	STRING	NO	A unique Id for the stop loss/stop loss limit leg
stopPrice	DECIMAL	YES	
stopLimitPrice	DECIMAL	NO	If provided, stopLimitTimeInForce is required.
stopIcebergQty	DECIMAL	NO	
stopLimitTimeInForce	ENUM	NO	Valid values are GTC/FOK/IOC
newOrderRespType	ENUM	NO	Set the response JSON.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Other Info:

Price Restrictions:
SELL: Limit Price > Last Price > Stop Price
BUY: Limit Price < Last Price < Stop Price
Quantity Restrictions:
Both legs must have the same quantity
ICEBERG quantities however do not have to be the same.
Order Rate Limit
OCO counts as 2 orders against the order rate limit.
Data Source: Matching Engine

Cancel OCO (TRADE)
Response:
{
  "orderListId": 0,
  "contingencyType": "OCO",
  "listStatusType": "ALL_DONE",
  "listOrderStatus": "ALL_DONE",
  "listClientOrderId": "C3wyj4WVEktd7u9aVBRXcN",
  "transactionTime": 1574040868128,
  "symbol": "LTCBTC",
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "clientOrderId": "pO9ufTiFGg3nw2fOdgeOXa"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "clientOrderId": "TXOvglzXuaubXAaENpaRCB"
    }
  ],
  "orderReports": [
    {
      "symbol": "LTCBTC",
      "origClientOrderId": "pO9ufTiFGg3nw2fOdgeOXa",
      "orderId": 2,
      "orderListId": 0,
      "clientOrderId": "unfWT8ig8i0uj6lPuYLez6",
      "price": "1.00000000",
      "origQty": "10.00000000",
      "executedQty": "0.00000000",
      "cummulativeQuoteQty": "0.00000000",
      "status": "CANCELED",
      "timeInForce": "GTC",
      "type": "STOP_LOSS_LIMIT",
      "side": "SELL",
      "stopPrice": "1.00000000"
    },
    {
      "symbol": "LTCBTC",
      "origClientOrderId": "TXOvglzXuaubXAaENpaRCB",
      "orderId": 3,
      "orderListId": 0,
      "clientOrderId": "unfWT8ig8i0uj6lPuYLez6",
      "price": "3.00000000",
      "origQty": "10.00000000",
      "executedQty": "0.00000000",
      "cummulativeQuoteQty": "0.00000000",
      "status": "CANCELED",
      "timeInForce": "GTC",
      "type": "LIMIT_MAKER",
      "side": "SELL"
    }
  ]
}
DELETE /api/v3/orderList (HMAC SHA256) Cancel an entire Order List.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
orderListId	LONG	NO	Either orderListId or listClientOrderId must be provided
listClientOrderId	STRING	NO	Either orderListId or listClientOrderId must be provided
newClientOrderId	STRING	NO	Used to uniquely identify this cancel. Automatically generated by default
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Additional notes:

Canceling an individual leg will cancel the entire OCO
Data Source: Matching Engine

Query OCO (USER_DATA)
Response:
{
  "orderListId": 27,
  "contingencyType": "OCO",
  "listStatusType": "EXEC_STARTED",
  "listOrderStatus": "EXECUTING",
  "listClientOrderId": "h2USkA5YQpaXHPIrkd96xE",
  "transactionTime": 1565245656253,
  "symbol": "LTCBTC",
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 4,
      "clientOrderId": "qD1gy3kc3Gx0rihm9Y3xwS"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 5,
      "clientOrderId": "ARzZ9I00CPM8i3NhmU9Ega"
    }
  ]
}
GET /api/v3/orderList (HMAC SHA256)

Retrieves a specific OCO based on provided optional parameters

Weight(IP): 2

Parameters:

Name	Type	Mandatory	Description
orderListId	LONG	NO	Either orderListId or origClientOrderId must be provided
origClientOrderId	STRING	NO	Either orderListId or origClientOrderId must be provided
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Database

Query all OCO (USER_DATA)
Response:
[
  {
    "orderListId": 29,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "amEEAXryFzFwYF1FeRpUoZ",
    "transactionTime": 1565245913483,
    "symbol": "LTCBTC",
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 4,
        "clientOrderId": "oD7aesZqjEGlZrbtRpy5zB"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 5,
        "clientOrderId": "Jr1h6xirOxgeJOUuYQS7V3"
      }
    ]
  },
  {
    "orderListId": 28,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "hG7hFNxJV6cZy3Ze4AUT4d",
    "transactionTime": 1565245913407,
    "symbol": "LTCBTC",
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 2,
        "clientOrderId": "j6lFOfbmFMRjTYA7rRJ0LP"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 3,
        "clientOrderId": "z0KCjOdditiLS5ekAFtK81"
      }
    ]
  }
]
GET /api/v3/allOrderList (HMAC SHA256)

Retrieves all OCO based on provided optional parameters

Weight(IP): 10

Parameters

Name	Type	Mandatory	Description
fromId	LONG	NO	If supplied, neither startTime or endTime can be provided
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default Value: 500; Max Value: 1000
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Database

Query Open OCO (USER_DATA)
Response:
[
  {
    "orderListId": 31,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "wuB13fmulKj3YjdqWEcsnp",
    "transactionTime": 1565246080644,
    "symbol": "LTCBTC",
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 4,
        "clientOrderId": "r3EH2N76dHfLoSZWIUw1bT"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 5,
        "clientOrderId": "Cv1SnyPD3qhqpbjpYEHbd2"
      }
    ]
  }
]
GET /api/v3/openOrderList (HMAC SHA256)

Weight(IP): 3

Parameters

Name	Type	Mandatory	Description
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Database

Account Information (USER_DATA)
Response:
{
  "makerCommission": 15,
  "takerCommission": 15,
  "buyerCommission": 0,
  "sellerCommission": 0,
  "canTrade": true,
  "canWithdraw": true,
  "canDeposit": true,
  "updateTime": 123456789,
  "accountType": "SPOT",
  "balances": [
    {
      "asset": "BTC",
      "free": "4723846.89208129",
      "locked": "0.00000000"
    },
    {
      "asset": "LTC",
      "free": "4763368.68006011",
      "locked": "0.00000000"
    }
  ],
  "permissions": [
    "SPOT"
  ]
}
GET /api/v3/account (HMAC SHA256)

Get current account information.

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Memory => Database

Account Trade List (USER_DATA)
Response:
[
  {
    "symbol": "BNBBTC",
    "id": 28457,
    "orderId": 100234,
    "orderListId": -1, //Unless OCO, the value will always be -1
    "price": "4.00000100",
    "qty": "12.00000000",
    "quoteQty": "48.000012",
    "commission": "10.10000000",
    "commissionAsset": "BNB",
    "time": 1499865549590,
    "isBuyer": true,
    "isMaker": false,
    "isBestMatch": true
  }
]
GET /api/v3/myTrades (HMAC SHA256)

Get trades for a specific account and symbol.

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
orderId	LONG	NO	This can only be used in combination with symbol.
startTime	LONG	NO	
endTime	LONG	NO	
fromId	LONG	NO	TradeId to fetch from. Default gets most recent trades.
limit	INT	NO	Default 500; max 1000.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Notes:

If fromId is set, it will get id >= that fromId. Otherwise most recent trades are returned.
Data Source: Database

Query Current Order Count Usage (TRADE)
Response:
[

  {
    "rateLimitType": "ORDERS",
    "interval": "SECOND",
    "intervalNum": 10,
    "limit": 10000,
    "count": 0
  },
  {
    "rateLimitType": "ORDERS",
    "interval": "DAY",
    "intervalNum": 1,
    "limit": 20000,
    "count": 0
  }
]
GET /api/v3/rateLimit/order

Displays the user's current order count usage for all intervals.

Weight(IP): 20

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Data Source: Memory

Margin Account/Trade

Cross Margin Account Transfer (MARGIN)
Response:
{
    //transaction id
    "tranId": 100000001
}
POST /sapi/v1/margin/transfer (HMAC SHA256)

Execute transfer between spot account and cross margin account.

Weight(IP): 600

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	The asset being transferred, e.g., BTC
amount	DECIMAL	YES	The amount to be transferred
type	INT	YES	1: transfer from main account to cross margin account 2: transfer from cross margin account to main account
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Margin Account Borrow (MARGIN)
Response:
{
    //transaction id
    "tranId": 100000001
}
POST /sapi/v1/margin/loan (HMAC SHA256)

Apply for a loan.

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
symbol	STRING	NO	isolated symbol
amount	DECIMAL	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If "isIsolated" = "TRUE", "symbol" must be sent
"isIsolated" = "FALSE" for crossed margin loan
Margin Account Repay (MARGIN)
Response:
{
    //transaction id
    "tranId": 100000001
}
POST /sapi/v1/margin/repay (HMAC SHA256)

Repay loan for margin account.

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
symbol	STRING	NO	isolated symbol
amount	DECIMAL	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If "isIsolated" = "TRUE", "symbol" must be sent
"isIsolated" = "FALSE" for crossed margin repay
Query Margin Asset (MARKET_DATA)
Response:
{
    "assetFullName": "Binance Coin",
    "assetName": "BNB",
    "isBorrowable": false,
    "isMortgageable": true,
    "userMinBorrow": "0.00000000",
    "userMinRepay": "0.00000000"
}
GET /sapi/v1/margin/asset

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
Query Cross Margin Pair (MARKET_DATA)
Response:
{
   "id":323355778339572400,
   "symbol":"BTCUSDT",
   "base":"BTC",
   "quote":"USDT",
   "isMarginTrade":true,
   "isBuyAllowed":true,
   "isSellAllowed":true
}
GET /sapi/v1/margin/pair

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
Get All Margin Assets (MARKET_DATA)
Response:
  [
      {
          "assetFullName": "USD coin",
          "assetName": "USDC",
          "isBorrowable": true,
          "isMortgageable": true,
          "userMinBorrow": "0.00000000",
          "userMinRepay": "0.00000000"
      },
      {
          "assetFullName": "BNB-coin",
          "assetName": "BNB",
          "isBorrowable": true,
          "isMortgageable": true,
          "userMinBorrow": "1.00000000",
          "userMinRepay": "0.00000000"
      },
      {
          "assetFullName": "Tether",
          "assetName": "USDT",
          "isBorrowable": true,
          "isMortgageable": true,
          "userMinBorrow": "1.00000000",
          "userMinRepay": "0.00000000"
      },
      {
          "assetFullName": "etherum",
          "assetName": "ETH",
          "isBorrowable": true,
          "isMortgageable": true,
          "userMinBorrow": "0.00000000",
          "userMinRepay": "0.00000000"
      },
      {
          "assetFullName": "Bitcoin",
          "assetName": "BTC",
          "isBorrowable": true,
          "isMortgageable": true,
          "userMinBorrow": "0.00000000",
          "userMinRepay": "0.00000000"
      }
  ]
GET /sapi/v1/margin/allAssets

Weight(IP): 1

Parameters:

None

Get All Cross Margin Pairs (MARKET_DATA)
Response:
[
    {
        "base": "BNB",
        "id": 351637150141315861,
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "BNBBTC"
    },
    {
        "base": "TRX",
        "id": 351637923235429141,
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "TRXBTC"
    },
    {
        "base": "XRP",
        "id": 351638112213990165,
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "XRPBTC"
    },
    {
        "base": "ETH",
        "id": 351638524530850581,
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "ETHBTC"
    },
    {
        "base": "BNB",
        "id": 376870400832855109,
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "USDT",
        "symbol": "BNBUSDT"
  }
]
GET /sapi/v1/margin/allPairs

Weight(IP): 1

Parameters:

None

Query Margin PriceIndex (MARKET_DATA)
Response:
{
   "calcTime": 1562046418000,
   "price": "0.00333930",
   "symbol": "BNBBTC"
}
GET /sapi/v1/margin/priceIndex

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
Margin Account New Order (TRADE)
Response ACK:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "isIsolated": true,       // if isolated margin
  "transactTime": 1507725176595
}
Response RESULT:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "transactTime": 1507725176595,
  "price": "1.00000000",
  "origQty": "10.00000000",
  "executedQty": "10.00000000",
  "cummulativeQuoteQty": "10.00000000",
  "status": "FILLED",
  "timeInForce": "GTC",
  "type": "MARKET",
  "isIsolated": true,       // if isolated margin
  "side": "SELL"
}
Response FULL:
{
  "symbol": "BTCUSDT",
  "orderId": 28,
  "clientOrderId": "6gCrw2kRUAF9CvJDGP16IP",
  "transactTime": 1507725176595,
  "price": "1.00000000",
  "origQty": "10.00000000",
  "executedQty": "10.00000000",
  "cummulativeQuoteQty": "10.00000000",
  "status": "FILLED",
  "timeInForce": "GTC",
  "type": "MARKET",
  "side": "SELL",
  "marginBuyBorrowAmount": 5,       // will not return if no margin trade happens
  "marginBuyBorrowAsset": "BTC",    // will not return if no margin trade happens
  "isIsolated": true,       // if isolated margin
  "fills": [
    {
      "price": "4000.00000000",
      "qty": "1.00000000",
      "commission": "4.00000000",
      "commissionAsset": "USDT"
    },
    {
      "price": "3999.00000000",
      "qty": "5.00000000",
      "commission": "19.99500000",
      "commissionAsset": "USDT"
    },
    {
      "price": "3998.00000000",
      "qty": "2.00000000",
      "commission": "7.99600000",
      "commissionAsset": "USDT"
    },
    {
      "price": "3997.00000000",
      "qty": "1.00000000",
      "commission": "3.99700000",
      "commissionAsset": "USDT"
    },
    {
      "price": "3995.00000000",
      "qty": "1.00000000",
      "commission": "3.99500000",
      "commissionAsset": "USDT"
    }
  ]
}
POST /sapi/v1/margin/order (HMAC SHA256)

Post a new order for margin account.

Weight(UID): 6

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
side	ENUM	YES	BUY
SELL
type	ENUM	YES	
quantity	DECIMAL	NO	
quoteOrderQty	DECIMAL	NO	
price	DECIMAL	NO	
stopPrice	DECIMAL	NO	Used with STOP_LOSS, STOP_LOSS_LIMIT, TAKE_PROFIT, and TAKE_PROFIT_LIMIT orders.
newClientOrderId	STRING	NO	A unique id among open orders. Automatically generated if not sent.
icebergQty	DECIMAL	NO	Used with LIMIT, STOP_LOSS_LIMIT, and TAKE_PROFIT_LIMIT to create an iceberg order.
newOrderRespType	ENUM	NO	Set the response JSON. ACK, RESULT, or FULL; MARKET and LIMIT order types default to FULL, all other orders default to ACK.
sideEffectType	ENUM	NO	NO_SIDE_EFFECT, MARGIN_BUY, AUTO_REPAY; default NO_SIDE_EFFECT.
timeInForce	ENUM	NO	GTC,IOC,FOK
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Margin Account Cancel Order (TRADE)
Response:
{
  "symbol": "LTCBTC",
  "isIsolated": true,       // if isolated margin
  "orderId": 28,
  "origClientOrderId": "myOrder1",
  "clientOrderId": "cancelMyOrder1",
  "price": "1.00000000",
  "origQty": "10.00000000",
  "executedQty": "8.00000000",
  "cummulativeQuoteQty": "8.00000000",
  "status": "CANCELED",
  "timeInForce": "GTC",
  "type": "LIMIT",
  "side": "SELL"
}
DELETE /sapi/v1/margin/order (HMAC SHA256)

Cancel an active order for margin account.

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
orderId	LONG	NO	
origClientOrderId	STRING	NO	
newClientOrderId	STRING	NO	Used to uniquely identify this cancel. Automatically generated by default.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Either orderId or origClientOrderId must be sent.
Margin Account Cancel all Open Orders on a Symbol (TRADE)
Response:
[
  {
    "symbol": "BTCUSDT",
    "isIsolated": true,       // if isolated margin
    "origClientOrderId": "E6APeyTJvkMvLMYMqu1KQ4",
    "orderId": 11,
    "orderListId": -1,
    "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
    "price": "0.089853",
    "origQty": "0.178622",
    "executedQty": "0.000000",
    "cummulativeQuoteQty": "0.000000",
    "status": "CANCELED",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY"
  },
  {
    "symbol": "BTCUSDT",
    "isIsolated": false,       // if isolated margin
    "origClientOrderId": "A3EF2HCwxgZPFMrfwbgrhv",
    "orderId": 13,
    "orderListId": -1,
    "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
    "price": "0.090430",
    "origQty": "0.178622",
    "executedQty": "0.000000",
    "cummulativeQuoteQty": "0.000000",
    "status": "CANCELED",
    "timeInForce": "GTC",
    "type": "LIMIT",
    "side": "BUY"
  },
  {
    "orderListId": 1929,
    "contingencyType": "OCO",
    "listStatusType": "ALL_DONE",
    "listOrderStatus": "ALL_DONE",
    "listClientOrderId": "2inzWQdDvZLHbbAmAozX2N",
    "transactionTime": 1585230948299,
    "symbol": "BTCUSDT",
    "isIsolated": true,       // if isolated margin
    "orders": [
      {
        "symbol": "BTCUSDT",
        "orderId": 20,
        "clientOrderId": "CwOOIPHSmYywx6jZX77TdL"
      },
      {
        "symbol": "BTCUSDT",
        "orderId": 21,
        "clientOrderId": "461cPg51vQjV3zIMOXNz39"
      }
    ],
    "orderReports": [
      {
        "symbol": "BTCUSDT",
        "origClientOrderId": "CwOOIPHSmYywx6jZX77TdL",
        "orderId": 20,
        "orderListId": 1929,
        "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
        "price": "0.668611",
        "origQty": "0.690354",
        "executedQty": "0.000000",
        "cummulativeQuoteQty": "0.000000",
        "status": "CANCELED",
        "timeInForce": "GTC",
        "type": "STOP_LOSS_LIMIT",
        "side": "BUY",
        "stopPrice": "0.378131",
        "icebergQty": "0.017083"
      },
      {
        "symbol": "BTCUSDT",
        "origClientOrderId": "461cPg51vQjV3zIMOXNz39",
        "orderId": 21,
        "orderListId": 1929,
        "clientOrderId": "pXLV6Hz6mprAcVYpVMTGgx",
        "price": "0.008791",
        "origQty": "0.690354",
        "executedQty": "0.000000",
        "cummulativeQuoteQty": "0.000000",
        "status": "CANCELED",
        "timeInForce": "GTC",
        "type": "LIMIT_MAKER",
        "side": "BUY",
        "icebergQty": "0.639962"
      }
    ]
  }
]
DELETE /sapi/v1/margin/openOrders (HMAC SHA256)

Cancels all active orders on a symbol for margin account.
This includes OCO orders.

Weight(IP): 1

Parameters

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Get Cross Margin Transfer History (USER_DATA)
Response:
{
  "rows": [
    {
      "amount": "0.10000000",
      "asset": "BNB",
      "status": "CONFIRMED",
      "timestamp": 1566898617,
      "txId": 5240372201,
      "type": "ROLL_IN"
    },
    {
      "amount": "5.00000000",
      "asset": "USDT",
      "status": "CONFIRMED",
      "timestamp": 1566888436,
      "txId": 5239810406,
      "type": "ROLL_OUT"
    },
    {
      "amount": "1.00000000",
      "asset": "EOS",
      "status": "CONFIRMED",
      "timestamp": 1566888403,
      "txId": 5239808703,
      "type": "ROLL_IN"
    }
  ],
  "total": 3
}
GET /sapi/v1/margin/transfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
type	STRING	NO	Transfer Type: ROLL_IN, ROLL_OUT
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
archived	STRING	NO	Default: false. Set to true for archived data from 6 months ago
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Response in descending order
Returns data for last 7 days by default
Set archived to true to query data from 6 months ago
Query Loan Record (USER_DATA)
Response:
{
  "rows": [
    {
        "isolatedSymbol": "BNBUSDT", // isolated symbol, will not be returned for crossed margin
        "txId": 12807067523,
        "asset": "BNB",
        "principal": "0.84624403",
        "timestamp": 1555056425000,
        "status": "CONFIRMED"   //one of PENDING (pending execution), CONFIRMED (successfully loaned), FAILED (execution failed, nothing happened to your account);
    }
  ],
  "total": 1
}
GET /sapi/v1/margin/loan (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isolatedSymbol	STRING	NO	isolated symbol
txId	LONG	NO	the tranId in POST /sapi/v1/margin/loan
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
archived	STRING	NO	Default: false. Set to true for archived data from 6 months ago
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
txId or startTime must be sent. txId takes precedence.
Response in descending order
If isolatedSymbol is not sent, crossed margin data will be returned
Set archived to true to query data from 6 months ago
Query Repay Record (USER_DATA)
Response:
{
     "rows": [
         {
                "isolatedSymbol": "BNBUSDT", // isolated symbol, will not be returned for crossed margin
                "amount": "14.00000000",   //Total amount repaid
                "asset": "BNB",   
                "interest": "0.01866667",    //Interest repaid
                "principal": "13.98133333",   //Principal repaid
                "status": "CONFIRMED",   //one of PENDING (pending execution), CONFIRMED (successfully execution), FAILED (execution failed, nothing happened to your account)
                "timestamp": 1563438204000,
                "txId": 2970933056
         }
     ],
     "total": 1
}
GET /sapi/v1/margin/repay (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isolatedSymbol	STRING	NO	isolated symbol
txId	LONG	NO	return of /sapi/v1/margin/repay
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
archived	STRING	NO	Default: false. Set to true for archived data from 6 months ago
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
txId or startTime must be sent. txId takes precedence.
Response in descending order
If isolatedSymbol is not sent, crossed margin data will be returned
Set archived to true to query data from 6 months ago
Get Interest History (USER_DATA)
Response:
{
    "rows":[
        {
            "isolatedSymbol": "BNBUSDT", // isolated symbol, will not be returned for crossed margin
            "asset": "BNB",
            "interest": "0.02414667",
            "interestAccuredTime": 1566813600000,
            "interestRate": "0.01600000",
            "principal": "36.22000000",
            "type": "ON_BORROW"
        }
    ],
    "total": 1
}
GET /sapi/v1/margin/interestHistory (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
isolatedSymbol	STRING	NO	isolated symbol
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
archived	STRING	NO	Default: false. Set to true for archived data from 6 months ago
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Response in descending order
If isolatedSymbol is not sent, crossed margin data will be returned
Set archived to true to query data from 6 months ago
type in response has 4 enums:
PERIODIC interest charged per hour
ON_BORROW first interest charged on borrow
PERIODIC_CONVERTED interest charged per hour converted into BNB
ON_BORROW_CONVERTED first interest charged on borrow converted into BNB
Get Force Liquidation Record (USER_DATA)
Response:
  {
      "rows": [
          {
              "avgPrice": "0.00388359",
              "executedQty": "31.39000000",
              "orderId": 180015097,
              "price": "0.00388110",
              "qty": "31.39000000",
              "side": "SELL",
              "symbol": "BNBBTC",
              "timeInForce": "GTC",
              "isIsolated": true,
              "updatedTime": 1558941374745
          }
      ],
      "total": 1
  }
GET /sapi/v1/margin/forceLiquidationRec (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	NO	
endTime	LONG	NO	
isolatedSymbol	STRING	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Response in descending order
Query Cross Margin Account Details (USER_DATA)
Response:
{
      "borrowEnabled": true,
      "marginLevel": "11.64405625",
      "totalAssetOfBtc": "6.82728457",
      "totalLiabilityOfBtc": "0.58633215",
      "totalNetAssetOfBtc": "6.24095242",
      "tradeEnabled": true,
      "transferEnabled": true,
      "userAssets": [
          {
              "asset": "BTC",
              "borrowed": "0.00000000",
              "free": "0.00499500",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00499500"
          },
          {
              "asset": "BNB",
              "borrowed": "201.66666672",
              "free": "2346.50000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "2144.83333328"
          },
          {
              "asset": "ETH",
              "borrowed": "0.00000000",
              "free": "0.00000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00000000"
          },
          {
              "asset": "USDT",
              "borrowed": "0.00000000",
              "free": "0.00000000",
              "interest": "0.00000000",
              "locked": "0.00000000",
              "netAsset": "0.00000000"
          }
      ]
}
GET /sapi/v1/margin/account (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Query Margin Account's Order (USER_DATA)
Response:
{
   "clientOrderId": "ZwfQzuDIGpceVhKW5DvCmO",
   "cummulativeQuoteQty": "0.00000000",
   "executedQty": "0.00000000",
   "icebergQty": "0.00000000",
   "isWorking": true,
   "orderId": 213205622,
   "origQty": "0.30000000",
   "price": "0.00493630",
   "side": "SELL",
   "status": "NEW",
   "stopPrice": "0.00000000",
   "symbol": "BNBBTC",
   "isIsolated": true,
   "time": 1562133008725,
   "timeInForce": "GTC",
   "type": "LIMIT",
   "updateTime": 1562133008725
}
GET /sapi/v1/margin/order (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
orderId	LONG	NO	
origClientOrderId	STRING	NO	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Either orderId or origClientOrderId must be sent.
For some historical orders cummulativeQuoteQty will be < 0, meaning the data is not available at this time.
Query Margin Account's Open Orders (USER_DATA)
Response:
[
   {
       "clientOrderId": "qhcZw71gAkCCTv0t0k8LUK",
       "cummulativeQuoteQty": "0.00000000",
       "executedQty": "0.00000000",
       "icebergQty": "0.00000000",
       "isWorking": true,
       "orderId": 211842552,
       "origQty": "0.30000000",
       "price": "0.00475010",
       "side": "SELL",
       "status": "NEW",
       "stopPrice": "0.00000000",
       "symbol": "BNBBTC",
       "isIsolated": true,
       "time": 1562040170089,
       "timeInForce": "GTC",
       "type": "LIMIT",
       "updateTime": 1562040170089
    }
]
GET /sapi/v1/margin/openOrders (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	NO	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If the symbol is not sent, orders for all symbols will be returned in an array.
When all symbols are returned, the number of requests counted against the rate limiter is equal to the number of symbols currently trading on the exchange.
If isIsolated ="TRUE", symbol must be sent.
Query Margin Account's All Orders (USER_DATA)
Response:
[
      {
          "clientOrderId": "D2KDy4DIeS56PvkM13f8cP",
          "cummulativeQuoteQty": "0.00000000",
          "executedQty": "0.00000000",
          "icebergQty": "0.00000000",
          "isWorking": false,
          "orderId": 41295,
          "origQty": "5.31000000",
          "price": "0.22500000",
          "side": "SELL",
          "status": "CANCELED",
          "stopPrice": "0.18000000",
          "symbol": "BNBBTC",
          "isIsolated": false,
          "time": 1565769338806,
          "timeInForce": "GTC",
          "type": "TAKE_PROFIT_LIMIT",
          "updateTime": 1565769342148
      },
      {
          "clientOrderId": "gXYtqhcEAs2Rn9SUD9nRKx",
          "cummulativeQuoteQty": "0.00000000",
          "executedQty": "0.00000000",
          "icebergQty": "1.00000000",
          "isWorking": true,
          "orderId": 41296,
          "origQty": "6.65000000",
          "price": "0.18000000",
          "side": "SELL",
          "status": "CANCELED",
          "stopPrice": "0.00000000",
          "symbol": "BNBBTC",
          "isIsolated": false,
          "time": 1565769348687,
          "timeInForce": "GTC",
          "type": "LIMIT",
          "updateTime": 1565769352226
      },
      {
          "clientOrderId": "duDq1BqohhcMmdMs9FSuDy",
          "cummulativeQuoteQty": "0.39450000",
          "executedQty": "2.63000000",
          "icebergQty": "0.00000000",
          "isWorking": true,
          "orderId": 41297,
          "origQty": "2.63000000",
          "price": "0.00000000",
          "side": "SELL",
          "status": "FILLED",
          "stopPrice": "0.00000000",
          "symbol": "BNBBTC",
          "isIsolated": false,
          "time": 1565769358139,
          "timeInForce": "GTC",
          "type": "MARKET",
          "updateTime": 1565769358139
      }

]
GET /sapi/v1/margin/allOrders (HMAC SHA256)

Weight(IP): 200

Request Limit
60times/min per IP

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
orderId	LONG	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 500; max 500.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If orderId is set, it will get orders >= that orderId. Otherwise most recent orders are returned.
For some historical orders cummulativeQuoteQty will be < 0, meaning the data is not available at this time.
Margin Account New OCO (TRADE)
Response:
{
  "orderListId": 0,
  "contingencyType": "OCO",
  "listStatusType": "EXEC_STARTED",
  "listOrderStatus": "EXECUTING",
  "listClientOrderId": "JYVpp3F0f5CAG15DhtrqLp",
  "transactionTime": 1563417480525,
  "symbol": "LTCBTC",
  "marginBuyBorrowAmount": "5",       // will not return if no margin trade happens
  "marginBuyBorrowAsset": "BTC",    // will not return if no margin trade happens
  "isIsolated": false,       // if isolated margin
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "clientOrderId": "Kk7sqHb9J6mJWTMDVW7Vos"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "clientOrderId": "xTXKaGYd4bluPVp78IVRvl"
    }
  ],
  "orderReports": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "orderListId": 0,
      "clientOrderId": "Kk7sqHb9J6mJWTMDVW7Vos",
      "transactTime": 1563417480525,
      "price": "0.000000",
      "origQty": "0.624363",
      "executedQty": "0.000000",
      "cummulativeQuoteQty": "0.000000",
      "status": "NEW",
      "timeInForce": "GTC",
      "type": "STOP_LOSS",
      "side": "BUY",
      "stopPrice": "0.960664"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "orderListId": 0,
      "clientOrderId": "xTXKaGYd4bluPVp78IVRvl",
      "transactTime": 1563417480525,
      "price": "0.036435",
      "origQty": "0.624363",
      "executedQty": "0.000000",
      "cummulativeQuoteQty": "0.000000",
      "status": "NEW",
      "timeInForce": "GTC",
      "type": "LIMIT_MAKER",
      "side": "BUY"
    }
  ]
}
POST /sapi/v1/margin/order/oco (HMAC SHA256)

Send in a new OCO for a margin account

Weight(UID): 6

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
listClientOrderId	STRING	NO	A unique Id for the entire orderList
side	ENUM	YES	
quantity	DECIMAL	YES	
limitClientOrderId	STRING	NO	A unique Id for the limit order
price	DECIMAL	YES	
limitIcebergQty	DECIMAL	NO	
stopClientOrderId	STRING	NO	A unique Id for the stop loss/stop loss limit leg
stopPrice	DECIMAL	YES	
stopLimitPrice	DECIMAL	NO	If provided, stopLimitTimeInForce is required.
stopIcebergQty	DECIMAL	NO	
stopLimitTimeInForce	ENUM	NO	Valid values are GTC/FOK/IOC
newOrderRespType	ENUM	NO	Set the response JSON.
sideEffectType	ENUM	NO	NO_SIDE_EFFECT, MARGIN_BUY, AUTO_REPAY; default NO_SIDE_EFFECT.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Other Info:

Price Restrictions:
SELL: Limit Price > Last Price > Stop Price
BUY: Limit Price < Last Price < Stop Price
Quantity Restrictions:
Both legs must have the same quantity
ICEBERG quantities however do not have to be the same.
Order Rate Limit
OCO counts as 2 orders against the order rate limit.
Margin Account Cancel OCO (TRADE)
Response:
{
  "orderListId": 0,
  "contingencyType": "OCO",
  "listStatusType": "ALL_DONE",
  "listOrderStatus": "ALL_DONE",
  "listClientOrderId": "C3wyj4WVEktd7u9aVBRXcN",
  "transactionTime": 1574040868128,
  "symbol": "LTCBTC",
  "isIsolated": false,       // if isolated margin
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 2,
      "clientOrderId": "pO9ufTiFGg3nw2fOdgeOXa"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 3,
      "clientOrderId": "TXOvglzXuaubXAaENpaRCB"
    }
  ],
  "orderReports": [
    {
      "symbol": "LTCBTC",
      "origClientOrderId": "pO9ufTiFGg3nw2fOdgeOXa",
      "orderId": 2,
      "orderListId": 0,
      "clientOrderId": "unfWT8ig8i0uj6lPuYLez6",
      "price": "1.00000000",
      "origQty": "10.00000000",
      "executedQty": "0.00000000",
      "cummulativeQuoteQty": "0.00000000",
      "status": "CANCELED",
      "timeInForce": "GTC",
      "type": "STOP_LOSS_LIMIT",
      "side": "SELL",
      "stopPrice": "1.00000000"
    },
    {
      "symbol": "LTCBTC",
      "origClientOrderId": "TXOvglzXuaubXAaENpaRCB",
      "orderId": 3,
      "orderListId": 0,
      "clientOrderId": "unfWT8ig8i0uj6lPuYLez6",
      "price": "3.00000000",
      "origQty": "10.00000000",
      "executedQty": "0.00000000",
      "cummulativeQuoteQty": "0.00000000",
      "status": "CANCELED",
      "timeInForce": "GTC",
      "type": "LIMIT_MAKER",
      "side": "SELL"
    }
  ]
}
DELETE /sapi/v1/margin/orderList (HMAC SHA256)

Cancel an entire Order List for a margin account.

Weight(UID): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
orderListId	LONG	NO	Either orderListId or listClientOrderId must be provided
listClientOrderId	STRING	NO	Either orderListId or listClientOrderId must be provided
newClientOrderId	STRING	NO	Used to uniquely identify this cancel. Automatically generated by default
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Additional notes:

Canceling an individual leg will cancel the entire OCO
Query Margin Account's OCO (USER_DATA)
Response:
{
  "orderListId": 27,
  "contingencyType": "OCO",
  "listStatusType": "EXEC_STARTED",
  "listOrderStatus": "EXECUTING",
  "listClientOrderId": "h2USkA5YQpaXHPIrkd96xE",
  "transactionTime": 1565245656253,
  "symbol": "LTCBTC",
  "isIsolated": false,       // if isolated margin
  "orders": [
    {
      "symbol": "LTCBTC",
      "orderId": 4,
      "clientOrderId": "qD1gy3kc3Gx0rihm9Y3xwS"
    },
    {
      "symbol": "LTCBTC",
      "orderId": 5,
      "clientOrderId": "ARzZ9I00CPM8i3NhmU9Ega"
    }
  ]
}
GET /sapi/v1/margin/orderList (HMAC SHA256)

Retrieves a specific OCO based on provided optional parameters

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
symbol	STRING	NO	mandatory for isolated margin, not supported for cross margin
orderListId	LONG	NO	Either orderListId or origClientOrderId must be provided
origClientOrderId	STRING	NO	Either orderListId or origClientOrderId must be provided
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Query Margin Account's all OCO (USER_DATA)
Response:
[
  {
    "orderListId": 29,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "amEEAXryFzFwYF1FeRpUoZ",
    "transactionTime": 1565245913483,
    "symbol": "LTCBTC",
    "isIsolated": true,       // if isolated margin
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 4,
        "clientOrderId": "oD7aesZqjEGlZrbtRpy5zB"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 5,
        "clientOrderId": "Jr1h6xirOxgeJOUuYQS7V3"
      }
    ]
  },
  {
    "orderListId": 28,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "hG7hFNxJV6cZy3Ze4AUT4d",
    "transactionTime": 1565245913407,
    "symbol": "LTCBTC",
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 2,
        "clientOrderId": "j6lFOfbmFMRjTYA7rRJ0LP"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 3,
        "clientOrderId": "z0KCjOdditiLS5ekAFtK81"
      }
    ]
  }
]
GET /sapi/v1/margin/allOrderList (HMAC SHA256)

Retrieves all OCO for a specific margin account based on provided optional parameters

Weight(IP): 200

Parameters

Name	Type	Mandatory	Description
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
symbol	STRING	NO	mandatory for isolated margin, not supported for cross margin
fromId	LONG	NO	If supplied, neither startTime or endTime can be provided
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default Value: 500; Max Value: 1000
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Query Margin Account's Open OCO (USER_DATA)
Response:
[
  {
    "orderListId": 31,
    "contingencyType": "OCO",
    "listStatusType": "EXEC_STARTED",
    "listOrderStatus": "EXECUTING",
    "listClientOrderId": "wuB13fmulKj3YjdqWEcsnp",
    "transactionTime": 1565246080644,
    "symbol": "LTCBTC",
    "isIsolated": false,       // if isolated margin
    "orders": [
      {
        "symbol": "LTCBTC",
        "orderId": 4,
        "clientOrderId": "r3EH2N76dHfLoSZWIUw1bT"
      },
      {
        "symbol": "LTCBTC",
        "orderId": 5,
        "clientOrderId": "Cv1SnyPD3qhqpbjpYEHbd2"
      }
    ]
  }
]
GET /sapi/v1/margin/openOrderList (HMAC SHA256)

Weight(IP): 10

Parameters

Name	Type	Mandatory	Description
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
symbol	STRING	NO	mandatory for isolated margin, not supported for cross margin
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Query Margin Account's Trade List (USER_DATA)
Response:
[
    {
        "commission": "0.00006000",
        "commissionAsset": "BTC",
        "id": 34,
        "isBestMatch": true,
        "isBuyer": false,
        "isMaker": false,
        "orderId": 39324,
        "price": "0.02000000",
        "qty": "3.00000000",
        "symbol": "BNBBTC",
        "isIsolated": false,
        "time": 1561973357171
    }
]
GET /sapi/v1/margin/myTrades (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
isIsolated	STRING	NO	for isolated margin or not, "TRUE", "FALSE"，default "FALSE"
startTime	LONG	NO	
endTime	LONG	NO	
fromId	LONG	NO	TradeId to fetch from. Default gets most recent trades.
limit	INT	NO	Default 500; max 1000.
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If fromId is set, it will get trades >= that fromId. Otherwise most recent trades are returned.
Query Max Borrow (USER_DATA)
Response:
{
  "amount": "1.69248805", // account's currently max borrowable amount with sufficient system availability
  "borrowLimit": "60" // max borrowable amount limited by the account level
}
GET /sapi/v1/margin/maxBorrowable (HMAC SHA256)

Weight(IP): 50

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isolatedSymbol	STRING	NO	isolated symbol
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If isolatedSymbol is not sent, crossed margin data will be sent.
borrowLimit is also available from https://www.binance.com/en/margin-fee
Query Max Transfer-Out Amount (USER_DATA)
Response:
 {
      "amount": "3.59498107"
 }
GET /sapi/v1/margin/maxTransferable (HMAC SHA256)

Weight(IP): 50

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
isolatedSymbol	STRING	NO	isolated symbol
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
If isolatedSymbol is not sent, crossed margin data will be sent.
Isolated Margin Account Transfer (MARGIN)
Response:
{
    //transaction id
    "tranId": 100000001
}
POST /sapi/v1/margin/isolated/transfer (HMAC SHA256)

Weight(UID): 600

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	asset,such as BTC
symbol	STRING	YES	
transFrom	STRING	YES	"SPOT", "ISOLATED_MARGIN"
transTo	STRING	YES	"SPOT", "ISOLATED_MARGIN"
amount	DECIMAL	YES	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Get Isolated Margin Transfer History (USER_DATA)
Response:
{
  "rows": [
    {
      "amount": "0.10000000",
      "asset": "BNB",
      "status": "CONFIRMED",
      "timestamp": 1566898617000,
      "txId": 5240372201,
      "transFrom": "SPOT",
      "transTo": "ISOLATED_MARGIN"
    },
    {
      "amount": "5.00000000",
      "asset": "USDT",
      "status": "CONFIRMED",
      "timestamp": 1566888436123,
      "txId": 5239810406,
      "transFrom": "ISOLATED_MARGIN",
      "transTo": "SPOT"
    }
  ],
  "total": 2
}
GET /sapi/v1/margin/isolated/transfer (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
symbol	STRING	YES	
transFrom	STRING	NO	"SPOT", "ISOLATED_MARGIN"
transTo	STRING	NO	"SPOT", "ISOLATED_MARGIN"
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Current page, default 1
size	LONG	NO	Default 10, max 100
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Isolated Margin Account Info (USER_DATA)
Response:
If "symbols" is not sent
{
   "assets":[
      {
        "baseAsset": 
        {
          "asset": "BTC",
          "borrowEnabled": true,
          "borrowed": "0.00000000",
          "free": "0.00000000",
          "interest": "0.00000000",
          "locked": "0.00000000",
          "netAsset": "0.00000000",
          "netAssetOfBtc": "0.00000000",
          "repayEnabled": true,
          "totalAsset": "0.00000000"
        },
        "quoteAsset": 
        {
          "asset": "USDT",
          "borrowEnabled": true,
          "borrowed": "0.00000000",
          "free": "0.00000000",
          "interest": "0.00000000",
          "locked": "0.00000000",
          "netAsset": "0.00000000",
          "netAssetOfBtc": "0.00000000",
          "repayEnabled": true,
          "totalAsset": "0.00000000"
        },
        "symbol": "BTCUSDT",
        "isolatedCreated": true, 
        "enabled": true, // true-enabled, false-disabled
        "marginLevel": "0.00000000", 
        "marginLevelStatus": "EXCESSIVE", // "EXCESSIVE", "NORMAL", "MARGIN_CALL", "PRE_LIQUIDATION", "FORCE_LIQUIDATION"
        "marginRatio": "0.00000000",
        "indexPrice": "10000.00000000",
        "liquidatePrice": "1000.00000000",
        "liquidateRate": "1.00000000",
        "tradeEnabled": true
      }
    ],
    "totalAssetOfBtc": "0.00000000",
    "totalLiabilityOfBtc": "0.00000000",
    "totalNetAssetOfBtc": "0.00000000" 
}
If "symbols" is sent
{
   "assets":[
      {
        "baseAsset": 
        {
          "asset": "BTC",
          "borrowEnabled": true,
          "borrowed": "0.00000000",
          "free": "0.00000000",
          "interest": "0.00000000",
          "locked": "0.00000000",
          "netAsset": "0.00000000",
          "netAssetOfBtc": "0.00000000",
          "repayEnabled": true,
          "totalAsset": "0.00000000"
        },
        "quoteAsset": 
        {
          "asset": "USDT",
          "borrowEnabled": true,
          "borrowed": "0.00000000",
          "free": "0.00000000",
          "interest": "0.00000000",
          "locked": "0.00000000",
          "netAsset": "0.00000000",
          "netAssetOfBtc": "0.00000000",
          "repayEnabled": true,
          "totalAsset": "0.00000000"
        },
        "symbol": "BTCUSDT",
        "isolatedCreated": true, 
        "enabled": true, // true-enabled, false-disabled
        "marginLevel": "0.00000000", 
        "marginLevelStatus": "EXCESSIVE", // "EXCESSIVE", "NORMAL", "MARGIN_CALL", "PRE_LIQUIDATION", "FORCE_LIQUIDATION"
        "marginRatio": "0.00000000",
        "indexPrice": "10000.00000000",
        "liquidatePrice": "1000.00000000",
        "liquidateRate": "1.00000000",
        "tradeEnabled": true
      }
    ]
}
GET /sapi/v1/margin/isolated/account (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbols	STRING	NO	Max 5 symbols can be sent; separated by ",". e.g. "BTCUSDT,BNBUSDT,ADAUSDT"
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
If "symbols" is not sent, all isolated assets will be returned.
If "symbols" is sent, only the isolated assets of the sent symbols will be returned.
Disable Isolated Margin Account (TRADE)
Response:
{
  "success": true,
  "symbol": "BTCUSDT"
}
DELETE /sapi/v1/margin/isolated/account (HMAC SHA256)

Disable isolated margin account for a specific symbol. Each trading pair can only be deactivated once every 24 hours.

Weight(UID): 300

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Enable Isolated Margin Account (TRADE)
Response:
{
  "success": true,
  "symbol": "BTCUSDT"
}
POST /sapi/v1/margin/isolated/account (HMAC SHA256)

Enable isolated margin account for a specific symbol(Only supports activation of previously disabled accounts).

Weight(UID): 300

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Enabled Isolated Margin Account Limit (USER_DATA)
Response:
{
  "enabledAccount": 5,
  "maxAccount": 20
}
GET /sapi/v1/margin/isolated/accountLimit (HMAC SHA256)

Query enabled isolated margin account limit.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Isolated Margin Symbol (USER_DATA)
Response:
{
   "symbol":"BTCUSDT",
   "base":"BTC",
   "quote":"USDT",
   "isMarginTrade":true,
   "isBuyAllowed":true,
   "isSellAllowed":true      
}
GET /sapi/v1/margin/isolated/pair (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Get All Isolated Margin Symbol(USER_DATA)
Response:
[
    {
        "base": "BNB",
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "BNBBTC"     
    },
    {
        "base": "TRX",
        "isBuyAllowed": true,
        "isMarginTrade": true,
        "isSellAllowed": true,
        "quote": "BTC",
        "symbol": "TRXBTC"    
    }
]
GET /sapi/v1/margin/isolated/allPairs (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Toggle BNB Burn On Spot Trade And Margin Interest (USER_DATA)
Response:
{
   "spotBNBBurn":true,
   "interestBNBBurn": false   
}
POST /sapi/v1/bnbBurn (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
spotBNBBurn	STRING	NO	"true" or "false"; Determines whether to use BNB to pay for trading fees on SPOT
interestBNBBurn	STRING	NO	"true" or "false"; Determines whether to use BNB to pay for margin loan's interest 
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
"spotBNBBurn" and "interestBNBBurn" should be sent at least one.
Get BNB Burn Status (USER_DATA)
Response:
{
   "spotBNBBurn":true,
   "interestBNBBurn": false   
}
GET /sapi/v1/bnbBurn (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Margin Interest Rate History (USER_DATA)
Response:
[
    {
        "asset": "BTC",
        "dailyInterestRate": "0.00025000",
        "timestamp": 1611544731000,
        "vipLevel": 1    
    },
    {
        "asset": "BTC",
        "dailyInterestRate": "0.00035000",
        "timestamp": 1610248118000,
        "vipLevel": 1    
    }
]
GET /sapi/v1/margin/interestRateHistory (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
vipLevel	INT	NO	Default: user's vip level
startTime	LONG	NO	Default: 7 days ago
endTime	LONG	NO	Default: present. Maximum range: 1 months.
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Cross Margin Fee Data (USER_DATA)
Response:
[
    {
        "vipLevel": 0,
        "coin": "BTC",
        "transferIn": true,
        "borrowable": true,
        "dailyInterest": "0.00026125",
        "yearlyInterest": "0.0953",
        "borrowLimit": "180",
        "marginablePairs": [
            "BNBBTC",
            "TRXBTC",
            "ETHBTC",
            "BTCUSDT"
        ]
    }
]
GET /sapi/v1/margin/crossMarginData (HMAC SHA256)

Get cross margin fee data collection with any vip level or user's current specific data as https://www.binance.com/en/margin-fee

Weight(IP): 1 when coin is specified; 5 when the coin parameter is omitted

Parameters:

Name	Type	Mandatory	Description
vipLevel	INT	NO	User's current specific margin data will be returned if vipLevel is omitted
coin	STRING	NO	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Isolated Margin Fee Data (USER_DATA)
Response:
[
    {
        "vipLevel": 0,
        "symbol": "BTCUSDT",
        "leverage": "10",
        "data": [
            {
                "coin": "BTC",
                "dailyInterest": "0.00026125",
                "borrowLimit": "270"
            },
            {
                "coin": "USDT",
                "dailyInterest": "0.000475",
                "borrowLimit": "2100000"
            }
        ]
    }
]
GET /sapi/v1/margin/isolatedMarginData (HMAC SHA256)

Get isolated margin fee data collection with any vip level or user's current specific data as https://www.binance.com/en/margin-fee

Weight(IP): 1 when a single is specified; 10 when the symbol parameter is omitted

Parameters:

Name	Type	Mandatory	Description
vipLevel	INT	NO	User's current specific margin data will be returned if vipLevel is omitted
symbol	STRING	NO	
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
Query Isolated Margin Tier Data (USER_DATA)
Response:
[
    {
        "symbol": "BTCUSDT",
        "tier": 1,
        "effectiveMultiple": "10",
        "initialRiskRatio": "1.111",
        "liquidationRiskRatio": "1.05",
        "baseAssetMaxBorrowable": "9",
        "quoteAssetMaxBorrowable": "70000"
    }
]
GET /sapi/v1/margin/isolatedMarginTier (HMAC SHA256)

Get isolated margin tier data collection with any tier as https://www.binance.com/en/margin-data

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
tier	STRING	NO	All margin tier data will be returned if tier is omitted
recvWindow	LONG	NO	No more than 60000
timestamp	LONG	YES	
User Data Streams

The base API endpoint is: https://api.binance.com
A User Data Stream listenKey is valid for 60 minutes after creation.
Doing a PUT on a listenKey will extend its validity for 60 minutes.
Doing a DELETE on a listenKey will close the stream and invalidate the listenKey.
Doing a POST on an account with an active listenKey will return the currently active listenKey and extend its validity for 60 minutes.
The base websocket endpoint is: wss://stream.binance.com:9443
User Data Streams are accessed at /ws/<listenKey> or /stream?streams=<listenKey>
A single connection to stream.binance.com is only valid for 24 hours; expect to be disconnected at the 24 hour mark
LISTEN KEY (SPOT)
Create a ListenKey (USER_STREAM)

Response:
{
  "listenKey": "pqia91ma19a5s61cv6a81va65sdf19v8a65a1a5s61cv6a81va65sdf19v8a65a1"
}
POST /api/v3/userDataStream

Start a new user data stream. The stream will close after 60 minutes unless a keepalive is sent. If the account has an active listenKey, that listenKey will be returned and its validity will be extended for 60 minutes.

Weight: 1

Parameters:

NONE

Data Source: Memory

Ping/Keep-alive a ListenKey (USER_STREAM)

Response:
{}
PUT /api/v3/userDataStream

Keepalive a user data stream to prevent a time out. User data streams will close after 60 minutes. It's recommended to send a ping about every 30 minutes.

Weight: 1

Parameters:

Name	Type	Mandatory	Description
listenKey	STRING	YES	
Data Source: Memory

Close a ListenKey (USER_STREAM)

Response:
{}
DELETE /api/v3/userDataStream

Close out a user data stream.

Weight: 1

Parameters:

Name	Type	Mandatory	Description
listenKey	STRING	YES	
Data Source: Memory

LISTEN KEY (MARGIN)
Create a ListenKey (USER_STREAM)

Response:
{"listenKey":  "T3ee22BIYuWqmvne0HNq2A2WsFlEtLhvWCtItw6ffhhdmjifQ2tRbuKkTHhr"}
POST /sapi/v1/userDataStream

Weight: 1

Parameters:

NONE

Ping/Keep-alive a ListenKey (USER_STREAM)

Response:
{}
PUT /sapi/v1/userDataStream

Weight: 1

Parameters:

Name	Type	Mandatory	Description
listenKey	STRING	YES	
Close a ListenKey (USER_STREAM)

Response:
{}
DELETE /sapi/v1/userDataStream

Weight: 1

Parameters:

Name	Type	Mandatory	Description
listenKey	STRING	YES	
LISTEN KEY (ISOLATED MARGIN)
Generate a Listen Key (USER_STREAM)

Response:
{
    "listenKey":  "T3ee22BIYuWqmvne0HNq2A2WsFlEtLhvWCtItw6ffhhdmjifQ2tRbuKkTHhr"
}
POST /sapi/v1/userDataStream/isolated

Weight: 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
Ping/Keep-alive a Listen Key (USER_STREAM)

Response:
{}
PUT /sapi/v1/userDataStream/isolated

Weight: 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
listenKey	STRING	YES	
Close a ListenKey (USER_STREAM)

Response:
{}
DELETE /sapi/v1/userDataStream/isolated

Weight: 1

Parameters:

Name	Type	Mandatory	Description
symbol	STRING	YES	
listenKey	STRING	YES	
Payload: Account Update
outboundAccountPosition is sent any time an account balance has changed and contains the assets that were possibly changed by the event that generated the balance change.

Payload:
{
  "e": "outboundAccountPosition", //Event type
  "E": 1564034571105,             //Event Time
  "u": 1564034571073,             //Time of last account update
  "B": [                          //Balances Array
    {
      "a": "ETH",                 //Asset
      "f": "10000.000000",        //Free
      "l": "0.000000"             //Locked
    }
  ]
}
Payload: Balance Update
Balance Update occurs during the following:

Deposits or withdrawals from the account
Transfer of funds between accounts (e.g. Spot to Margin)
Payload
{
  "e": "balanceUpdate",         //Event Type
  "E": 1573200697110,           //Event Time
  "a": "BTC",                   //Asset
  "d": "100.00000000",          //Balance Delta
  "T": 1573200697068            //Clear Time
}
Payload: Order Update
Orders are updated with the executionReport event.

Check the Public API Definitions and below for relevant enum definitions.

Average price can be found by doing Z divided by z.

Payload:
{
  "e": "executionReport",        // Event type
  "E": 1499405658658,            // Event time
  "s": "ETHBTC",                 // Symbol
  "c": "mUvoqJxFIILMdfAW5iGSOW", // Client order ID
  "S": "BUY",                    // Side
  "o": "LIMIT",                  // Order type
  "f": "GTC",                    // Time in force
  "q": "1.00000000",             // Order quantity
  "p": "0.10264410",             // Order price
  "P": "0.00000000",             // Stop price
  "F": "0.00000000",             // Iceberg quantity
  "g": -1,                       // OrderListId
  "C": "",                       // Original client order ID; This is the ID of the order being canceled
  "x": "NEW",                    // Current execution type
  "X": "NEW",                    // Current order status
  "r": "NONE",                   // Order reject reason; will be an error code.
  "i": 4293153,                  // Order ID
  "l": "0.00000000",             // Last executed quantity
  "z": "0.00000000",             // Cumulative filled quantity
  "L": "0.00000000",             // Last executed price
  "n": "0",                      // Commission amount
  "N": null,                     // Commission asset
  "T": 1499405658657,            // Transaction time
  "t": -1,                       // Trade ID
  "I": 8641984,                  // Ignore
  "w": true,                     // Is the order on the book?
  "m": false,                    // Is this trade the maker side?
  "M": false,                    // Ignore
  "O": 1499405658657,            // Order creation time
  "Z": "0.00000000",             // Cumulative quote asset transacted quantity
  "Y": "0.00000000",             // Last quote asset transacted quantity (i.e. lastPrice * lastQty)
  "Q": "0.00000000"              // Quote Order Qty
}
Execution types:

NEW - The order has been accepted into the engine.
CANCELED - The order has been canceled by the user.
REPLACED (currently unused)
REJECTED - The order has been rejected and was not processed. (This is never pushed into the User Data Stream)
TRADE - Part of the order or all of the order's quantity has filled.
EXPIRED - The order was canceled according to the order type's rules (e.g. LIMIT FOK orders with no fill, LIMIT IOC or MARKET orders that partially fill) or by the exchange, (e.g. orders canceled during liquidation, orders canceled during maintenance)
If the order is an OCO, an event will be displayed named ListStatus in addition to the executionReport event.

Payload
{
  "e": "listStatus",                //Event Type
  "E": 1564035303637,               //Event Time
  "s": "ETHBTC",                    //Symbol
  "g": 2,                           //OrderListId
  "c": "OCO",                       //Contingency Type
  "l": "EXEC_STARTED",              //List Status Type
  "L": "EXECUTING",                 //List Order Status
  "r": "NONE",                      //List Reject Reason
  "C": "F4QN4G8DlFATFlIUQ0cjdD",    //List Client Order ID
  "T": 1564035303625,               //Transaction Time
  "O": [                            //An array of objects
    {
      "s": "ETHBTC",                //Symbol
      "i": 17,                      // orderId
      "c": "AJYsMjErWJesZvqlJCTUgL" //ClientOrderId
    },
    {
      "s": "ETHBTC",
      "i": 18,
      "c": "bfYPSQdLoqAJeNrOr9adzq"
    }
  ]
}
Savings Endpoints

The endpoints below allow you to interact with Binance Savings, previously known as Binance Lending.
For more information on this, please refer to the Binance Savings page
Get Flexible Product List (USER_DATA)
Response:
[
    {
        "asset": "BTC",
        "avgAnnualInterestRate": "0.00250025",
        "canPurchase": true,
        "canRedeem": true,
        "dailyInterestPerThousand": "0.00685000",
        "featured": true,
        "minPurchaseAmount": "0.01000000",
        "productId": "BTC001",
        "purchasedAmount": "16.32467016",
        "status": "PURCHASING",
        "upLimit": "200.00000000",
        "upLimitPerUser": "5.00000000"
    },
    {
        "asset": "BUSD",
        "avgAnnualInterestRate": "0.01228590",
        "canPurchase": true,
        "canRedeem": true,
        "dailyInterestPerThousand": "0.03836000",
        "featured": true,
        "minPurchaseAmount": "0.10000000",
        "productId": "BUSD001",
        "purchasedAmount": "10.38932339",
        "status": "PURCHASING",
        "upLimit": "100000.00000000",
        "upLimitPerUser": "50000.00000000"
    }
]
GET /sapi/v1/lending/daily/product/list (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
status	ENUM	NO	"ALL", "SUBSCRIBABLE", "UNSUBSCRIBABLE"; Default: "ALL"
featured	STRING	NO	"ALL", "TRUE"; Default: "ALL"
current	LONG	NO	Current query page. Default: 1, Min: 1
size	LONG	NO	Default: 50, Max: 100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Get Left Daily Purchase Quota of Flexible Product (USER_DATA)
Response:
{
    "asset": "BUSD", 
    "leftQuota": "50000.00000000"
}
GET /sapi/v1/lending/daily/userLeftQuota (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
productId	STRING	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Purchase Flexible Product (USER_DATA)
Response:
{
    "purchaseId": 40607
}
POST /sapi/v1/lending/daily/purchase (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
productId	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Left Daily Redemption Quota of Flexible Product (USER_DATA)
Response:
{
    "asset": "USDT",
    "dailyQuota": "10000000.00000000",
    "leftQuota": "0.00000000",
    "minRedemptionAmount": "0.10000000"
}
GET /sapi/v1/lending/daily/userRedemptionQuota (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
productId	STRING	YES	
type	ENUM	YES	"FAST", "NORMAL"
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Redeem Flexible Product (USER_DATA)
Response:
{}
POST /sapi/v1/lending/daily/redeem (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
productId	STRING	YES	
amount	DECIMAL	YES	
type	ENUM	YES	"FAST", "NORMAL"
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Flexible Product Position (USER_DATA)
Response:
[
    {
        "annualInterestRate": "0.02600000",
        "asset": "USDT",
        "avgAnnualInterestRate": "0.02599895",
        "canRedeem": true,
        "dailyInterestRate": "0.00007123",
        "freeAmount": "75.46000000",
        "freezeAmount": "0.00000000", // abandoned
        "lockedAmount": "0.00000000", // abandoned
        "productId": "USDT001",
        "productName": "USDT",
        "redeemingAmount": "0.00000000",
        "todayPurchasedAmount": "0.00000000",
        "totalAmount": "75.46000000",
        "totalInterest": "0.22759183"
    }
]
GET /sapi/v1/lending/daily/token/position (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Get Fixed and Activity Project List(USER_DATA)
Response:
[
    {
        "asset": "USDT",
        "displayPriority": 1,
        "duration": 90,
        "interestPerLot": "1.35810000",
        "interestRate": "0.05510000",
        "lotSize": "100.00000000",
        "lotsLowLimit": 1,
        "lotsPurchased": 74155,
        "lotsUpLimit": 80000,
        "maxLotsPerUser": 2000,
        "needKyc": false,
        "projectId": "CUSDT90DAYSS001",
        "projectName": "USDT",
        "status": "PURCHASING",
        "type": "CUSTOMIZED_FIXED",
        "withAreaLimitation": false
    }
]
GET /sapi/v1/lending/project/list (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	NO	
type	ENUM	YES	"ACTIVITY", "CUSTOMIZED_FIXED"
status	ENUM	NO	"ALL", "SUBSCRIBABLE", "UNSUBSCRIBABLE"; default "ALL"
isSortAsc	BOOLEAN	NO	default "true"
sortBy	ENUM	NO	"START_TIME", "LOT_SIZE", "INTEREST_RATE", "DURATION"; default "START_TIME"
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10, Max:100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Purchase Fixed/Activity Project (USER_DATA)
Response:
{
    "purchaseId": "18356"
}
POST /sapi/v1/lending/customizedFixed/purchase (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
projectId	STRING	YES	
lot	LONG	YES	
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Fixed/Activity Project Position (USER_DATA)
Response:
[
    {
        "asset": "USDT",
        "canTransfer": true,
        "createTimestamp": 1587010770000,
        "duration": 14,
        "endTime": 1588291200000,
        "interest": "0.19950000",
        "interestRate": "0.05201250",
        "lot": 1,
        "positionId": 51724,
        "principal": "100.00000000",
        "projectId": "CUSDT14DAYSS001",
        "projectName": "USDT",
        "purchaseTime": 1587010771000,
        "redeemDate": "2020-05-01",
        "startTime": 1587081600000,
        "status": "HOLDING",
        "type": "CUSTOMIZED_FIXED"
    }
]
GET /sapi/v1/lending/project/position/list (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
projectId	STRING	NO	
status	ENUM	NO	"HOLDING", "REDEEMED"
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Lending Account (USER_DATA)
Response:
{
    "positionAmountVos": [
        {
            "amount": "75.46000000",
            "amountInBTC": "0.01044819",
            "amountInUSDT": "75.46000000",
            "asset": "USDT"
        },
        {
            "amount": "1.67072036",
            "amountInBTC": "0.00023163",
            "amountInUSDT": "1.67289230",
            "asset": "BUSD"
        }
    ],
    "totalAmountInBTC": "0.01067982",
    "totalAmountInUSDT": "77.13289230",
    "totalFixedAmountInBTC": "0.00000000",
    "totalFixedAmountInUSDT": "0.00000000",
    "totalFlexibleInBTC": "0.01067982",
    "totalFlexibleInUSDT": "77.13289230"
 }
GET /sapi/v1/lending/union/account (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
Get Purchase Record (USER_DATA)
Response:
Flexible Products
[
    {
        "amount": "100.00000000",
        "asset": "USDT",
        "createTime": 1575018510000,
        "lendingType": "DAILY",
        "productName": "USDT",
        "purchaseId": 26055,
        "status": "SUCCESS"
    }
]
Fixed/Activity Products
[
    {
        "amount": "100.00000000",
        "asset": "USDT",
        "createTime": 1575018453000,
        "lendingType": "ACTIVITY",
        "lot": 1,
        "productName": "【Special】USDT 7D (8%)",
        "purchaseId": 36857,
        "status": "SUCCESS"
    }
]
GET /sapi/v1/lending/union/purchaseRecord (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
lendingType	ENUM	YES	"DAILY" for flexible, "ACTIVITY" for activity, "CUSTOMIZED_FIXED" for fixed
asset	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10, Max:100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
The time between startTime and endTime cannot be longer than 30 days.
If startTime and endTime are both not sent, then the last 30 days' data will be returned.
Get Redemption Record (USER_DATA)
Response:
Flexible Products
[
    {
        "amount": "10.54000000",
        "asset": "USDT",
        "createTime": 1577257222000,
        "principal": "10.54000000",
        "projectId": "USDT001",
        "projectName": "USDT",
        "status": "PAID",
        "type": "FAST"
     }
]
Fixed/Activity Products
[
    {
        "amount": "0.07070000",
        "asset": "USDT",
        "createTime": 1566200161000,
        "interest": "0.00070000",
        "principal": "0.07000000",
        "projectId": "test06",
        "projectName": "USDT 1 day (10% anniualized)",
        "startTime": 1566198000000,
        "status": "PAID"
     }
]
GET /sapi/v1/lending/union/redemptionRecord (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
lendingType	ENUM	YES	"DAILY" for flexible, "ACTIVITY" for activity, "CUSTOMIZED_FIXED" for fixed
asset	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10, Max:100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
The time between startTime and endTime cannot be longer than 30 days.
If startTime and endTime are both not sent, then the last 30 days' data will be returned.
Get Interest History (USER_DATA)
Response:
[
    {
        "asset": "BUSD",
        "interest": "0.00006408",
        "lendingType": "DAILY",
        "productName": "BUSD",
        "time": 1577233578000
    },
    {
        "asset": "USDT",
        "interest": "0.00687654",
        "lendingType": "DAILY",
        "productName": "USDT",
        "time": 1577233562000
    }
]
GET /sapi/v1/lending/union/interestHistory (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
lendingType	ENUM	YES	"DAILY" for flexible, "ACTIVITY" for activity, "CUSTOMIZED_FIXED" for fixed
asset	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10, Max:100
recvWindow	LONG	NO	The value cannot be greater than 60000
timestamp	LONG	YES	
The time between startTime and endTime cannot be longer than 30 days.
If startTime and endTime are both not sent, then the last 30 days' data will be returned.
Change Fixed/Activity Position to Daily Position(USER_DATA)
Response:

{
  "dailyPurchaseId": 862290,
  "success": true,      
  "time": 1577233578000
}

POST /sapi/v1/lending/positionChanged (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
projectId	STRING	YES	
lot	LONG	YES	
positionId	LONG	NO	for fixed position
recvWindow	LONG	NO	no more than 60000
timestamp	LONG	YES	
PositionId is mandatory parameter for fixed position.
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Mining Endpoints

The endpoints below allow to interact with Binance Pool.
For more information on this, please refer to the Binance Pool page
Acquiring Algorithm (MARKET_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": [
    {
      "algoName": "sha256",                        //  Algorithm name
      "algoId": 1,                                 // Algorithm ID
      "poolIndex": 0,                               // Sequence 
      "unit": "h/s"                                //   Unit
    }
  ]
}
GET /sapi/v1/mining/pub/algoList (HMAC SHA256)

Weight(IP): 1

Parameter:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Acquiring CoinName (MARKET_DATA)
GET /sapi/v1/mining/pub/coinList (HMAC SHA256)

Weight(IP): 1

Parameter:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Response:
{
  "code": 0,
  "msg": "",
  "data": [
    {
      "coinName": "BTC",                      //  Currencyname
      "coinId": 1,                            // id
      "poolIndex": 0,                         // Sort
      "algoId": 1,                            // Algorithm
      "algoName": "sha256"                    //Name of algorithm
    }
  ]
}
Request for Detail Miner List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": [
    {
      "workerName": "bhdc1.16A10404B",     //Mining Account name
      "type": "H_hashrate",               // Type of hourly hashrate
      "hashrateDatas": [
        {
          "time": 1587902400000,         //  Time
          "hashrate": "0",               // Hashrate
          "reject": 0                    //Rejection Rate
        },
        {
          "time": 1587906000000,
          "hashrate": "0",
          "reject": 0
        }
      ]
    },
    {
      "workerName": "bhdc1.16A10404B",    //Mining Account name
      "type": "D_hashrate",                //Type of daily hashrate
      "hashrateDatas": [
        {
          "time": 1587902400000,          //  Time
          "hashrate": "0",                // Hashrate 
          "reject": 0                     //Rejection Rate
        },
        {
          "time": 1587906000000,
          "hashrate": "0",
          "reject": 0
        }
      ]
    }
  ]
}
GET /sapi/v1/mining/worker/detail (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	For Example
algo	STRING	YES	Algorithm(sha256)	sha256
userName	STRING	YES	Mining account	test
workerName	STRING	YES	Miner’s name(required)	bhdc1.16A10404B
recvWindow	LONG	NO		
timestamp	LONG	YES		
Request for Miner List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "workerDatas": [
      {
        "workerId": "1420554439452400131",  //Miner ID
        "workerName": "2X73",               //Miner's name  
        "status": 3,                        // Status：1 valid, 2 invalid, 3 no longer valid
        "hashRate": 0,                      // Real-time rate
        "dayHashRate": 0,                   //24H Hashrate
        "rejectRate": 0,                    //Real-time Rejection Rate
        "lastShareTime": 1587712919000      // Last submission time 
      },
      {
        "workerId": "7893926126382807951",
        "workerName": "AZDC1.1A10101",
        "status": 2,
        "hashRate": 29711247541680,
        "dayHashRate": 12697781298013.66,
        "rejectRate": 0,
        "lastShareTime": 1587969727000
      }
    ],
    "totalNum": 18530,           // Total amount
    "pageSize": 20               // Rows per page
  }
}
GET /sapi/v1/mining/worker/list (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	For Example
algo	STRING	YES	Algorithm(sha256)	sha256
userName	STRING	YES	Mining account	test
pageIndex	INTEGER	NO	Page number，default is first page，start form 1	
sort	INTEGER	NO	sort sequence(default=0)0 positive sequence，1 negative sequence	
sortColumn	INTEGER	NO	Sort by( default 1): 
1: miner name, 
2: real-time computing power, 
3: daily average computing power, 
4: real-time rejection rate, 
5: last submission time	
workerStatus	INTEGER	NO	miners status(default=0)0 all，1 valid，2 invalid，3failure	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Earnings List(USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "accountProfits": [
      {
        "time": 1586188800000,            // Mining date
        "type": 31, // 0:Mining Wallet,5:Mining Address,7:Pool Savings,8:Transferred,31:Income Transfer ,32:Hashrate Resale-Mining Wallet 33:Hashrate Resale-Pool Savings
        "hashTransfer": null,            // Transferred Hashrate
        "transferAmount": null,          // Transferred Income   
        "dayHashRate": 129129903378244,  // Daily Hashrate
        "profitAmount": 8.6083060304,   //Earnings Amount
        "coinName":"BTC",              // Coin Type
        "status": 2    //Status：0:Unpaid， 1:Paying  2：Paid
      },
      {
        "time": 1607529600000,
        "coinName": "BTC",
        "type": 0,
        "dayHashRate": 9942053925926,
        "profitAmount": 0.85426469,
        "hashTransfer": 200000000000,
        "transferAmount": 0.02180958,
        "status": 2
      },
      {
        "time": 1607443200000,
        "coinName": "BTC",
        "type": 31,
        "dayHashRate": 200000000000,
        "profitAmount": 0.02905916,
        "hashTransfer": null,
        "transferAmount": null,
        "status": 2
      }
    ],
    "totalNum": 3,          // Total Rows
    "pageSize": 20          // Rows per page
  }
}
GET /sapi/v1/mining/payment/list (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
algo	STRING	YES	Transfer algorithm(sha256)	sha256
userName	STRING	YES	Mining account	test
coin	STRING	NO	Coin name	
startDate	Long	NO	Search date, millisecond timestamp, while empty query all	
endDate	Long	NO	Search date, millisecond timestamp, while empty query all	
pageIndex	INTEGER	NO	Page number, empty default first page, starting from 1	
pageSize	INTEGER	NO	Number of pages, minimum 10, maximum 200	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Extra Bonus List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "otherProfits": [
      {
        "time": 1607443200000,      // Mining date
        "coinName": "BTC",    // Coin Name
        "type": 4,            // 1: Merged Mining， 2: Activity Bonus, 3:Rebate 4:Smart Pool 6:Income Transfer 7:Pool Savings
        "profitAmount": 0.0011859,  //Amount
        "status": 2         //Status：0:Unpaid， 1:Paying  2：Paid
      }
    ],
    "totalNum": 3,          // Total Rows
    "pageSize": 20          // Rows per page
  }
}
GET /sapi/v1/mining/payment/other (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
algo	STRING	YES	Transfer algorithm(sha256)	sha256
userName	STRING	YES	Mining Account	test
coin	STRING	NO	Coin Name	
startDate	Long	NO	Search date, millisecond timestamp, while empty query all	
endDate	Long	NO	Search date, millisecond timestamp, while empty query all	
pageIndex	INTEGER	NO	Page number, empty default first page, starting from 1	
pageSize	INTEGER	NO	Number of pages, minimum 10, maximum 200	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Hashrate Resale List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "configDetails": [
      {
        "configId": 168,     // Mining ID
        "poolUsername": "123",  //Transfer out of subaccount
        "toPoolUsername": "user1", //  Transfer into subaccount
        "algoName": "Ethash",     // Transfer algorithm
        "hashRate": 5000000,     //  Transferred Hashrate quantity
        "startDay": 20201210,   // Start date
        "endDay": 20210405,   //End date
        "status": 1       //Status：0 Processing，1：Cancelled，2：Terminated 
      },
      {
        "configId": 166,
        "poolUsername": "pop",
        "toPoolUsername": "111111",
        "algoName": "Ethash",
        "hashRate": 3320000,
        "startDay": 20201226,
        "endDay": 20201227,
        "status": 0
      }
    ],
    "totalNum": 21,
    "pageSize": 200
  }
}
GET /sapi/v1/mining/hash-transfer/config/details/list (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
pageIndex	INTEGER	NO	Page number, empty default first page, starting from 1	
pageSize	INTEGER	NO	Number of pages, minimum 10, maximum 200	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Hashrate Resale Detail (USER_DATA)
Response:
{
    "code": 0,
    "msg": "",
    "data": {
        "profitTransferDetails": [{
                "poolUsername": "test4001",  // Transfer out of sub-account

                "toPoolUsername": "pop",    // Transfer into subaccount
                "algoName": "sha256",      // Transfer algorithm
                "hashRate": 200000000000,  // Transferred Hashrate quantity
                "day": 20201213,          // Transfer date
                "amount": 0.2256872,     // Transferred income
                "coinName": "BTC"        // Coin Name
            },
            {
                "poolUsername": "test4001",
                "toPoolUsername": "pop",
                "algoName": "sha256",
                "hashRate": 200000000000,
                "day": 20201213,
                "amount": 0.2256872,
                "coinName": "BTC"
            }
        ],
        "totalNum": 8,
        "pageSize": 200
    }
}
GET /sapi/v1/mining/hash-transfer/profit/details (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
configId	INTEGER	YES	Mining ID	168
userName	STRING	YES	Mining Account	test
pageIndex	INTEGER	NO	Page number, empty default first page, starting from 1	
pageSize	INTEGER	NO	Number of pages, minimum 10, maximum 200	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Hashrate Resale Request (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": 171  // Mining Account
}
POST /sapi/v1/mining/hash-transfer/config (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
userName	STRING	YES	Mining Account	test
algo	STRING	YES	Transfer algorithm(sha256)	sha256
endDate	Long	YES	Resale End Time (Millisecond timestamp)	1617659086000
startDate	Long	YES	Resale Start Time(Millisecond timestamp)	1607659086000
toPoolUser	STRING	YES	Mining Account	S19pro
hashRate	Long	YES	Resale hashrate h/s must be transferred (BTC is greater than 500000000000 ETH is greater than 500000)	100000000
recvWindow	LONG	NO		
timestamp	LONG	YES		
Cancel hashrate resale configuration(USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": true
}
POST /sapi/v1/mining/hash-transfer/config/cancel (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	Example
configId	INTEGER	YES	Mining ID	168
userName	STRING	YES	Mining Account	test
recvWindow	LONG	NO		
timestamp	LONG	YES		
Statistic List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "fifteenMinHashRate": "457835490067496409.00000000",          // 15 mins hashrate
    "dayHashRate": "214289268068874127.65000000",                 //  24H Hashrate
    "validNum": 0,                                                // Effective quantity
    "invalidNum": 17562,                                          // Invalid quantity
    "profitToday":{                                              // Today's estimate
      "BTC":"0.00314332",       
      "BSV":"56.17055953",
      "BCH":"106.61586001"
     },
    "profitYesterday":{                                       //  Yesterday's earnings
      "BTC":"0.00314332",
       "BSV":"56.17055953",
       "BCH":"106.61586001"
     },

    "userName": "test",                                    // Mining account
    "unit": "h/s",                                        //  Hashrate unit
    "algo": "sha256"                                      // Algorithm
  }
}
GET /sapi/v1/mining/statistics/user/status (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	For Example
algo	STRING	YES	Algorithm(sha256)	sha256
userName	STRING	YES	Mining account	test
recvWindow	LONG	NO		
timestamp	LONG	YES		
Account List (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": [
    {
      "type": "H_hashrate",        //Type of hourly hashrate
      "userName": "test",         // Mining account
      "list": [
        {
          "time": 1585267200000,    // Time
          "hashrate": "0.00000000", // Hashrate
          "reject": "0.00000000"    //Rejection Rate
        },
        {
          "time": 1585353600000,
          "hashrate": "0.00000000",
          "reject": "0.00000000"
        }
      ]
    },
    {
      "type": "D_hashrate",        //Type of daily hashrate
      "userName": "test",          // Mining account
      "list": [
        {
          "time": 1587906000000,     // Time
          "hashrate": "0.00000000", // Hashrate
          "reject": "0.00000000"    //Rejection Rate
        },
        {
          "time": 1587909600000,
          "hashrate": "0.00000000",
          "reject": "0.00000000"
        }
      ]
    }
  ]
}
GET /sapi/v1/mining/statistics/user/list (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	For Example
algo	STRING	YES	Algorithm(sha256)	sha256
userName	STRING	YES	Mining account	test
recvWindow	LONG	NO		
timestamp	LONG	YES		
Mining Account Earning (USER_DATA)
Response:
{
  "code": 0,
  "msg": "",
  "data": {
    "accountProfits": [
      {
        "time": 1607443200000,      
        "coinName": "BTC",   // Coin
        "type": 2,           // 0:Referral 1：Refund 2：Rebate
        "puid": 59985472,    //Sub-account id
        "subName": "vdvaghani", //Mining account
        "amount": 0.09186957    //Amount
      }
    ],
    "totalNum": 3,          // Total records
    "pageSize": 20          // Size of one page
  }
}
GET /sapi/v1/mining/payment/uid (HMAC SHA256)

Weight(IP): 5

Parameter:

Name	Type	Mandatory	Description	For Example
algo	STRING	YES	Algorithm(sha256)	sha256
startDate	Long	NO	Millisecond timestamp	
endDate	Long	NO	Millisecond timestamp	
pageIndex	INTEGER	NO	Default 1	
pageSize	INTEGER	NO	Min 10,Max 200	
recvWindow	LONG	NO		
timestamp	LONG	YES		
Futures

New Future Account Transfer (USER_DATA)
Response:
{
    "tranId": 100000001    //transaction id
}
POST /sapi/v1/futures/transfer (HMAC SHA256)

Execute transfer between spot account and futures account.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	The asset being transferred, e.g., USDT
amount	DECIMAL	YES	The amount to be transferred
type	INT	YES	1: transfer from spot account to USDT-Ⓜ futures account.
2: transfer from USDT-Ⓜ futures account to spot account. 
3: transfer from spot account to COIN-Ⓜ futures account. 
4: transfer from COIN-Ⓜ futures account to spot account.
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Future Account Transaction History List (USER_DATA)
Response:
{
  "rows": [
    {
      "asset": "USDT",
      "tranId": 100000001,
      "amount": "40.84624400",
      "type": "1",  // one of 1( from spot to USDT-Ⓜ), 2( from USDT-Ⓜ to spot), 3( from spot to COIN-Ⓜ), and 4( from COIN-Ⓜ to spot)
      "timestamp": 1555056425000,
      "status": "CONFIRMED" //one of PENDING (pending to execution), CONFIRMED (successfully transfered), FAILED (execution failed, nothing happened to your account);
    }
  ],
  "total": 1
}
GET /sapi/v1/futures/transfer (HMAC SHA256)

Weight(IP): 10

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
startTime	LONG	YES	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
size	LONG	NO	Default:10 Max:100
recvWindow	LONG	NO	
timestamp	LONG	YES	
Support query within the last 6 months only
If startTimeand endTime not sent, return records of the last 7 days by default
Borrow For Cross-Collateral (TRADE)
Response:
{
    "coin": "USDT",
    "amount": "4.50000000",
    "collateralCoin": "BUSD",
    "collateralAmount": "5.00000000",
    "time": 1582540328433,
    "borrowId": "438648398970089472"
}
POST /sapi/v1/futures/loan/borrow (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
amount	DECIMAL	YES when collateralAmount is empty	
collateralCoin	STRING	YES	
collateralAmount	DECIMAL	YES when amount is empty	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(UID): 3000

Rate Limit:
1/1s per account

Cross-Collateral Borrow History (USER_DATA)
Response:
{
    "rows":[
        {
            "confirmedTime": 1582540328433,
            "coin": "USDT",
            "collateralRate": "0.89991001",  // collateralLevel
            "leftTotal": "4.5",
            "leftPrincipal": "4.5",
            "deadline": 4736102399000,
            "collateralCoin": "BUSD",
            "collateralAmount": "5.0",
            "orderStatus": "PENDING",
            "borrowId": "438648398970089472"
        }
    ],
    "total": 1
}
GET /sapi/v1/futures/loan/borrow/history (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	default 500, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 10

Repay For Cross-Collateral (TRADE)
Response:
{
    "coin": "USDT",
    "amount": "1.68",
    "collateralCoin": "BUSD",
    "repayId": "439659223998894080"
}
POST /sapi/v1/futures/loan/repay (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
collateralCoin	STRING	YES	
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(UID): 3000

Rate Limit:

1/1s per account

Cross-Collateral Repayment History (USER_DATA)
Response:
{
    "rows":[
        {
            "coin": "USDT",
            "amount": "1.68",
            "collateralCoin": "BUSD",
            "repayType": "NORMAL", // "COLLATERAL" for collateral repayment
            "releasedCollateral": "1.80288889",
            "price": "1.001", // Loan/collateral exchange rate
            "repayCollateral": "10010", // Only for collateral repayment
            "confirmedTime": 1582781327575,
            "updateTime": 1582794387516, // time
            "status": "PENDING",
            "repayId": "439659223998894080"
        }
    ],
    "total": 1
}
GET /sapi/v1/futures/loan/repay/history HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	default 500, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 10

Cross-Collateral Wallet (USER_DATA)
Response:
{
    "totalCrossCollateral":"5.8238577133",
    "totalBorrowed":"5.07000000",
    "totalInterest":"0.0", // New for interest collection
    "interestFreeLimit": "100000", // New for interest free limit
    "asset": "USDT",
    "crossCollaterals":[
        {
            "collateralCoin":"BUSD",
            "locked":"5.82211108",
            "loanAmount": "5.07",
            "currentCollateralRate": "0.87168984",   // collateralLevel
            "interestFreeLimitUsed": "5.07", // New for interest free limit
            "principalForInterest": "0.0", // New for interest collection
            "interest": "0.0"  // New for interest collection
        },
        {
            "collateralCoin":"BTC",
            "locked":"0",
            "loanAmount": "0",
            "currentCollateralRate": "0",   // collateralLevel
            "interestFreeLimitUsed": "0", // New for interest free limit
            "principalForInterest": "0.0", // New for interest collection
            "interest": "0.0"  // New for interest collection
        }
    ]
}
GET /sapi/v1/futures/loan/wallet (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 10

Cross-Collateral Wallet V2 (USER_DATA)
Response:
{
    "totalCrossCollateral":"5.8238577133",
    "totalBorrowed":"5.07000000",
    "totalInterest":"0.0", // New for interest collection
    "interestFreeLimit": "100000", // New for interest free limit
    "asset": "USD", // New for USD value
    "crossCollaterals":[
        {
            "loanCoin":"USDT",
            "collateralCoin":"BUSD",
            "locked":"5.82211108",
            "loanAmount": "5.07",
            "currentCollateralRate": "0.87168984",   // collateralLevel
            "interestFreeLimitUsed": "5.07", // New for interest free limit
            "principalForInterest": "0.0", // New for interest collection
            "interest": "0.0"  // New for interest collection
        },
        {
            "loanCoin":"BUSD",
            "collateralCoin":"BTC",
            "locked":"0",
            "loanAmount": "0",
            "currentCollateralRate": "0",   // collateralLevel
            "interestFreeLimitUsed": "0", // New for interest free limit
            "principalForInterest": "0.0", // New for interest collection
            "interest": "0.0"  // New for interest collection
        }
    ]
}
GET /sapi/v2/futures/loan/wallet (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Cross-Collateral Information (USER_DATA)
Response:
[
    {
        "collateralCoin": "BUSD",
        "rate": "0.9",
        "marginCallCollateralRate": "0.95",
        "liquidationCollateralRate": "0.98",
        "currentCollateralRate": "0.87168984",
        "interestRate": "0.0", // New for interest collection
        "interestGracePeriod": "0" //Days, new for interest collection
    }
]
GET /sapi/v1/futures/loan/configs (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
collateralCoin	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
all collateral data will be returned if collateralCoin is not sent
Weight(IP): 10

Cross-Collateral Information V2 (USER_DATA)
Response:
[
    {
        "loanCoin": "BUSD",
        "collateralCoin": "BTC",
        "rate": "0.9",
        "marginCallCollateralRate": "0.95",
        "liquidationCollateralRate": "0.98",
        "currentCollateralRate": "0.87168984",
        "interestRate": "0.0", // New for interest collection
        "interestGracePeriod": "0" //Days, new for interest collection
    }
]
GET /sapi/v2/futures/loan/configs (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	NO	
collateralCoin	STRING	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
all loan and collateral data will be returned if loanCoin or collateralCoin is not sent
Weight(IP): 1

Calculate Rate After Adjust Cross-Collateral LTV (USER_DATA)
Response:
{
    "afterCollateralRate":"0.89736451"
}
GET /sapi/v1/futures/loan/calcAdjustLevel (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
collateralCoin	STRING	YES	
amount	DECIMAL	YES	
direction	ENUM	YES	"ADDITIONAL", "REDUCED"
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 50

Calculate Rate After Adjust Cross-Collateral LTV V2 (USER_DATA)
Response:
{
    "afterCollateralRate":"0.89736451"
}
GET /sapi/v2/futures/loan/calcAdjustLevel (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	YES	
collateralCoin	STRING	YES	
amount	DECIMAL	YES	
direction	ENUM	YES	"ADDITIONAL", "REDUCED"
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Get Max Amount for Adjust Cross-Collateral LTV (USER_DATA)
Response:
{
    "maxInAmount": "9.97109038",
    "maxOutAmount": "0.50952693"
}
GET /sapi/v1/futures/loan/calcMaxAdjustAmount (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
collateralCoin	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 50

Get Max Amount for Adjust Cross-Collateral LTV V2 (USER_DATA)
Response:
{
    "maxInAmount": "9.97109038",
    "maxOutAmount": "0.50952693"
}
GET /sapi/v2/futures/loan/calcMaxAdjustAmount (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	YES	
collateralCoin	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Adjust Cross-Collateral LTV (TRADE)
Response:
{
    "collateralCoin": "BUSD",
    "direction": "ADDITIONAL",
    "amount": "5.00000000",
    "time": 1583540328433
}
POST /sapi/v1/futures/loan/adjustCollateral (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
collateralCoin	STRING	YES	
amount	DECIMAL	YES	
direction	ENUM	YES	"ADDITIONAL", "REDUCED"
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(UID): 3000

RateLimit: 1/1s per account

Adjust Cross-Collateral LTV V2 (TRADE)
Response:
{
    "loanCoin" : "BUSD",
    "collateralCoin": "BTC",
    "direction": "ADDITIONAL",
    "amount": "5.00000000",
    "time": 1583540328433
}
POST /sapi/v2/futures/loan/adjustCollateral (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	YES	
collateralCoin	STRING	YES	
amount	DECIMAL	YES	
direction	ENUM	YES	"ADDITIONAL", "REDUCED"
recvWindow	LONG	NO	
timestamp	LONG	YES	
RateLimit: 1/1s per account

Adjust Cross-Collateral LTV History (USER_DATA)
Response:
{ 
    "rows":[
        {
            "amount": ".17398184",
            "collateralCoin": "BUSD", 
            "coin": "USDT", 
            "preCollateralRate":"0.87054861",
            "afterCollateralRate":"0.89736451",
            "direction": "REDUCED",
            "status": "COMPLETED",
            "adjustTime": 1583978243588
        }
    ],
    "total": 1
}
GET /sapi/v1/futures/loan/adjustCollateral/history (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	NO	
collateralCoin	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	default 500, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
All data will be returned if loanCoin or collateralCoin is not sent
Weight(IP): 10

Cross-Collateral Liquidation History (USER_DATA)
Response:
{
    "rows":[
        {
            "collateralAmountForLiquidation":"10.12345678",
            "collateralCoin": "BUSD",
            "forceLiquidationStartTime": 1583978243588,
            "coin": "USDT", 
            "restCollateralAmountAfterLiquidation": "15.12345678",
            "restLoanAmount": "11.12345678",
            "status": "PENDING"
        }
    ],
    "total": 1
}
GET /sapi/v1/futures/loan/liquidationHistory (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
loanCoin	STRING	NO	
collateralCoin	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	default 500, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
All data will be returned if loanCoin or collateralCoin is not sent
Weight(IP): 10

Check Collateral Repay Limit (USER_DATA)
Check the maximum and minimum limit when repay with collateral.

Response:
{
    "coin": "USDT",
    "collateralCoin": "BTC",
    "max": "15000",
    "min": "15"
}
GET /sapi/v1/futures/loan/collateralRepayLimit (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
collateralCoin	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Get Collateral Repay Quote (USER_DATA)
Get quote before repay with collateral is mandatory, the quote will be valid within 25 seconds.

Response:
{
    "coin": "USDT",
    "collateralCoin": "BTC",
    "amount": "0.00222",
    "quoteId": "8a03da95f0ad4fdc8067e3b6cde72423"
}
GET /sapi/v1/futures/loan/collateralRepay (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
coin	STRING	YES	
collateralCoin	STRING	YES	
amount	DECIMAL	YES	repay amount
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Repay with Collateral (USER_DATA)
Repay with collateral. Get quote before repay with collateral is mandatory, the quote will be valid within 25 seconds.

Response:
{
    "coin": "USDT",
    "collateralCoin": "BTC",
    "amount": "30",
    "quoteId": "3eece81ca2734042b2f538ea0d9cbdd3"
}
POST /sapi/v1/futures/loan/collateralRepay (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
quoteId	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Collateral Repayment Result (USER_DATA)
Check collateral repayment result.

Response:
{
    "quoteId": "3eece81ca2734042b2f538ea0d9cbdd3",
    "status": "SUCCESS"
}
GET /sapi/v1/futures/loan/collateralRepayResult (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
quoteId	STRING	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

Cross-Collateral Interest History (USER_DATA)
Response:
{
    "rows":[
        {
            "collateralCoin": "BUSD",
            "interestCoin": "USDT",
            "interest": "2.354",
            "interestFreeLimitUsed": "0", // New for interest free limit
            "principalForInterest": "10000",
            "interestRate": "0.002",
            "time": 1582794387516
        }
    ],
    "total": 1
}
GET /sapi/v1/futures/loan/interestHistory (HMAC SHA256)

Parameters:

Name	Type	Mandatory	Description
collateralCoin	STRING	NO	
startTime	LONG	NO	
endTime	LONG	NO	
current	LONG	NO	Currently querying page. Start from 1. Default:1
limit	LONG	NO	Default:500 Max:1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Weight(IP): 1

BLVT Endpoints

Get BLVT Info (MARKET_DATA)
Response:
[  
  {
    "tokenName": "BTCDOWN",  
    "description": "3X Short Bitcoin Token",
    "underlying": "BTC",
    "tokenIssued": "717953.95",
    "basket": "-821.474 BTCUSDT Futures",
    "currentBaskets":[
       {
         "symbol":"BTCUSDT",
         "amount":"-1183.984",
         "notionalValue":"-22871089.96704"
       }
     ], 
    "nav": "4.79",
    "realLeverage": "-2.316",
    "fundingRate": "0.001020",
    "dailyManagementFee": "0.0001",
    "purchaseFeePct": "0.0010",  
    "dailyPurchaseLimit": "100000.00", 
    "redeemFeePct": "0.0010",  
    "dailyRedeemLimit": "1000000.00",  
    "timestamp":1583127900000  
  },
  {
    "tokenName": "LINKUP",  
    "description": "3X LONG ChainLink Token",
    "underlying": "LINK",
    "tokenIssued": "163846.99",
    "basket": "417288.870 LINKUSDT Futures",
    "currentBaskets":[
       {
         "symbol":"LINKUSDT",
         "amount":"1640883.83",
         "notionalValue":"22596611.22293"
       }
     ], 
    "nav": "9.60",
    "realLeverage": "2.597",
    "fundingRate": "-0.000917",
    "dailyManagementFee": "0.0001",
    "purchaseFeePct": "0.0010",
    "dailyPurchaseLimit": "100000.00",
    "redeemFeePct": "0.0010",
    "dailyRedeemLimit": "1000000.00",
    "timestamp":1583127900000  
  }
 ]
GET /sapi/v1/blvt/tokenInfo

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	NO	BTCDOWN, BTCUP
Historical BLVT NAV Kline/Candlestick
The BLVT NAV system is based on Binance Futures, so the endpoint is based on fapi

Please go to here to check the endpoint and operate in accordance with the fapi usage specifications.

Subscribe BLVT (USER_DATA)
Response:
 {
    "id": 123,  
    "status": "S", // S, P, and F for "success", "pending", and "failure"
    "tokenName": "LINKUP",
    "amount": "0.95590905", // subscribed token amount
    "cost": "9.99999995", // subscription cost in usdt
    "timestamp":1600249972899  
 }
POST /sapi/v1/blvt/subscribe (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	YES	BTCDOWN, BTCUP
cost	DECIMAL	YES	spot balance
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot&Margin Trading permission for the API Key which requests this endpoint.
Query Subscription Record (USER_DATA)
Response:
[  
  {
    "id": 1,  
    "tokenName": "LINKUP",
    "amount": "0.54216292", // Subscription amount
    "nav": "18.42621386", // NAV price of subscription 
    "fee": "0.00999000", // Subscription fee in usdt
    "totalCharge": "9.99999991", // Subscription cost in usdt
    "timestamp":1599127217916  
  }
]
GET /sapi/v1/blvt/subscribe/record (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	NO	BTCDOWN, BTCUP
id	LONG	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	default 1000, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Only the data of the latest 90 days is available
Redeem BLVT (USER_DATA)
Response:
 {
    "id": 123,  
    "status": "S", // S, P, and F for "success", "pending", and "failure"
    "tokenName": "LINKUP",
    "redeemAmount": "0.95590905",       // Redemption token amount
    "amount": "10.05022099",    // Redemption value in usdt
    "timestamp":1600250279614  
 }
POST /sapi/v1/blvt/redeem (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	YES	BTCDOWN, BTCUP
amount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot&Margin Trading permission for the API Key which requests this endpoint.
Query Redemption Record (USER_DATA)
Response:
[  
  {
    "id": 1,  
    "tokenName": "LINKUP",
    "amount": "0.54216292", // Redemption amount
    "nav": "18.36345064",  // NAV of redemption
    "fee": "0.00995598", // Reemption fee
    "netProceed": "9.94602604", // Net redemption value in usdt
    "timestamp":1599128003050  
  }
]
GET /sapi/v1/blvt/redeem/record (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	NO	BTCDOWN, BTCUP
id	LONG	NO	
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	default 1000, max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
Only the data of the latest 90 days is available
Get BLVT User Limit Info (USER_DATA)
Response:
[  
  {
    "tokenName": "LINKUP",
    "userDailyTotalPurchaseLimit": "1000", // USDT
    "userDailyTotalRedeemLimit": "1000"    // USDT
  },
  {
    "tokenName": "LINKDOWN",
    "userDailyTotalPurchaseLimit": "1000", // USDT
    "userDailyTotalRedeemLimit": "50000"   // USDT
  } 
]
GET /sapi/v1/blvt/userLimit (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tokenName	STRING	NO	BTCDOWN, BTCUP
recvWindow	LONG	NO	
timestamp	LONG	YES	
Websocket BLVT Info Streams
The BLVT NAV system is based on Binance Futures, so the endpoint is based on futures websocket service.

Please go to here to check the stream event and operate in accordance with the fstream or fstream3 usage specifications.

BLVT NAV Kline/Candlestick Streams
The BLVT NAV system is based on Binance Futures, so the endpoint is based on futures websocket service.

Please go to here to check the stream event and operate in accordance with the fstream or fstream3 usage specifications.

BSwap Endpoints

The endpoints below allow you to interact with BSwap.
For more information on this, please refer to the BSwap page
List All Swap Pools (MARKET_DATA)
Response:
[
    {
        "poolId": 2,
        "poolName": "BUSD/USDT",
        "assets": [
            "BUSD",
            "USDT"
        ]
    },
    {
        "poolId": 3,
        "poolName": "BUSD/DAI",
        "assets": [
            "BUSD",
            "DAI"
        ]
    },
    {
        "poolId": 4,
        "poolName": "USDT/DAI",
        "assets": [
            "USDT",
            "DAI"
        ]
    }
]
GET /sapi/v1/bswap/pools

Get metadata about all swap pools.

Weight(IP): 1

Parameters:

None

Get liquidity information of a pool (USER_DATA)
Response:
[
    {
        "poolId": 2,
        "poolNmae": "BUSD/USDT",
        "updateTime": 1565769342148,
        "liquidity": {
            "BUSD": 100000315.79,
            "USDT": 99999245.54
        },
        "share": {
            "shareAmount": 12415,
            "sharePercentage": 0.00006207,
            "asset": {
                "BUSD": 6207.02,
                "USDT": 6206.95
            }
        }
    }
]
GET /sapi/v1/bswap/liquidity (HMAC SHA256)

Get liquidity information and user share of a pool.

Weight(IP):

1 for one pool

10 when the poolId parameter is omitted

Parameter:

Name	Type	Mandatory	Description
poolId	LONG	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Add Liquidity (TRADE)
Response:
{
    "operationId": 12341
}
POST /sapi/v1/bswap/liquidityAdd (HMAC SHA256)

Add liquidity to a pool.

Weight(UID): 1000 (Additional: 1 request every three seconds)

Parameter:

Name	Type	Mandatory	Description
poolId	LONG	YES	
type	STRING	NO	"Single" to add a single token; "Combination" to add dual tokens. Default "Single"
asset	STRING	YES	
quantity	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Remove Liquidity (TRADE)
Response:
{
    "operationId": 12341
}
POST /sapi/v1/bswap/liquidityRemove (HMAC SHA256)

Remove liquidity from a pool, type include SINGLE and COMBINATION, asset is mandatory for single asset removal

Weight(UID): 1000 (Additional: 1 request every three seconds)

Parameters:

Name	Type	Mandatory	Description
poolId	LONG	YES	
type	STRING	YES	SINGLE for single asset removal, COMBINATION for combination of all coins removal
asset	LIST	NO	Mandatory for single asset removal
shareAmount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Liquidity Operation Record (USER_DATA)
Response:
[
    {
        "operationId": 12341,
        "poolId": 2,
        "poolName": "BUSD/USDT",
        "operation": "ADD", // "ADD" or "REMOVE"
        "status": 1, // 0: pending, 1: success, 2: failed 
        "updateTime": 1565769342148,
        "shareAmount": "10.1"
    }
]
GET /sapi/v1/bswap/liquidityOps (HMAC SHA256)

Get liquidity operation (add/remove) records.

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
operationId	LONG	NO	
poolId	LONG	NO	
operation	ENUM	NO	ADD or REMOVE
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	default 3, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
Request Quote (USER_DATA)
Response:
{
    "quoteAsset": "USDT",
    "baseAsset": "BUSD",
    "quoteQty": 300000,
    "baseQty": 299975,
    "price": 1.00008334,
    "slippage": 0.00007245,
    "fee": 120
}
GET /sapi/v1/bswap/quote (HMAC SHA256)

Request a quote for swap quote asset (selling asset) for base asset (buying asset), essentially price/exchange rates.

quoteQty is quantity of quote asset (to sell).

Please be noted the quote is for reference only, the actual price will change as the liquidity changes, it's recommended to swap immediate after request a quote for slippage prevention.

Weight(UID): 150

Parameters:

Name	Type	Mandatory	Description
quoteAsset	STRING	YES	
baseAsset	STRING	YES	
quoteQty	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Swap (TRADE)
Response:
{
    "swapId": 2314
}
POST /sapi/v1/bswap/swap (HMAC SHA256)

Swap quoteAsset for baseAsset.

Weight(UID): 1000 (Additional: 1 request every three seconds)

Parameters:

Name	Type	Mandatory	Description
quoteAsset	STRING	YES	
baseAsset	STRING	YES	
quoteQty	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Swap History (USER_DATA)
Response:
[
    {
        "swapId": 2314,
        "swapTime": 1565770342148,
        "status": 0, // 0: pending, 1: success, 2: failed 
        "quoteAsset": "USDT",
        "baseAsset": "BUSD",
        "quoteQty": 300000,
        "baseQty": 299975,
        "price": 1.00008334,
        "fee": 120
    }
]
GET /sapi/v1/bswap/swap (HMAC SHA256)

Get swap history.

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
swapId	LONG	NO	
startTime	LONG	NO	
endTime	LONG	NO	
status	INT	NO	0: pending for swap, 1: success, 2: failed
quoteAsset	STRING	NO	
baseAsset	STRING	NO	
limit	LONG	NO	default 3, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Pool Configure (USER_DATA)
Response:
[
    {
        "poolId": 2,
        "poolNmae": "BUSD/USDT",
        "updateTime": 1565769342148,
        "liquidity": {
            "constantA": 2000, //"NA" if pool is an innovation pool
            "minRedeemShare": 0.1,
            "slippageTolerance":0.2 //The swap proceeds only when the slippage is within the set range
        },   
        "assetConfigure":{
            "BUSD": {
                "minAdd":10,
                "maxAdd": 20, 
                "minSwap": 10,
                "maxSwap": 30            
            },
            "USDT": {
                "minAdd":10,
                "maxAdd": 20, 
                "minSwap": 10,
                "maxSwap": 30   
            }
        }
    }
]
GET /sapi/v1/bswap/poolConfigure (HMAC SHA256)

Weight(IP): 150

Parameters:

Name	Type	Mandatory	Description
poolId	LONG	NO	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Add Liquidity Preview (USER_DATA)
Response:
{
        "quoteAsset": "USDT",
        "baseAsset": "BUSD", //Display when type is "COMBINATION"
        "quoteAmt": 300000,
        "baseAmt": 299975, // Display when type is "COMBINATION" 
        "price": 1.00008334,
        "share":1.23,
        "slippage": 0.00007245, //Display when type is "SINGLE" 
        "fee": 120, //Display when type is "SINGLE" 
}
GET /sapi/v1/bswap/addLiquidityPreview (HMAC SHA256)

Calculate expected share amount for adding liquidity in single or dual token.

Weight(IP): 150

Parameters:

Name	Type	Mandatory	Description
poolId	LONG	YES	
type	STRING	YES	"SINGLE" for adding a single token;"COMBINATION" for adding dual tokens
quoteAsset	STRING	YES	
quoteQty	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Remove Liquidity Preview (USER_DATA)
Response:
{
        "quoteAsset": "USDT",
        "baseAsset": "BUSD", //Display when type is "COMBINATION" 
        "quoteAmt": 300000,
        "baseAmt": 299975, //Display when type is "COMBINATION" 
        "price": 1.00008334,
        "slippage": 0.00007245, //Display when type is "SINGLE" 
        "fee": 120 //Display when type is "SINGLE" 
}

GET /sapi/v1/bswap/removeLiquidityPreview (HMAC SHA256)

Calculate the expected asset amount of single token redemption or dual token redemption.

Weight(IP): 150

Parameters:

Name	Type	Mandatory	Description
poolId	LONG	YES	
type	STRING	YES	Type is "SINGLE", remove and obtain a single token;Type is "COMBINATION", remove and obtain dual token.
quoteAsset	STRING	YES	
shareAmount	DECIMAL	YES	
recvWindow	LONG	NO	
timestamp	LONG	YES	
Get Unclaimed Rewards Record (USER_DATA)
Response:
{
        "totalUnclaimedRewards": {         
            "BUSD": 100000315.79,
            "BNB": 0.00000001,
            "USDT": 0.00000002                              
         },         
    "details":{
            "BNB/USDT":{
                "BUSD": 100000315.79,
                "USDT": 0.00000002                        
                },
            "BNB/BTC":{
                "BNB": 0.00000001
                } 
        }
}


GET /sapi/v1/bswap/unclaimedRewards (HMAC SHA256)

Get unclaimed rewards record.

Weight(UID): 1000

Parameters:

Name	Type	Mandatory	Description
type	INT	NO	0: Swap rewards,1:Liquidity rewards, default to 0
recvWindow	LONG	NO	
timestamp	LONG	YES	
Claim Rewards (TRADE)
Response:
{
    "success":true
}

POST /sapi/v1/bswap/claimRewards (HMAC SHA256)

Claim swap rewards or liquidity rewards

Weight(UID): 1000

Parameters:

Name	Type	Mandatory	Description
type	INT	NO	0: Swap rewards,1:Liquidity rewards, default to 0
recvWindow	LONG	NO	
timestamp	LONG	YES	
You need to openEnable Spot & Margin Trading permission for the API Key which requests this endpoint.
Get Claimed History (USER_DATA)
Response:
[
    {
        "poolId":52,  
        "poolName":"BNB/USDT",                     
        "assetRewards": "BNB",
        "claimTime":1565769342148,             
        "claimAmount":0.00000023,
        "status":1 // 0: pending, 1: success
    }
]


GET /sapi/v1/bswap/claimedHistory (HMAC SHA256)

Get history of claimed rewards.

Weight(UID): 1000

Parameters:

Name	Type	Mandatory	Description
poolId	LONG	NO	
assetRewards	STRING	NO	
type	INT	NO	0: Swap rewards,1:Liquidity rewards, default to 0
startTime	LONG	NO	
endTime	LONG	NO	
limit	LONG	NO	Default 3, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
Fiat Endpoints

Get Fiat Deposit/Withdraw History (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": [
   {
      "orderNo":"7d76d611-0568-4f43-afb6-24cac7767365",
      "fiatCurrency": "BRL",
      "indicatedAmount": "10.00",  
      "amount": "10.00", 
      "totalFee": "0.00",   // Trade fee
      "method": "BankAccount",  // Trade method
      "status": "Expired",  // Processing, Failed, Successful, Finished, Refunding, Refunded, Refund Failed, Order Partial credit Stopped
      "createTime": 1626144956000,
      "updateTime": 1626400907000   
   }
   ],
   "total": 1,
   "success": true
}
GET /sapi/v1/fiat/orders (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
transactionType	STRING	YES	0-deposit,1-withdraw
beginTime	LONG	NO	
endTime	LONG	NO	
page	INT	NO	default 1
rows	INT	NO	default 100, max 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
If beginTime and endTime are not sent, the recent 30-day data will be returned.
Get Fiat Payments History (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": [
   {
      "orderNo": "353fca443f06466db0c4dc89f94f027a",
      "sourceAmount": "20.0",  // Fiat trade amount
      "fiatCurrency": "EUR",   // Fiat token
      "obtainAmount": "4.462", // Crypto trade amount
      "cryptoCurrency": "LUNA",  // Crypto token
      "totalFee": "0.2",     // Trade fee
      "price": "4.437472", 
      "status": "Failed",  // Processing, Completed, Failed, Refunded
      "createTime": 1624529919000,
      "updateTime": 1624529919000  
   }
   ],
   "total": 1,
   "success": true
}
GET /sapi/v1/fiat/payments (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
transactionType	STRING	YES	0-buy,1-sell
beginTime	LONG	NO	
endTime	LONG	NO	
page	INT	NO	default 1
rows	INT	NO	default 100, max 500
recvWindow	LONG	NO	
timestamp	LONG	YES	
If beginTime and endTime are not sent, the recent 30-day data will be returned.
C2C Endpoints

Get C2C Trade History (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": [
   {
      "orderNumber":"20219644646554779648",
      "advNo": "11218246497340923904",
      "tradeType": "SELL",  
      "asset": "BUSD", 
      "fiat": "CNY",  
      "fiatSymbol": "￥",
      "amount": "5000.00000000",  // Quantity (in Crypto)
      "totalPrice": "33400.00000000",
      "unitPrice": "6.68", // Unit Price (in Fiat)
      "orderStatus": "COMPLETED",  // PENDING, TRADING, BUYER_PAYED, DISTRIBUTING, COMPLETED, IN_APPEAL, CANCELLED, CANCELLED_BY_SYSTEM
      "createTime": 1619361369000,
      "commission": "0",   // Transaction Fee (in Crypto)
      "counterPartNickName": "ab***",
      "advertisementRole": "TAKER"        
     }
   ],
   "total": 1,
   "success": true
}
GET /sapi/v1/c2c/orderMatch/listUserOrderHistory (HMAC SHA256)

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
tradeType	STRING	YES	BUY, SELL
startTimestamp	LONG	NO	
endTimestamp	LONG	NO	
page	INT	NO	default 1
rows	INT	NO	default 100, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
If startTimestamp and endTimestamp are not sent, the recent 30-day data will be returned.
The max interval between startTimestamp and endTimestamp is 30 days.
Crypto Loans Endpoints

Get Crypto Loans Income History (USER_DATA)
Response:
[
   {
        "asset": "BUSD",
        "type": "borrowIn",
        "amount": "100",
        "timestamp": 1633771139847,
        "tranId": "80423589583"
    },
    {
        "asset": "BUSD",
        "type": "borrowIn",
        "amount": "100",
        "timestamp": 1634638371496,
        "tranId": "81685123491"
    }
 ]

GET /sapi/v1/loan/income (HMAC SHA256)

Weight(UID): 6000

Parameters:

Name	Type	Mandatory	Description
asset	STRING	YES	
type	STRING	NO	All types will be returned by default. Enum：borrowIn ,collateralSpent, repayAmount, collateralReturn(Collateral return after repayment), addCollateral, removeCollateral, collateralReturnAfterLiquidation
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	default 20, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
If startTime and endTime are not sent, the recent 7-day data will be returned.
The max interval between startTime and endTime is 30 days.
Pay Endpoints

Get Pay Trade History (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": [
   {
       "orderType": "C2C", // Enum：PAY(C2B Merchant Acquiring Payment), PAY_REFUND(C2B Merchant Acquiring Payment,refund), C2C(C2C Transfer Payment),CRYPTO_BOX(Crypto box), CRYPTO_BOX_RF(Crypto Box, refund), C2C_HOLDING(Transfer to new Binance user), C2C_HOLDING_RF(Transfer to new Binance user,refund), PAYOUT(B2C Disbursement Payment)
       "transactionId": "M_P_71505104267788288",  
       "transactionTime": 1610090460133, //trade timestamp
       "amount": "23.72469206", //order amount(up to 8 decimal places), positive is income, negative is expenditure
       "currency": "BNB", 
       "fundsDetail": [ //ddetails
               {
                "currency": "USDT", //asset 
                "amount": "1.2" 
                },
                {
                 "currency": "ETH",
                 "amount": "0.0001"
                }
          ]
     }
   ],
  "success": true
}
GET /sapi/v1/pay/transactions (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
startTimestamp	LONG	NO	
endTimestamp	LONG	NO	
limit	INT	NO	default 100, max 100
recvWindow	LONG	NO	
timestamp	LONG	YES	
If startTimestamp and endTimestamp are not sent, the recent 90 days' data will be returned.
The max interval between startTimestamp and endTimestamp is 90 days.
Support for querying orders within the last 18 months.
Convert Endpoints

Get Convert Trade History (USER_DATA)
Response:
{
   "list": [
        {
            "quoteId": "f3b91c525b2644c7bc1e1cd31b6e1aa6",
            "orderId": 940708407462087195,  
            "orderStatus": "SUCCESS",  // order status
            "fromAsset": "USDT",       // from asset
            "fromAmount": "20",        // from amount
            "toAsset": "BNB",          // to asset
            "toAmount": "0.06154036",  // to amount
            "ratio": "0.00307702",     // price ratio
            "inverseRatio": "324.99",  // inverse price 
            "createTime": 1624248872184
        }
   ],
    "startTime": 1623824139000,
    "endTime": 1626416139000,
    "limit": 100,
    "moreData": false
}
GET /sapi/v1/convert/tradeFlow (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	YES	
endTime	LONG	YES	
limit	INT	NO	Default 100, Max 1000
recvWindow	LONG	NO	
timestamp	LONG	YES	
The max interval between startTime and endTime is 30 days.
Rebate Endpoints

Get Spot Rebate History Records (USER_DATA)
Response:
{
   "status": "OK",
   "type": "GENERAL",
   "code": "000000000",
   "data": {
        "page": 1,  // current page
        "totalRecords": 2,  // total records
        "totalPageNum": 1,  // total pages
        "data": [
            {
                "asset": "USDT",  // rebate asset
                "type": 1,        // rebate type：1 is commission rebate，2 is referral kickback
                "amount": "0.0001126", 
                "updateTime": 1637651320000
            },
            {
                "asset": "ETH",
                "type": 1,
                "amount": "0.00000056",
                "updateTime": 1637928379000
            }
        ]
    }

}
GET /sapi/v1/rebate/taxQuery (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	NO	
endTime	LONG	NO	
page	INT	NO	Default 1
recvWindow	LONG	NO	
timestamp	LONG	YES	
The max interval between startTime and endTime is 30 days.
If startTime and endTime are not sent, the recent 7 days' data will be returned.
The earliest startTime is supported on June 10, 2020
NFT Endpoints

Get NFT Transaction History (USER_DATA)
Response:
{
  "total": 2,  //total records
  "list": [
    {
      "orderNo": "1_470502070600699904", // 0: purchase order, 1: sell order, 2: royalty income, 3: primary market order, 4: mint fee
      "tokens": [
        {
          "network": "BSC",  // NFT Network
          "tokenId": "216000000496",  // NFT Token ID
          "contractAddress": "MYSTERY_BOX0000087"  // NFT Contract Address
        }
      ],
      "tradeTime": 1626941236000,     
      "tradeAmount": "19.60000000",  
      "tradeCurrency": "BNB"            
    },
    {
      "orderNo": "1_488306442479116288",
      "tokens": [
        {
          "network": "BSC",
          "tokenId": "132900000007",
          "contractAddress": "0xAf12111a592e408DAbC740849fcd5e68629D9fb6"
        }
      ],
      "tradeTime": 1631186130000,
      "tradeAmount": "192.00000000",
      "tradeCurrency": "BNB"
    }
  ]
}
GET /sapi/v1/nft/history/transactions (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
orderType	INT	YES	0: purchase order, 1: sell order, 2: royalty income, 3: primary market order, 4: mint fee
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 50, Max 50
page	INT	NO	Default 1
recvWindow	LONG	NO	
timestamp	LONG	YES	
The max interval between startTime and endTime is 90 days.
If startTime and endTime are not sent, the recent 7 days' data will be returned.
Get NFT Deposit History(USER_DATA)
Response:
{
  "total": 2,
  "list": [
    {
      "network": "ETH",  // NFT Network
      "txID": null,      // Transaction ID
      "contractAdrress": "0xe507c961ee127d4439977a61af39c34eafee0dc6",  // NFT Contract Address
      "tokenId": "10014",   // NFT Token ID
      "timestamp": 1629986047000  
    },
    {
      "network": "BSC",
      "txID": null,
      "contractAdrress": "0x058451b463bab04f52c0799d55c4094f507acfa9",
      "tokenId": "10016",
      "timestamp": 1630083581000
    }
  ]
}
GET /sapi/v1/nft/history/deposit (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 50, Max 50
page	INT	NO	Default 1
recvWindow	LONG	NO	
timestamp	LONG	YES	
The max interval between startTime and endTime is 90 days.
If startTime and endTime are not sent, the recent 7 days' data will be returned.
Get NFT Withdraw History (USER_DATA)
Response:
{
  "total": 178,
  "list": [
    {
      "network": "ETH",
      "txID": "0x2be5eed31d787fdb4880bc631c8e76bdfb6150e137f5cf1732e0416ea206f57f",
      "contractAdrress": "0xe507c961ee127d4439977a61af39c34eafee0dc6",  // NFT Contract Address
      "tokenId": "1000001247",    // NFT Token ID
      "timestamp": 1633674433000, 
      "fee": 0.1,         // Withdraw Fee
      "feeAsset": "ETH"   // Asset
    },
    {
      "network": "ETH",
      "txID": "0x3b3aea5c0a4faccd6f306641e6deb9713ab229ac233be3be227f580311e4362a",
      "contractAdrress": "0xe507c961ee127d4439977a61af39c34eafee0dc6",
      "tokenId": "40000030",
      "timestamp": 1633677022000,
      "fee": 0.1,
      "feeAsset": "ETH"
    }
  ]
}
GET /sapi/v1/nft/history/withdraw (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
startTime	LONG	NO	
endTime	LONG	NO	
limit	INT	NO	Default 50, Max 50
page	INT	NO	Default 1
recvWindow	LONG	NO	
timestamp	LONG	YES	
The max interval between startTime and endTime is 90 days.
If startTime and endTime are not sent, the recent 7 days' data will be returned.
Get NFT Asset (USER_DATA)
Response:
{
  "total": 347,
  "list": [
    {
      "network": "BSC",  // NFT Network
      "contractAddress": "REGULAR11234567891779", // NFT Contract Address
      "tokenId": "100900000017"  // NFT Token ID
    },
    {
      "network": "BSC",
      "contractAddress": "SSMDQ8W59",
      "tokenId": "200500000011"
    },
    {
      "network": "BSC",
      "contractAddress": "SSMDQ8W59",
      "tokenId": "200500000019"
    }
  ]
}
GET /sapi/v1/nft/user/getAsset (HMAC SHA256)

Weight(UID): 3000

Parameters:

Name	Type	Mandatory	Description
limit	INT	NO	Default 50, Max 50
page	INT	NO	Default 1
recvWindow	LONG	NO	
timestamp	LONG	YES	
Binance Code Endpoints

Binance Code allows simple crypto transfer and exchange through secured and prepaid codes that give access to crypto assets. Binance Code API solution is to facilitate instant creation, redemption and value-checking for Binance Codes. Binance code consists of two parts: Reference number and Binance code. The reference number can circulate in public, and it can be used to verify the validity of the code; Binance Code should be kept carefully, because as long as someone has the code, they can redeem it anytime.

Note：The following endpoints do not currently support sub-account requests

Create a Binance Code (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": {
    "referenceNo": "0033002327977405", //Reference number
    "code": "AOGANK3NB4GIT3C6"         //Binance code
  },
   "success": true
}
POST /sapi/v1/giftcard/createCode (HMAC SHA256)

This API is for creating a Binance Code. To get started with, please make sure:

You have a Binance account
You have passed kyc
You have a sufﬁcient balance in your Binance funding wallet
You need Enable Withdrawals for the API Key which requests this endpoint.
Weight(IP): 1

Daily creation volume: 2 BTC / 24H Daily creation times: 200 Codes / 24H

Parameters:

Name	Type	Mandatory	Description
token	STRING	YES	The coin type contained in the Binance Code
amount	DOUBLE	YES	The amount of the coin
recvWindow	LONG	NO	
timestamp	LONG	YES	
Redeem a Binance Code (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": {
    "token":"BNB", //coin
    "amount":"10", //amount
    "referenceNo": "0033002327977405",    //reference number
    "identityNo": "10316281761814589440"  //ignore
  }, 
   "success": true
}
POST /sapi/v1/giftcard/redeemCode (HMAC SHA256)

This API is for redeeming the Binance Code. Once redeemed, the coins will be deposited in your funding wallet.

Please note that if you enter the wrong code 5 times within 24 hours, you will no longer be able to redeem any Binance Code that day.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
code	STRING	YES	Binance code
recvWindow	LONG	NO	
timestamp	LONG	YES	
Verify a Binance Code (USER_DATA)
Response:
{
   "code": "000000",
   "message": "success",
   "data": {
    "valid":true,  
    "token":"BNB",  // coin
    "amount":"0.00000001"  // amount
  }, 
   "success": true
}
GET /sapi/v1/giftcard/verify (HMAC SHA256)

This API is for verifying whether the Binance Code is valid or not by entering Binance Code or reference number.

Please note that if you enter the wrong binance code 5 times within an hour, you will no longer be able to verify any binance code for that hour.

Weight(IP): 1

Parameters:

Name	Type	Mandatory	Description
referenceNo	STRING	YES	reference number
recvWindow	LONG	NO	
timestamp	LONG	YES	
Error Codes

The error JSON payload:
{
  "code":-1121,
  "msg":"Invalid symbol."
}
Errors consist of two parts: an error code and a message. Codes are universal, but messages can vary.

10xx - General Server or Network issues
-1000 UNKNOWN

An unknown error occurred while processing the request.
An unknown error occurred while processing the request.[%s]
-1001 DISCONNECTED

Internal error; unable to process your request. Please try again.
-1002 UNAUTHORIZED

You are not authorized to execute this request.
-1003 TOO_MANY_REQUESTS

Too many requests queued.
Too much request weight used; please use the websocket for live updates to avoid polling the API.
Too much request weight used; current limit is %s request weight per %s %s. Please use the websocket for live updates to avoid polling the API.
Way too much request weight used; IP banned until %s. Please use the websocket for live updates to avoid bans.
-1004 SERVER_BUSY

Server is busy, please wait and try again
-1006 UNEXPECTED_RESP

An unexpected response was received from the message bus. Execution status unknown.
-1007 TIMEOUT

Timeout waiting for response from backend server. Send status unknown; execution status unknown.
-1014 UNKNOWN_ORDER_COMPOSITION

Unsupported order combination.
-1015 TOO_MANY_ORDERS

Too many new orders.
Too many new orders; current limit is %s orders per %s.
-1016 SERVICE_SHUTTING_DOWN

This service is no longer available.
-1020 UNSUPPORTED_OPERATION

This operation is not supported.
-1021 INVALID_TIMESTAMP

Timestamp for this request is outside of the recvWindow.
Timestamp for this request was 1000ms ahead of the server's time.
-1022 INVALID_SIGNATURE

Signature for this request is not valid.
-1099 Not found, authenticated, or authorized

This replaces error code -1999
11xx - 2xxx Request issues
-1100 ILLEGAL_CHARS

Illegal characters found in a parameter.
Illegal characters found in a parameter. %s
Illegal characters found in parameter %s; legal range is %s.
-1101 TOO_MANY_PARAMETERS

Too many parameters sent for this endpoint.
Too many parameters; expected %s and received %s.
Duplicate values for a parameter detected.
-1102 MANDATORY_PARAM_EMPTY_OR_MALFORMED

A mandatory parameter was not sent, was empty/null, or malformed.
Mandatory parameter %s was not sent, was empty/null, or malformed.
Param %s or %s must be sent, but both were empty/null!
-1103 UNKNOWN_PARAM

An unknown parameter was sent.
-1104 UNREAD_PARAMETERS

Not all sent parameters were read.
Not all sent parameters were read; read %s parameter(s) but was sent %s.
-1105 PARAM_EMPTY

A parameter was empty.
Parameter %s was empty.
-1106 PARAM_NOT_REQUIRED

A parameter was sent when not required.
Parameter %s sent when not required.
-1111 BAD_PRECISION

Precision is over the maximum defined for this asset.
-1112 NO_DEPTH

No orders on book for symbol.
-1114 TIF_NOT_REQUIRED

TimeInForce parameter sent when not required.
-1115 INVALID_TIF

Invalid timeInForce.
-1116 INVALID_ORDER_TYPE

Invalid orderType.
-1117 INVALID_SIDE

Invalid side.
-1118 EMPTY_NEW_CL_ORD_ID

New client order ID was empty.
-1119 EMPTY_ORG_CL_ORD_ID

Original client order ID was empty.
-1120 BAD_INTERVAL

Invalid interval.
-1121 BAD_SYMBOL

Invalid symbol.
-1125 INVALID_LISTEN_KEY

This listenKey does not exist.
-1127 MORE_THAN_XX_HOURS

Lookup interval is too big.
More than %s hours between startTime and endTime.
-1128 OPTIONAL_PARAMS_BAD_COMBO

Combination of optional parameters invalid.
-1130 INVALID_PARAMETER

Invalid data sent for a parameter.
Data sent for parameter %s is not valid.
-1131 BAD_RECV_WINDOW

recvWindow must be less than 60000
-2010 NEW_ORDER_REJECTED

NEW_ORDER_REJECTED
-2011 CANCEL_REJECTED

CANCEL_REJECTED
-2013 NO_SUCH_ORDER

Order does not exist.
-2014 BAD_API_KEY_FMT

API-key format invalid.
-2015 REJECTED_MBX_KEY

Invalid API-key, IP, or permissions for action.
-2016 NO_TRADING_WINDOW

No trading window could be found for the symbol. Try ticker/24hrs instead.
3xxx-5xxx SAPI-specific issues
-3000 INNER_FAILURE

Internal server error.
-3001 NEED_ENABLE_2FA

Please enable 2FA first.
-3002 ASSET_DEFICIENCY

We don't have this asset.
-3003 NO_OPENED_MARGIN_ACCOUNT

Margin account does not exist.
-3004 TRADE_NOT_ALLOWED

Trade not allowed.
-3005 TRANSFER_OUT_NOT_ALLOWED

Transferring out not allowed.
-3006 EXCEED_MAX_BORROWABLE

Your borrow amount has exceed maximum borrow amount.
-3007 HAS_PENDING_TRANSACTION

You have pending transaction, please try again later.
-3008 BORROW_NOT_ALLOWED

Borrow not allowed.
-3009 ASSET_NOT_MORTGAGEABLE

This asset are not allowed to transfer into margin account currently.
-3010 REPAY_NOT_ALLOWED

Repay not allowed.
-3011 BAD_DATE_RANGE

Your input date is invalid.
-3012 ASSET_ADMIN_BAN_BORROW

Borrow is banned for this asset.
-3013 LT_MIN_BORROWABLE

Borrow amount less than minimum borrow amount.
-3014 ACCOUNT_BAN_BORROW

Borrow is banned for this account.
-3015 REPAY_EXCEED_LIABILITY

Repay amount exceeds borrow amount.
-3016 LT_MIN_REPAY

Repay amount less than minimum repay amount.
-3017 ASSET_ADMIN_BAN_MORTGAGE

This asset are not allowed to transfer into margin account currently.
-3018 ACCOUNT_BAN_MORTGAGE

Transferring in has been banned for this account.
-3019 ACCOUNT_BAN_ROLLOUT

Transferring out has been banned for this account.
-3020 EXCEED_MAX_ROLLOUT

Transfer out amount exceeds max amount.
-3021 PAIR_ADMIN_BAN_TRADE

Margin account are not allowed to trade this trading pair.
-3022 ACCOUNT_BAN_TRADE

You account's trading is banned.
-3023 WARNING_MARGIN_LEVEL

You can't transfer out/place order under current margin level.
-3024 FEW_LIABILITY_LEFT

The unpaid debt is too small after this repayment.
-3025 INVALID_EFFECTIVE_TIME

Your input date is invalid.
-3026 VALIDATION_FAILED

Your input param is invalid.
-3027 NOT_VALID_MARGIN_ASSET

Not a valid margin asset.
-3028 NOT_VALID_MARGIN_PAIR

Not a valid margin pair.
-3029 TRANSFER_FAILED

Transfer failed.
-3036 ACCOUNT_BAN_REPAY

This account is not allowed to repay.
-3037 PNL_CLEARING

PNL is clearing. Wait a second.
-3038 LISTEN_KEY_NOT_FOUND

Listen key not found.
-3041 BALANCE_NOT_CLEARED

Balance is not enough
-3042 PRICE_INDEX_NOT_FOUND

PriceIndex not available for this margin pair.
-3043 TRANSFER_IN_NOT_ALLOWED

Transferring in not allowed.
-3044 SYSTEM_BUSY

System busy.
-3045 SYSTEM

The system doesn't have enough asset now.
-3999 NOT_WHITELIST_USER

This function is only available for invited users.
-4001 CAPITAL_INVALID

Invalid operation.
-4002 CAPITAL_IG

Invalid get.
-4003 CAPITAL_IEV

Your input email is invalid.
-4004 CAPITAL_UA

You don't login or auth.
-4005 CAPAITAL_TOO_MANY_REQUEST

Too many new requests.
-4006 CAPITAL_ONLY_SUPPORT_PRIMARY_ACCOUNT

Support main account only.
-4007 CAPITAL_ADDRESS_VERIFICATION_NOT_PASS

Address validation is not passed.
-4008 CAPITAL_ADDRESS_TAG_VERIFICATION_NOT_PASS

Address tag validation is not passed.
-4010 CAPITAL_WHITELIST_EMAIL_CONFIRM

White list mail has been confirmed.
-4011 CAPITAL_WHITELIST_EMAIL_EXPIRED

White list mail is invalid.
-4012 CAPITAL_WHITELIST_CLOSE

White list is not opened.
-4013 CAPITAL_WITHDRAW_2FA_VERIFY

2FA is not opened.
-4014 CAPITAL_WITHDRAW_LOGIN_DELAY

Withdraw is not allowed within 2 min login.
-4015 CAPITAL_WITHDRAW_RESTRICTED_MINUTE

Withdraw is limited.
-4016 CAPITAL_WITHDRAW_RESTRICTED_PASSWORD

Within 24 hours after password modification, withdrawal is prohibited.
-4017 CAPITAL_WITHDRAW_RESTRICTED_UNBIND_2FA

Within 24 hours after the release of 2FA, withdrawal is prohibited.
-4018 CAPITAL_WITHDRAW_ASSET_NOT_EXIST

We don't have this asset.
-4019 CAPITAL_WITHDRAW_ASSET_PROHIBIT

Current asset is not open for withdrawal.
-4021 CAPITAL_WITHDRAW_AMOUNT_MULTIPLE

Asset withdrawal must be an %s multiple of %s.
-4022 CAPITAL_WITHDRAW_MIN_AMOUNT

Not less than the minimum pick-up quantity %s.
-4023 CAPITAL_WITHDRAW_MAX_AMOUNT

Within 24 hours, the withdrawal exceeds the maximum amount.
-4024 CAPITAL_WITHDRAW_USER_NO_ASSET

You don't have this asset.
-4025 CAPITAL_WITHDRAW_USER_ASSET_LESS_THAN_ZERO

The number of hold asset is less than zero.
-4026 CAPITAL_WITHDRAW_USER_ASSET_NOT_ENOUGH

You have insufficient balance.
-4027 CAPITAL_WITHDRAW_GET_TRAN_ID_FAILURE

Failed to obtain tranId.
-4028 CAPITAL_WITHDRAW_MORE_THAN_FEE

The amount of withdrawal must be greater than the Commission.
-4029 CAPITAL_WITHDRAW_NOT_EXIST

The withdrawal record does not exist.
-4030 CAPITAL_WITHDRAW_CONFIRM_SUCCESS

Confirmation of successful asset withdrawal.
-4031 CAPITAL_WITHDRAW_CANCEL_FAILURE

Cancellation failed.
-4032 CAPITAL_WITHDRAW_CHECKSUM_VERIFY_FAILURE

Withdraw verification exception.
-4033 CAPITAL_WITHDRAW_ILLEGAL_ADDRESS

Illegal address.
-4034 CAPITAL_WITHDRAW_ADDRESS_CHEAT

The address is suspected of fake.
-4035 CAPITAL_WITHDRAW_NOT_WHITE_ADDRESS

This address is not on the whitelist. Please join and try again.
-4036 CAPITAL_WITHDRAW_NEW_ADDRESS

The new address needs to be withdrawn in {0} hours.
-4037 CAPITAL_WITHDRAW_RESEND_EMAIL_FAIL

Re-sending Mail failed.
-4038 CAPITAL_WITHDRAW_RESEND_EMAIL_TIME_OUT

Please try again in 5 minutes.
-4039 CAPITAL_USER_EMPTY

The user does not exist.
-4040 CAPITAL_NO_CHARGE

This address not charged.
-4041 CAPITAL_MINUTE_TOO_SMALL

Please try again in one minute.
-4042 CAPITAL_CHARGE_NOT_RESET

This asset cannot get deposit address again.
-4043 CAPITAL_ADDRESS_TOO_MUCH

More than 100 recharge addresses were used in 24 hours.
-4044 CAPITAL_BLACKLIST_COUNTRY_GET_ADDRESS

This is a blacklist country.
-4045 CAPITAL_GET_ASSET_ERROR

Failure to acquire assets.
-4046 CAPITAL_AGREEMENT_NOT_CONFIRMED

Agreement not confirmed.
-4047 CAPITAL_DATE_INTERVAL_LIMIT

Time interval must be within 0-90 days
-5001 ASSET_DRIBBLET_CONVERT_SWITCH_OFF

Don't allow transfer to micro assets.
-5002 ASSET_ASSET_NOT_ENOUGH

You have insufficient balance.
-5003 ASSET_USER_HAVE_NO_ASSET

You don't have this asset.
-5004 USER_OUT_OF_TRANSFER_FLOAT

The residual balances have exceeded 0.001BTC, Please re-choose.
The residual balances of %s have exceeded 0.001BTC, Please re-choose.
-5005 USER_ASSET_AMOUNT_IS_TOO_LOW

The residual balances of the BTC is too low
The residual balances of %s is too low, Please re-choose.
-5006 USER_CAN_NOT_REQUEST_IN_24_HOURS

Only transfer once in 24 hours.
-5007 AMOUNT_OVER_ZERO

Quantity must be greater than zero.
-5008 ASSET_WITHDRAW_WITHDRAWING_NOT_ENOUGH

Insufficient amount of returnable assets.
-5009 PRODUCT_NOT_EXIST

Product does not exist.
-5010 TRANSFER_FAIL

Asset transfer fail.
-5011 FUTURE_ACCT_NOT_EXIST

future account not exists.
-5012 TRANSFER_PENDING

Asset transfer is in pending.
-5021 PARENT_SUB_HAVE_NO_RELATION

This parent sub have no relation
-5012 FUTURE_ACCT_OR_SUBRELATION_NOT_EXIST

future account or sub relation not exists.
6XXX - Savings Issues
-6001 DAILY_PRODUCT_NOT_EXIST

Daily product not exists.
-6003 DAILY_PRODUCT_NOT_ACCESSIBLE

Product not exist or you don't have permission
-6004 DAILY_PRODUCT_NOT_PURCHASABLE

Product not in purchase status
-6005 DAILY_LOWER_THAN_MIN_PURCHASE_LIMIT

Smaller than min purchase limit
-6006 DAILY_REDEEM_AMOUNT_ERROR

Redeem amount error
-6007 DAILY_REDEEM_TIME_ERROR

Not in redeem time
-6008 DAILY_PRODUCT_NOT_REDEEMABLE

Product not in redeem status
-6009 REQUEST_FREQUENCY_TOO_HIGH

Request frequency too high
-6011 EXCEEDED_USER_PURCHASE_LIMIT

Exceeding the maximum num allowed to purchase per user
-6012 BALANCE_NOT_ENOUGH

Balance not enough
-6013 PURCHASING_FAILED

Purchasing failed
-6014 UPDATE_FAILED

Exceed up-limit allowed to purchased
-6015 EMPTY_REQUEST_BODY

Empty request body
-6016 PARAMS_ERR

Parameter err
-6017 NOT_IN_WHITELIST

Not in whitelist
-6018 ASSET_NOT_ENOUGH

Asset not enough
-6019 PENDING

Need confirm
-6020 PROJECT_NOT_EXISTS

Project not exists
70xx - Futures
-7001 FUTURES_BAD_DATE_RANGE

Date range is not supported.
-7002 FUTURES_BAD_TYPE

Data request type is not supported.
-9xxx Filter failures
Error message	Description
"Filter failure: PRICE_FILTER"	price is too high, too low, and/or not following the tick size rule for the symbol.
"Filter failure: PERCENT_PRICE"	price is X% too high or X% too low from the average weighted price over the last Y minutes.
"Filter failure: LOT_SIZE"	quantity is too high, too low, and/or not following the step size rule for the symbol.
"Filter failure: MIN_NOTIONAL"	price * quantity is too low to be a valid order for the symbol.
"Filter failure: ICEBERG_PARTS"	ICEBERG order would break into too many parts; icebergQty is too small.
"Filter failure: MARKET_LOT_SIZE"	MARKET order's quantity is too high, too low, and/or not following the step size rule for the symbol.
"Filter failure: MAX_POSITION"	The account's position has reached the maximum defined limit. 
This is composed of the sum of the balance of the base asset, and the sum of the quantity of all open BUYorders.
"Filter failure: MAX_NUM_ORDERS"	Account has too many open orders on the symbol.
"Filter failure: MAX_NUM_ALGO_ORDERS"	Account has too many open stop loss and/or take profit orders on the symbol.
"Filter failure: MAX_NUM_ICEBERG_ORDERS"	Account has too many open iceberg orders on the symbol.
"Filter failure: EXCHANGE_MAX_NUM_ORDERS"	Account has too many open orders on the exchange.
"Filter failure: EXCHANGE_MAX_NUM_ALGO_ORDERS"	Account has too many open stop loss and/or take profit orders on the exchange.
10xxx - Futures Cross Collateral
-10017 REPAY_CHECK_BEYOND_LIABILITY

Repay amount should not be larger than liability.
13xxx - BLVT
-13000 BLVT_FORBID_REDEEM

Redeption of the token is forbiden now
-13001 BLVT_EXCEED_DAILY_LIMIT

Exceeds individual 24h redemption limit of the token
-13002 BLVT_EXCEED_TOKEN_DAILY_LIMIT

Exceeds total 24h redemption limit of the token
-13003 BLVT_FORBID_PURCHASE

Subscription of the token is forbiden now
-13004 BLVT_EXCEED_DAILY_PURCHASE_LIMIT

Exceeds individual 24h subscription limit of the token
-13005 BLVT_EXCEED_TOKEN_DAILY_PURCHASE_LIMIT

Exceeds total 24h subscription limit of the token
-13006 BLVT_PURCHASE_LESS_MIN_AMOUNT

Subscription amount is too small
-13007 BLVT_PURCHASE_AGREEMENT_NOT_SIGN

The Agreement is not signed
12xxx - Liquid Swap
-12014 TOO MANY REQUESTS

More than 1 request in 3 seconds
45xxx - Binance Code
-450001

This token is not currently supported, please re-enter
-450005

Amount cannot be 0, please re-enter
The amount is too small, please re-enter
-450017

The total amount of codes you created has exceeded the 24-hour limit, please try again after UTC 0
-450018

Too many codes created in 24 hours, please try again after UTC 0
-450020

Too many invalid verify attempts, please try later
-450022

Too many invalid redeem attempts in 24 hours, please try again after UTC 0
Order Rejection Issues
Error messages like these are indicated when the error is coming specifically from the matching engine:

-1010 ERROR_MSG_RECEIVED
-2010 NEW_ORDER_REJECTED
-2011 CANCEL_REJECTED
The following messages which will indicate the specific error:

Error message	Description
"Unknown order sent."	The order (by either orderId, clientOrderId, origClientOrderId) could not be found.
"Duplicate order sent."	The clientOrderId is already in use.
"Market is closed."	The symbol is not trading.
"Account has insufficient balance for requested action."	Not enough funds to complete the action.
"Market orders are not supported for this symbol."	MARKET is not enabled on the symbol.
"Iceberg orders are not supported for this symbol."	icebergQty is not enabled on the symbol
"Stop loss orders are not supported for this symbol."	STOP_LOSS is not enabled on the symbol
"Stop loss limit orders are not supported for this symbol."	STOP_LOSS_LIMIT is not enabled on the symbol
"Take profit orders are not supported for this symbol."	TAKE_PROFIT is not enabled on the symbol
"Take profit limit orders are not supported for this symbol."	TAKE_PROFIT_LIMIT is not enabled on the symbol
"Price * QTY is zero or less."	price * quantity is too low
"IcebergQty exceeds QTY."	icebergQty must be less than the order quantity
"This action disabled is on this account."	Contact customer support; some actions have been disabled on the account.
"Unsupported order combination"	The orderType, timeInForce, stopPrice, and/or icebergQty combination isn't allowed.
"Order would trigger immediately."	The order's stop price is not valid when compared to the last traded price.
"Cancel order is invalid. Check origClientOrderId and orderId."	No origClientOrderId or orderId was sent in.
"Order would immediately match and take."	LIMIT_MAKER order type would immediately match and trade, and not be a pure maker order.
"The relationship of the prices for the orders is not correct."	The prices set in the OCO is breaking the Price rules. 
The rules are: 
SELL Orders: Limit Price > Last Price > Stop Price 
BUY Orders: Limit Price < Last Price < Stop Price
"OCO orders are not supported for this symbol"	OCO is not enabled on the symbol.
"Quote order qty market orders are not support for this symbol."	MARKET orders using the parameter quoteOrderQty are not enabled on this symbol.
Notes

Request Parameters
Email Address: uvhwuvhw@gmail.com

# ftx_stake_accounts
Exploration of FTX/Alameda Solana stake accounts

## Background
This is data in support of this post, explaining a method used to identify the Alameda stake accounts and various keys:
[https://twitter.com/solanobahn/status/1697488177945284722?s=20](https://twitter.com/solanobahn/status/1697488177945284722?s=20)

## Disclaimer
This data is a best-guess attempt at measuring the amount of stake [formerly] controlled by Alameda Research and/or FTX. It is not an allegation of wrongdoing by anyone. 
It is an impartial attempt to identify which accounts, and how many SOL tokens these entities controlled. There will be errors, either by mistake or omission. USE OF THIS DATA IS AT YOUR OWN RISK.
The data is not presented as the basis for the reader to buy or sell any digital assets, and is expressly not financial advice. 

## Verify Data Integrity
Read HOW_TO_VERIFY_DATA.md

## Files
#### activity:
* 3HDLCsoyLPA8PWcH4D3Vn38ge3RX9KAE2D6qTdAwBeRw = Alameda staking accounts "controller"
* 9fzhgGN5vyumFWAExvvE5YSKRhk7RNL53qPYusL9h6To = Alameda's signer on recent large, 3.1M stake withdrawal
* stake_program_event_log_ftx_until_20230831.csv = history of these stake accounts going back to Feb 2023 (CAUTION (!): this is not the entire history of any of these stake accounts)
* stake_program_event_log_shortlist_until_20230831.csv = isolated view of activity for specific accounts of interest

#### address_lists:
* all_ftx_staking_addresses.csv = all staker, withdrawer, stakePubkey, and misc Alameda addresses
* shortlist.csv = specifi
* spl_transfer_authority.csv = list of accounts that were the "authority" on an SPL token transfer signed by 3HDLCsoyLPA8PWcH4D3Vn38ge3RX9KAE2D6qTdAwBeRw
* stakePubkey.csv = list of unique stake accounts ONLY
* staker.csv = list of unique stake authority ONLY
* withdrawer.csv = list of unique withdraw authority ONLY

#### stake_data:
* ftx_stakes_20230831_u.csv = data grepped (using all_ftx_staking_addresses.csv) from Solana CLI command `solana stakes --output json | in2csv --format json > solana_stakes.csv` 

#### stats:
* ftx_stake_stats.csv = summary table pulled from a postgresql database that shows the various instruction data by date. Supported instructions are: initialize, delegate, deactivate, and withdraw (missing: merge, and others... sorry!)

## Contact
To discuss this research please contact:

email: [ashpoolin@protonmail.com](mailto:ashpoolin@protonmail.com)

twitter: [solanobahn](https://twitter.com/solanobahn)

github: [github.com/ashpoolin](https://github.com/ashpoolin/)

web: [gelato.sh](https://www.gelato.sh/)

## Support
On-chain research is not particularly lucrative, and data + hardware is expensive. If this work has been helpful to you, please consider giving me a tip:
* Solana: 4EiLmcLNYYYQq9H2B1ESDDf8WwMKeCcp5heDgrp8SL2w
* Ethereum: 0xb397d6Af4CB79c9a845d90222f9fd887E38beaC4
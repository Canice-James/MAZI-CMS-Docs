# Tournaments in NR1
A tournament is a competitive event in which players compete to win rewards. Players get points for any bets or wins, and their score is displayed on the tournament leaderboard. The player with the highest score at the end of a tournament is a winner and will receive a reward. Depending on the terms and conditions of each tournament, players in other places can also get rewards.
1. To create a new tournament in NR1, open the **Tournaments** menu.

![Tournaments_menu](nr1_tournament.png ':size=900') 

2. On the **Tournaments** page, click the **Plus** button. 

![Tournaments_page](tournament_nr1_2.png ':size=900') 

3. In the **Tournament** dialog, specify the following information: 

![Tournaments_dialog](tournaments_nr1_dialog.png ':size=600') 

- **Alias**: Tournament alias. Aliases in NR1 and CMS must be identical. 
- **Name**: Tournament name.
- **Active**: Select this checkbox to activate a tournament.
- **Providers (all games)**: All games of a selected provider that will be featured in a tournament.
- **Providers (live)**: All live games of a selected provider that will be featured in a tournament.
- **Games**: Specific games that will be featured in a tournament. The providers’ fields must be empty.
- **Countries**: Countries that will feature different games for this tournament.
    - **Country**: Country where other games will be featured.
    - **Country providers (all games)**: All games of a selected provider in the specified country that will be featured in a tournament.
    - **Country games**: Specific games in the selected country that will be featured in a tournament. The providers’ field must be empty.
- **Min players**: Minimum number of players for the tournament to be successful. If the minimum number of players is not met by the end of the tournament, no participants will receive rewards.
- **Min bets (EUR)**: Minimum bet amount (specified in EUR) required to participate in a tournament.
- **Pool**: Amount of a tournament reward. 
- **Pool type**: Type of a tournament reward: bonus, loyalty, coins, cash.
- **Wager**: Number of times a bonus must be wagered before any winnings can be withdrawn. 40 is set by default.
- **Date from**: Date and time when the tournament is supposed to start. The start date must be in the future and cannot be later than the end date.
- **Date to**: Date and time when the tournament is supposed to finish. The end date must be later than the start date.
- **Type**: Type of a tournament in terms of recurrence.
    - **Once**: One-time tournament. 
    - **Repeatable**: Repetitive tournament:
        - **Start**: Day of the week when a tournament will start.
        - **Duration**: Number of times a tournament will be repeated.
- **Domains**: Brands that will have this tournament.
- **Currency**: Rewards currency.
- **Sport**: Select this checkbox for a sports tournament.
- **Sort by points**: If "Total Win from the bet / Bet Amount" - select, if "Total Bet converted in EURO" - leave unselected.
- **Autocrediting**: Automatic crediting of winnings.
- **Championship IDs**: Championship IDs that will be featured in a tournament.

### Tournament rewards
Tournament rewards (a pool) are specified in the tournament settings. The pool amount can be distributed among the participants. There are two options: a fixed sum in a currency or a percentage of the total pool amount.

To distribute rewards:
1. On the **Tournaments** page, click the **Prize** icon.
2. In the **Tournament rewards** dialog, click the **Plus** button and enter a sum or percentage for each place in a new row.

Note that the total amount cannot exceed the tournament pool amount. 

![Tournaments_rewards](tourn_gif.gif ':size=900')
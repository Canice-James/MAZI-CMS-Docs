# Achievements in NR1
Achievements is a reward system aimed at engaging players in new casino and sports activities. They come in various forms, such as weekly challenges, and can be triggered by different actions, such as deposits, logins, placing bets, joining tournaments, and others. For example, a player who deposits 200 euros will receive 15 coins as an achievement.
1. To create an achievement in NR1, open **Administration> Achievements**.

![Achievements_menu](achiev_nr1.png ':size=900') 

2. On the **Achievements** page, select your project at the bottom of the page and click **Load**.
3. To add a new achievement, click the **Add new record** button. 

![Achievements_page](achiev_nr1_2.png ':size=900') 

4. In the **Update achievement** dialog, specify the following information:

![Achievements_dialog](achievement_dialog.png ':size=400') 

* **Active**: Select this checkbox to activate an achievement.
* **Start date**: Time and date when achievement will be available.
* **End date**: Time and date when achievement will be no longer available.
* **Is booster**: Booster achievement. Booster achievements are connected to “trophies” (simple, composite, or progressive achievements).
* **Achievement ID**: Random number to monitor achievements within the platform. 
* **Name**: Achievement name. 
* **Type**: Achievement type.
* **Composit**: Achievement triggered by completing other achievements.
* **Composit_collection**: Specific type of an achievement (a collection) that is triggered by completing other achievements.
* **Period**: Periodical achievement (for example, weekly challenges).
* **Progressive**: Achievement triggered by multiple actions (for example, 50 spins).
* **Simple**: Achievement triggered by one action (for example, a first deposit).
* **Trigger**:
  * **any_login**: Achievement is triggered by the player’s login.
  * **any_shop_buy**: Achievement is triggered by a shop purchase.
  * **app_login**: Achievement is triggered by the player’s mobile login.
  * **card_bought**: Achievement is triggered by a card purchase.
  * **coin_change**: Achievement is triggered by coin exchange.
  * **collection_bought**: Achievement is triggered by completing a collection.
  * **deposit** (simple/progressive/period): Achievement is triggered by a first deposit.
  * **email_verify**: Achievement is triggered by email verification.
  * **express_bet** (period): Achievement is triggered by a multi-sport bet.
  * **favorites**
  * **free_spin** (simple): Achievement is triggered by a first free spin.
  * **games_spin** (progressive): Achievement is triggered by spins in slots and casino games.
  * **level (simple)**: Achievement is triggered by reaching a specific level.
  * **login (simple)**: Achievement is triggered by a first login (desktop).
  * **mask_bought**: Achievement is triggered by purchasing masks.
  * **mask_changing** (simple/progressive): Achievement is triggered by purchasing a costume or several costumes.
  * **mobile_play** (simple): Achievement is triggered by a mobile play.
  * **none**: Achievement without a trigger.
  * **percent_bonus**
  * **shooting_spin**: Achievement is triggered by shoots (spins) in the Shooting range.
  * **single_bet**: Achievement is triggered by a single sports bet.
  * **spin (progressive)**: Achievement is triggered by placing a bet in a specific game.
  * **spin11/spin50/spin53**: Achievement is triggered by making a specific number of spins.
  * **system_bet**: Achievement is triggered by a combined bet in sports.
  * **taken_achievement**: Achievement is triggered by the completion of another specific achievement.
  * **total_earned_coins** (simple): Achievement is triggered by depositing a sum of money.
  * **tournament_participant** (simple): Achievement is triggered when a player gets a place in a tournament.
  * **tournament_prize** (simple): Achievement is triggered when a player gets a prize in a tournament.
  * **tournament_win** (simple): Achievement is triggered when a player wins a tournament.
  * **vip_level**: Achievement is triggered by reaching a specific VIP level.
  * **virtual_bet**: Achievement is triggered by a bet in a virtual sport. 
  * **win_spin** (progressive): Achievement is triggered by winning a certain sum of money.
  * **withdrawal** (simple): Achievement is triggered by a first withdrawal.
* **Category**: Achievement category.
* **Game providers**: Game provider whose game will be featured in this achievement. The “Game providers” and “Game” should be selected if the achievement includes only one specific game.
* **Game**: Game of the selected game provider that will be featured in this achievement.
* **Games**: Games of different providers that will be featured in this achievement.
* **Tags**: Achievement tags.

**Edit JSON fields**: Clicking this button will display two additional fields: **Rules** and **Data**.

### Achievement rules

These are main JSON rules and their explanation:
* **min**: Minimum value required for the achievement trigger to work. Depending on the achievement trigger it might be:
    * Minimum bet amount. E.g.: "min": 0.3 for spin trigger reads minimum bet counted toward the achievement is €0.3.
    * Minimum win amount. E.g.: "min": 100 for win_spin trigger reads minimum winning counted toward the achievement is €100.
    * Minimum deposit amount. E.g.: "min": 100 for deposit trigger reads minimum deposit counted toward the achievement is €100.
* **finish**: Defines how many times a trigger should work for the achievement to be completed.
* **reward**: Amount of reward. Units of measurement are defined by the accompanying parameters **isBonusReward** or **isRealReward**.
* **isBonusReward**: True/false value defining the type of the reward (real or bonus). For bonus rewards, the type is defined in the bonusRewardType field.
* **bonusRewardType**: Coins, loyalty points, freespins, bonus money.
* **isRealReward**: Real money.
* **level**: Numeric parameter that defines the level player should gain to complete the achievement.
* **autoTake**: A flag that defines whether the reward will be credited automatically or a user should claim the reward, or CS manager should add it to the user account manually, for example. 
* **periodicity**: How often an achievement is refreshed: daily, weekly, etc.
* **allowedGamesIds**: Allowed game IDs.
* **outcomes**: An array of specific achievement sub-rules; can contain minOdd, minSize, championshipIds, categoryIds.
* **championshipIds**: IDs of championships that qualify for an achievement.
* **categoryIds**: IDs of sport categories that qualify for an achievement. 
* **sportIds**: IDs of sports that qualify for an achievement.
* **minOdd**: Minimum odd for a sport bet that qualifies for an achievement.
* **minSize**: Minimum number of outcomes for sport bets that qualify for an achievement.
* **winsOnly**: True/ False. Achievement progress is updated ONLY if the user's bet on the associated event results is win (True).
* **dynamicRewardRate**: A factor to multiply the reward. E.g.: "dynamicRewardRate"=1.5 for a deposit trigger means that the deposit amount will be multiplied by 1.5 and the resulting sum will be credited to the user account. There are some achievement that elaborate on that functionality in a more complex way. I.e., an achievement required a user to make 10 bets. With "dynamicRewardRate"=0.05, every time user places a bet, 5% of it are added to the reward. When the achievement is complete, user is going to receive the compound amount. 
* **type**: A field for specific achievements that include extra logic. I.e.: placing a bet every day for a week; winning a tournament.
* **deposit** along with **transactionsNumber**: A deposit counter for achievements that require a certain number of deposits to be made (2, 5, etc.) .
* **isLiveGame**: Live game for casino-related achievements (true/false):
  * **true** – limits the games to Live games only.
  * **false** – excludes Live games from the list games that qualify for the achievement progress.
* **maxTournamentPlace**: Defines the maximum tournament position user should obtain to get an achievement. I.e., maxTournamentPlace = 50 translates to receiving any place from 1-50 in an in-house tournament.
* **tournamentPrizePoolTypes**: Defines the Tournament award type user should receive to get an achievement. In other words, limits the achievement to a certain prize type: 
  * **coins** – fortune coins.
  * **loyalty** – loyalty coins.
  * **bonus** – bonus money
  E.g., with tournamentPrizePoolTypes = coins, user should participate in a tournament and get some coins as a reward for that tournament. For now, there is no way to point out the number of coins/bonus money/etc. user should win.

#### Achievements specifics
Achievements can award coins, real money, free spins, and bonuses.
Progressive achievements have two conditions:
* **minimum** – the minimum step user needs to perform to progress in that achievements (i.e., bet = 1$; if user bets <1$, the progress is not added).
* **finish** – achievement is fulfilled, reward can be collected.

### Most popular achievements
#### Deposit amount
This is an achievement for depositing a certain amount of money.

Type: simple.

Trigger: total_earned_coins

Rules: `{"type": "max", "finish": 180000, "reward": 5000, "autoTake": true, "isRealReward": true}`
* This achievement is awarded for depositing 180000 EUR, which is defined by the value of the "finish" parameter.
* The reward is 5000 EUR in real money (defined by the "isRealReward" parameter).
* The reward is automatically taken (the "autoTake" parameter).

#### First Deposit
This achievement is awarded for the first deposit.

Type: simple

Trigger: deposit

Rules: `{"finish": 1, "reward": 1}`

Optional parameters: `{"finish": 1, "reward": 1, "autoTake": true}`

#### First withdrawal 
This achievement is awarded for the first withdrawal.

Type: simple

Trigger: withdrawal

Rules: `{"finish": 1, "reward": 1}`

#### Second deposit
This achievement is awarded for making the second deposit.

Type: progressive

Trigger: deposit

Rules: `{"finish": 1, "reward": 1, "deposit": {"transactionsNumber": 2}, "autoTake": true}`

* Tracking the number of deposits here is performed with the help of the "transactionsNumber": 2 parameter inside the "deposit" parameter. Changing the number for transactionsNumber parameter will turn this achievement into Make N-th deposit. 
* The reward is automatically taken with the help of an autobonus configured for this achievement.

#### Single win
This achievement is awarded for a single winning of a certain amount of money.

Type: progressive

Trigger: win_spin

Rules: `{"min": 100, "finish": 1, "reward": 1, "autoTake": true}`

* This achievement is awarded for a single winning of 100 EUR. Changing the value of the "min" parameter defines the amount of money user should win to get that achievement.
* The award is granted automatically via an autobonus associated with the achievement.

#### Make a number of spins in slot games
This achievement is awarded for making spins in slot games.

Type: progressive

Trigger: games_spin

Rules: `{"finish": 100, "reward": 1, "autoTake": true, "allowedGamesIds": [11111, 11112]}`

* To get this achievement user should perform 100 spins ("finish": 100) in one of the games that are defined in the allowedGamesIds array.
* The reward is automatically taken with the help of an autobonus associated with it.

#### Make a bet N days in a row

This achievement is awarded for making a bet several days in a row.

Type: progressive

Trigger: games_spin

Rules: `{"type": "dayByDay", "finish": 10, "reward": 1, "autoTake": true}`

* To accomplish this achievement, user should make a bet 10 days in a row. Changing the value of the "finish" parameter will change the number of days the bets should be made.
* The reward is granted via an autobonus configured for this achievement.   

##### Make bets in a certain game
This achievement is awarded for placing bets in a defined game. If an achievement is tied to a single game, the game ID is should be explicitly defined. Otherwise, if spins in multiple games should be counted towards the achievement progression, the array of games should be added to the "allowedGamesIds" parameter in rules.

Type: progressive

Trigger: spin

Rules: `{"min": 0.3, "finish": 150, "reward": 1}`
* "min" parameter defines the minimum size of the bet valid for the achievement.
* "finish" parameter defines the number of spins a person should make.
* "reward" is 1 EUR in this case.
* The ID of the game is defined in a separate NR1 field, and in the game_id parameter of the achievements table on the back-end side. 

Optional parameters:
`{"min": 0.3, "finish": 150, "reward": 1, "allowedGamesIds": [11111, 11112]}`

* This achievement follows the same rules, but supports an array of slot games.

#### Level
These achievements are awarded for reaching levels.

Type: simple

Trigger: level

Rules: `{"level": 85, "finish": 1, "reward": 0, "autoTake": true, "isBonusReward": true, "bonusRewardType": "bonusMoney"}`

* The reward for this achievement is some amount of bonus money granted automatically: this is done by having an autobonus configured in NR1 system that is associated with this achievement. 

#### First login

This achievement is awarded for the first user login.

Type: simple

Trigger: login

Rules: `{"finish": 1, "reward": 1}`

#### First freespin

This achievement is awarded for the first used freespin.

Type: simple

Trigger: free_spin

Rules: `{"finish": 1, "reward": 1}`

#### First mask change (buy a costume)
This achievement is awarded for the costume purchase. 

Type: simple

Trigger: mask_changing

Rules: `{"finish": 1, "reward": 1, "autoTake": true}`

#### First mobile play

This achievement is awarded for the first mobile play.

Type: simple

Trigger: mobile_play

Rules: `{"finish": 1, "reward": 1}`

Optional parameters: `{"finish": 1, "reward": 1, "autoTake": true}`

#### First coin exchange
This achievement is awarded for the first coin exchange.

Type: simple

Trigger: coin_change

Rules: `{"finish": 1, "reward": 1}`

Optional parameters: {`"finish": 1, "reward": 1, "autoTake": true}`

#### Purchase multiple costumes
This achievement is awarded for purchasing several costumes.

Type: progressive

Trigger: mask_changing

Rules: `{"finish": 5, "reward": 1, "autoTake": true}`

* Changing the value of the "finish" parameter defines the number of costumes to purchase to get this achievement.
* The award is assigned automatically via an autobonus configured for this achievement. 

#### Tournament position
This achievement is awarded when user participates in an in-house tournament and finishes it on a certain place (not limited to prize places). For example, one can set up an achievement for top10, top50, and top100.

In order not to provide multiple achievements to a user (i.e., top100, top50 and top 10 for ending up on position #8 in a tournament), consecutive achievements can be used.

Type: simple

Trigger: tournament_participant

Rules: `{"finish": 1, "reward": 1, "maxTournamentPlace": 50}`

#### Tournament Prize Type
Defines the Tournament award type user should receive to get an achievement. In other words, user should participate in an in-house tournament and receives a certain type of prize for it.

Available values: ["coins" | "loyalty" | "bonus"]

E.g., with tournamentPrizePoolTypes = coins, user should participate in a tournament and get some coins as a reward for that tournament. For now, there is no way to point out the number of coins/bonus money/etc. user should win.

Type: simple

Trigger (any):
* tournament_win
* tournament_prize
* tournament_participant

Rules: `{"finish": 1, "reward": 1, "maxTournamentPlace": 50, "tournamentPrizePoolTypes": ["coins"]}`

#### Tournament win
This achievement is awarded when user wins a tournament.

Type: simple

Trigger: tournament_win or tournament_prize

Rules: `{"finish": 1, "reward": 1}`

#### Place a number of bets in Live Casino
This achievement is awarded to players who make a number of bets in Live Casino.

Type: progressive

Trigger: games_spin

Rules: `{"finish": 100, "reward": 1, "autoTake": true, "isLiveGame": true}`

* isLiveGame parameter limits the allowed games for this achievement to Live Casino only.
* The reward is granted automatically due to having an autobonus in NR1 system associated with this achievement. 

#### Weekly deposit
This achievement is granted for depositing a certain amount of money. It can be earned once a week.

Type: period

Trigger: deposit

Rules: `{"min": 10, "finish": 1, "autoTake": true, "periodicity": "isoWeek", "dynamicRewardRate": 2}`

* Awarded for making a minimum deposit of 10 EUR ("min": 10).
* The achievement can be accomplished once a week ("periodicity": "isoWeek")
* The reward depends on the deposit amount – users deposit is multiplied by a factor defined in the "dynamicRewardRate" parameter. E.g., if a user has deposited 50 EUR with "dynamicRewardRate" parameter set to 2, he will get another 100 EUR on top of his deposit. 
* The reward is automatically awarded ("autoTake": true)

#### Weekly sport achievement
This achievement is awarded for placing a bet on a certain sport with some extra conditions. 

Type: period

Trigger: express_bet

Rules:
`{"finish": 1, "autoTake": true, "outcomes": {"minOdd": 1.3, "minSize": 3, "championshipIds": [111111, 111112]}, "periodicity": "isoWeek", "dynamicRewardRate": 1}`

* The "outcomes" parameter limits the bets that are valid for the achievement in question:
  * "minOdd" parameter means that only bets with an odd of 1.3 qualifies for that achievement.
  * "minSize" limits the minimum number of outcomes for sport bets that qualify for an achievement.
  * "championshipIds" array limits the list of championships that qualify for an achievement. In the example above, for example, only basketball championships are listed to limit the achievement to basketball betting only.
* The achievement can be accomplished once a week ("periodicity": "isoWeek")
* The reward depends on the betting amount – user's bet is multiplied by a factor defined in the "dynamicRewardRate" parameter. E.g., if a user has betted 50 EUR with "dynamicRewardRate" parameter set to 2, he will get 100 EUR. 
* The reward is obtained automatically ("autoTake": true).


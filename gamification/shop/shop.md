# Shop
Players can exchange virtual currency in a Shop to buy items that enhance their gaming experience and provide additional benefits. They can spend coins for bonus money, free spins, free bets, and other items depending on the game.
The most common types of shop items are:
* Free spins: Spins in slot games. 
* Free bets: Placing bets in a sportsbook. 
* Exchange: Buying bonus money for coins. 
* Bonus money: Money that can be used in casino games.

1. To create a shop item in NR1, open **Administration > Shop products**. 

![Shop_products](shop_nr1.png ':size=900') 

2. On the **Shop products** page, select your project at the bottom of the page and click **Load**. 
3. To add a new shop item, click the **Add new record** button. 

![Shop_add_new](shop_nr1_add.png ':size=900') 

4. In the Update shop product dialog, specify the following information: 

![Shop_dialog](shop_dialog.png ':size=400') 

* **Active**: Select this checkbox to activate a shop item.
* **Single buying**: If this checkbox is selected, this shop item will be available for purchase only once.
* **Product ID**: Random digit to monitor shop items within the platform. Use last used ID number + 1.
* **Type**: Shop item type (avatar, cash crab, exchange, fortune coin, free bet, freespin, mask, raffle ticket, twist).
* **Game providers** and **Game**: Select a provider and game only when creating a shop item for a specific game (for example, for freespins).
* **Alias**: Information about a shop item (for example, "freespin_5_11111" for 5 free spins, "11111" - Game ID for a new shop item).
* **Price**: Price of a shop item in coins.
* **Offer**: Amount of shop items (for example, 10 free spins). 
* **Wager**: Bonus wager requirements. The bonus must be wagered several times before any associated winnings can be withdrawn. 40 is set by default.
* **Plan ID**: ID for a sport bonus plan (for example, for free bets). 
* **Add new record**: Clicking this button opens 2 additional fields: Currency and Value. They are used only for “free bet” and “exchange” shop item types and to convert coins into the player’s local currency.
  * **Currency**: Currency code.
  * **Value**: Currency amount (for example, 50 euros).

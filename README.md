MiniVault Plugin
MiniVault is a lightweight and easy-to-use economy plugin for Minecraft servers, offering essential economy features similar to Vault but with a smaller, more streamlined approach. It supports basic commands for managing balances, transferring money between players, selling items, and viewing a simple in-game shop. The plugin is compatible with Paper 1.8+ servers and can be extended or customized to fit your server's needs.

Features:
/balance: View your current balance in the game.

/pay <player> <amount>: Transfer money to another player.

/sell: Sell items you're holding (DIAMOND, EMERALD, CACTUS, and more).

/sell <item> <amount>: Sell items directly from your inventory by specifying the item and quantity.

/shop: Display a list of available items for sale, along with their prices.

Simple Shop: Built-in shop to sell DIAMOND, EMERALD, CACTUS, and other items with prices.

Supported Items and Prices:
DIAMOND = $100.00 each

EMERALD = $75.00 each

IRON_INGOT = $10.00 each

GOLD_INGOT = $20.00 each

CACTUS = $5.00 each

How to Set Up the Plugin:
Download and Install:

Download the MiniVault.jar file from GitHub.

Place the MiniVault.jar file in your server's plugins folder.

Restart or reload your server to generate the necessary files.

Configure plugin.yml:

The plugin will automatically generate a plugin.yml file upon startup. This file contains configuration for commands like /balance, /pay, /sell, and /shop.

How to Use:
1. Check Your Balance:
To see how much money you have in your account, simply type:

bash
Copy
Edit
/balance
This will display your current balance in the game.

2. Send Money to Another Player:
To send money to another player, use the /pay command:

php-template
Copy
Edit
/pay <player> <amount>
For example, to send $50 to a player named Steve, type:

bash
Copy
Edit
/pay Steve 50
The player will receive the specified amount, and you'll see a confirmation message.

3. Selling Items:
To sell items, hold the item in your hand and type:

bash
Copy
Edit
/sell
This will sell the item you're holding (if it is one of the items available for sale in the plugin, like DIAMOND, EMERALD, etc.). The price for each item is predefined in the plugin.

Alternatively, you can sell directly from your inventory by specifying the item name and quantity:

php-template
Copy
Edit
/sell <item> <amount>
For example, to sell 64 cactus from your inventory, type:

bash
Copy
Edit
/sell cactus 64
The plugin will deduct the specified amount of items and pay you the corresponding amount of money.

4. View the Shop:
To see what items are available for sale and their prices, use the /shop command:

bash
Copy
Edit
/shop
This will display a list of sellable items, such as:

diff
Copy
Edit
---------------------------
Sell Shop:
- DIAMOND = $100.00
- EMERALD = $75.00
- IRON_INGOT = $10.00
- GOLD_INGOT = $20.00
- CACTUS = $5.00
---------------------------
Customizing the Plugin:
You can easily extend or modify the shop items and prices by editing the setupShop() method in the MiniVault.java file. To add a new item or change the price, simply add a new line to the sellPrices map like this:

java
Copy
Edit
sellPrices.put(Material.<ITEM_NAME>, <PRICE>);
For example, to add GOLD_NUGGET to the shop for $1.00:

java
Copy
Edit
sellPrices.put(Material.GOLD_NUGGET, 1.0);
After making changes, save the file, recompile the plugin, and restart your server.

Troubleshooting:
Plugin Not Loading:

Make sure you have the correct version of Paper (1.8 or higher).

Double-check that the plugin .jar file is placed in the correct plugins folder.

Check the server logs for any errors when loading the plugin.

Commands Not Working:

Ensure the player has permission to run the commands. You may need to set up permissions using a plugin like PermissionsEx or LuckPerms.

Check for any typos in the commands.

License:
This plugin is open-source and can be freely used or modified for personal or commercial use. If you make any modifications or enhancements, feel free to contribute back to this repository!

Contributing:
Fork this repository and make your improvements.

Submit a pull request with any bug fixes or new features you want to contribute.

File an issue if you encounter any bugs or have suggestions for new features.

With this plugin, you’ll have a simple, efficient, and customizable economy system for your Minecraft server without the complexity of full-featured plugins like Vault. It’s great for smaller servers or for those who just want to manage a few basic commands to handle in-game currency and transactions!

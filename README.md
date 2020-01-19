# Quests

Create quests/missions for users to go on to earn rewards.

This has been remade completely within GUI. All the quest creation/editing/removal is done through the GUI. Each page has its own instructions for use, therefore I won't need to explain how to use it here, it is essentially fool-proof.

Features

    Complete GUI menu for accepting quests
    Create/Edit/Remove quests from with the menu
    View all available quests and accept them with the click of a button
    See your current quest progress by viewing the "My Quests" tab
    Claim your rewards through the quest menu
    Create NPC's to issue rewards (requires HumanNPC)
    Create NPC's for delivery missions (requires HumanNPC)
    Currently 5 different quest types to choose from; Loot, Gather, Kill, Craft, Delivery
    Issue rewards in the form of items, RP(ServerRewards), Coins(Economics), XP (Rust), XP (HuntRPG)
    Quest cool down to tackle quest spamming

Important Information - Be sure to read this!

    To create/edit/remove quests you must be auth1/2
    When creating/edit and you are prompted to type something you do **NOT **require a "/" infront of the word/sentence, nor do you require quotation marks
    Follow the instructions given and you won't have any issues!
    Quest items will be taken from the user upon collection

BetterChat character limits
In some cases you may want to set a quest with 1x Bear kill for example, however BetterChat has a minimum character limit for messages. To bypass this simply use 0's infront of your single or double digit. Example. 1 will become 001, 10 will become 010 and so on.

Delivery Missions and Quest Vendors- MUST READ
_How do delivery missions work? _A delivery mission is unlike the other available quest types. Delivery missions require multiple delivery vendors. The user must visit one delivery vendor, that vendor will then ask the user to deliver a package to another delivery vendor. The amount of reward for completing a delivery missions varies based on a multiplier (see below) and the distance between the 2 vendors.
You can add new delivery/quest vendors VIA the Creation Menu

    Each vendor has their own reward and multiplier.
    When requesting a delivery mission a random vendor will be chosen.
    The reward amount is calculated based on distance between the 2 vendors
    Always consider what the maximum reward could be.
    The minimum amount of a item will always be 1
    If you want to give something like a** weapon as a reward**, but don't want the player to get 100 Assault Rifles set the multiplier to 0

When creating a new delivery vendor keep in mind that the multiplier will work as follows;
Vendor A is 2000m away from Vendor B. If the reward multiplier is 0.75 the reward amount will be 2000 x 0.75 = 1500.

LustyMap Delivery and Quest vendor icon support
Download the icons from CHAOS_CODE (search for Plugin Attachments)

    You must extract the icons to the oxide/data/LustyMap/custom folder prior to adding any vendors
    When you add a new vendor a new icon will automatically appear on the map
    There is enough delivery vendor icons for 15 vendors. I have included the .psd if you want to modify or add more icons .

Editing item names for translation
To translate item names to another language you must copy the file 'quests_itemnames.json' from your server. This can be found in the 'oxide/data/Quests/' folder.
Open the file in your preferred text editor and you will see every ingame item.
Each entry will look like this: "rifle.ak": "Assault Rifle",
The** left** side is the items short name, you must NOT edit this. Only edit the name on the right hand side.
Once you are done editing, unload the plugin and then upload the modified file and overwrite the original.
If you come into any errors after doing this you can delete the file and let the plugin generate you a new one.

Chat Commands
/q - Opens the quest menu
/questnpc - Used to register a NPC vendor (requires you to start the process through the menu!) You may also assign a name to the NPC by adding the name after the command.
Example: /questnpc Lakeside Vendor
*Note that the name is not required to be in quotation marks

Config

```json
{
  "Colors": {
    "Background_Dark": {
      "Alpha": 0.98,
      "Color": "#2a2a2a"
    },
    "Background_Light": {
      "Alpha": 0.3,
      "Color": "#696969"
    },
    "Button_Accept": {
      "Alpha": 0.9,
      "Color": "#00cd00"
    },
    "Button_Cancel": {
      "Alpha": 0.9,
      "Color": "#8c1919"
    },
    "Button_Completed": {
      "Alpha": 0.9,
      "Color": "#829db4"
    },
    "Button_Pending": {
      "Alpha": 0.9,
      "Color": "#a8a8a8"
    },
    "Button_Standard": {
      "Alpha": 0.9,
      "Color": "#2a2a2a"
    },
    "TextColor_Primary": "#ce422b",
    "TextColor_Secondary": "#939393"
  },
  "DisableUI_FadeIn": false,
  "KeybindOptions": {
    "Autoset_KeyBind": false,
    "KeyBind_Key": "k"
  },
  "LustyMapIntegration": {
    "Icon_Delivery": "deliveryicon",
    "Icon_Vendor": "vendoricon"
  },
  "UseNPCVendors": false
}
```

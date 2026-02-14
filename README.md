# ChatResponderMC

**ChatResponderMC** is a simple Spigot plugin for Minecraft servers running version 1.21 or later. This plugin allows you to define custom messages sent to a player depending on the result of a placeholder when mentioning a username in Minecraft chat.

## Example Use
ChatResponderMC automatically responds to player messages based on placeholders.

For example, using `%essentials_afk%`, if a player who is currently AFK is mentioned, the plugin will notify the player who mentioned them:

**In-game example:**
[Player1]: Hi Player2
[ChatResponderMC]: Player2 is currently AFK!

You can define multiple placeholders to create custom responses for different plugins or conditions.

---

## Example Config

```yaml
verbose: false # Set to false to disable detailed logs

afk_check:
  placeholder: "%essentials_afk%"
  expected_result: "yes"
  true_message: "&7&o{player} is currently AFK."
  false_message: "disabled" # No false message for this placeholder

placeholder2:
  placeholder: "%otherplugin_someplaceholder%"
  expected_result: "true"
  true_message: "&a{player} is here!"
  false_message: "&c{player} is not here." # Set to "disabled" to not send a message on false output
```

## Installation
1. Download the latest release from the [Releases](https://github.com/Alfie51m/ChatResponderMC/releases) section.
2. Download the latest release of [PlaceholderAPI](https://hangar.papermc.io/HelpChat/PlaceholderAPI), this plugin is required when using ChatResponderMC.
3. Place the `.jar` files in your server's `plugins` folder.
3. Restart your server.

## Contributing
Feel free to submit issues or contribute via pull requests on the [GitHub repository](https://github.com/Alfie51m/ChatResponderMC).

## License
This project is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt).

--- 

### **Thanks for using ChatResponderMC**
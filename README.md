<!-- Plugin pages -->
[traincarts]: https://www.spigotmc.org/resources/39592/
[itemsadder]: https://www.spigotmc.org/resources/73355/

<!-- GitHub Links -->
[releases]: https://github.com/Andre601/TCMinecartVariants/releases
[license]: https://github.com/Andre601/TCMinecartVariants/blob/main/LICENSE

<!-- Other Links -->
[ia-wiki]: https://itemsadder.devs.beer
[mc-packs]: https://mc-packs.net
[jsonmerger]: https://itemsadder.github.io/jsonmerger/

# TCMinecartVariants

<a href="https://discord.gg/6dazXp6" target="_blank">
  <img alt="discord" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@2/assets/minimal/social/discord-singular_vector.svg" height="64" align="right">
</a>
<a href="https://app.revolt.chat/invite/74TpERXA" target="_blank">
  <img alt="revolt" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@2/assets/minimal/social/revolt-singular_vector.svg" height="64" align="right">
</a>

TCMinecartVariants is a collection of JSON model files for Minecraft: Java Edition and was made as a way to add custom models to the plugin [TrainCarts][traincarts].  
The goal is to add new Minecart models with different ores loaded.

## Disclaimer

This resource does NOT add new Minecart models to the game. This is NOT a mod nor a plugin.  
The added models are customized Iron Horse Armor, using the `CustomModelData` attribute of Minecraft. This means it only supports MC versions with CustomModelData support.

## Contents

The downloadable zip from the Releases page contains the following files and folders:

- `TCMinecartVariants.zip` - Standalone Resource pack made for Minecraft 1.18.x (Older/Newer versions may work but require changes to the `pack.mcmeta`'s `pack_format`).
- `tcminecartvariants.yml` - YAML file for the plugin [TrainCarts][traincarts] which adds saved trains to use ([Instructions](#traincarts)).
- `assets/` - Folder containing the files of the resource. Can be added to plugins such as [ItemsAdder][itemsadder] ([Instructions](#itemsadder)).

## Installation

The resource can be installed in different ways, depending on different conditions.

### Before you start...

Something important to note here is, that the models use the `iron_horse_armor` as their base-item with `CustomModelData` values to change the used model for the item.  
Because of this should you be careful whenever you add the resources to another resource pack (or a plugin) that already uses the aforementioned item.

You can use the [JSONMerger tool][jsonmerger] provided by LoneDev to merge two JSON files into one.

### Standalone Resource pack

> Remember to read [Before you start...](#before-you-start) first.

- Download `TCMinecartVariants-<version>.zip` from the [Release page][releases].
- Extract the `TCMinecartVariants.zip` file from it.
- Upload the zip file to a hosting platform such as [mc-packs.net][mc-packs].
- Copy the direct download URL. Redirects do not work. The URL needs to result in the zip being downloaded.
- Paste the URL as the `resource-pack` value in your `server.properties` file.
- (Optional but recommended) Set the `resource-pack-sha1` to a valid SHA1 of your resource pack. Sites such as mc-packs provide one.
- Restart the server.

### Include into own resource pack

> Remember to read [Before you start...](#before-you-start) first.

- Download `TCMinecartVariants-<version>.zip` from the [Release page][releases].
- Extract the `assets/` folder from it.
- Add the folder to your resource pack's own `assets/` folder.
  - There should now be a path called `assets/tcminecartvariants/models/minecarts/`
- Update your zip file.

> **Note**  
> Always give proper credit to me and this repository. Read the [license file][license] for details.

### ItemsAdder

> Remember to read [Before you start...](#before-you-start) first.

TCMinecartVariants can be added to ItemsAdder, but with certain limitations.

#### Version 3.2.5 and older

- Download `TCMinecartVariants-<version>.zip` from the [Release page][releases].
- Extract the `assets/` folder from it.
- Move the folder into `plugins/ItemsAdder/data/resource_pack/`.
- Run `/iazip` and update your hosted resource pack. Refer to the [ItemsAdder Wiki][ia-wiki] for details.

> **Note**  
> This resource pack does not support getting Items through `/iaget`, `/iagive` or the `/ia` GUI. You have to use the vanilla `/give` command to obtain the item.  
> See the [command](#command) section for instructions.

#### Version 3.3.0 and newer

- Download `TCMinecartVariants-<version>.zip` from the [Release page][releases].
- Extract the `assets/` folder from it.
- Create a folder called `tcminecartvariants/` in `/plugins/ItemsAdder/contents/`
- Create a `resourcepack/` folder inside it.
- Drag and Drop the contents of `assets/` into the `resourcepack/` folder.
  - There should now be a path called `plugins/ItemsAdder/contents/tcminecartvariants/resourcepack/tcminecartvariants/models/minecarts/` and one called `plugins/ItemsAdder/contents/tcminecartvariants/resourcepack/minecraft/models/item/`
- Run `/iazip` and update your hosted resource pack. Refer to the [ItemsAdder Wiki][ia-wiki] for details.

> **Note**  
> This resource pack does not support getting Items through `/iaget`, `/iagive` or the `/ia` GUI. You have to use the vanilla `/give` command to obtain the item.  
> See the [command](#command) section for instructions.

### Other Custom Item plugins

Unfortunately can I not give instructions on other plugins that add custom items through automatically generated resource packs.  
Please refer to their respective documentation for instructions. All the important files are found in `assets/minecraft/models/item/` and `assets/tcminecartvariants/models/minecarts/` respectively.

## Getting the items

### Items

The following models are provided with their respective CustomModelData value or TrainCarts name:

| Minecart Model                | CustomModelData | TrainCarts name               |
| ----------------------------- | --------------- | ----------------------------- |
| `coal_minecart`               | `30000`         | `coal_minecart`               |
| `copper_minecart`             | `30001`         | `copper_minecart`             |
| `diamond_minecart`            | `30002`         | `diamond_minecart`            |
| `emerald_minecart`            | `30003`         | `emerald_minecart`            |
| `gold_minecart`               | `30004`         | `gold_minecart`               |
| `iron_minecart`               | `30005`         | `iron_minecart`               |
| `lapis_minecart`              | `30006`         | `lapis_minecart`              |
| `redstone_minecart`           | `30007`         | `redstone_minecart`           |
| `deepslate_coal_minecart`     | `30020`         | `deepslate_coal_minecart`     |
| `deepslate_copper_minecart`   | `30021`         | `deepslate_copper_minecart`   |
| `deepslate_diamond_minecart`  | `30022`         | `deepslate_diamond_minecart`  |
| `deepslate_emerald_minecart`  | `30023`         | `deepslate_emerald_minecart`  |
| `deepslate_gold_minecart`     | `30024`         | `deepslate_gold_minecart`     |
| `deepslate_iron_minecart`     | `30025`         | `deepslate_iron_minecart`     |
| `deepslate_lapis_minecart`    | `30026`         | `deepslate_lapis_minecart`    |
| `deepslate_redstone_minecart` | `30027`         | `deepslate_redstone_minecart` |
| `minecart`                    | `30040`         | `minecart`                    |


### Command

Use `/give @p iron_horse_armor{CustomModelData:<model_data>} 1` to give yourself the right item.  
Make sure to replace `<model_data>` with one of the [above listed](#items) numbers.

> **Warning**  
> The command may not work the same way on older versions. It could also work differently if a plugin such as EssentialsX overrides it. You can always prefix `give` with `minecraft:` to force the usage of the vanilla command (`/minecraft:give ...`).

**Example:**  
To get the `deepslate_diamond_minecart` would the command be `/give @p iron_horse_armor{CustomModelData:30022} 1`

### TrainCarts

TCMinecartVariants provides a `tcminecartvariants.yml` file, which contains saved trains for [TrainCarts][traincarts] to use.

To obtain such a train, make sure to have moved the `tcminecartvariants.yml` file into `plugins/Train_Carts/savedTrainModules/`. You may need to reload the plugin for it to be added properly.  
After this can you use `/train chest give @p --train <name>` to obtain a Chest to spawn the train. Make sure to replace `<name>` with one of the [above listed names](#items).

**Example:**  
To get the `deepslate_diamond_minecart` would the command be `/train chest give @p --train deepslate_diamond_minecart`

## License

This resource is provided under the MIT License. Please read the [LICENSE file][license] for details.

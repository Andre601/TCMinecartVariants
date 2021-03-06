<!-- Plugin pages -->
[traincarts]: https://www.spigotmc.org/resources/39592/
[itemsadder]: https://www.spigotmc.org/resources/73355/

<!-- GitHub Links -->
[releases]: https://github.com/Andre601/TCMinecartVariants/releases
[license]: https://github.com/Andre601/TCMinecartVariants/blob/main/LICENSE

<!-- Other Links -->
[ia-wiki]: https://itemsadder.devs.beer

# TCMinecartVariants

TCMinecartVariants is a collection of JSON model files for Minecraft: Java Edition and was made as a way to add custom models to the plugin [TrainCarts][traincarts].  
The goal is to add new Minecart models with different ores loaded.

## Disclaimer

This resource does NOT add new Minecart models to the game. This is NOT a mod nor a plugin.  
The added models are customized Iron Horse Armor, using the `CustomModelData` attribute of Minecraft.

## Contents

The downloadable zip from the Releases page contains the following files and folders:

- `TCMinecartVariants.zip` - Standalone Resource pack made for Minecraft 1.18.x (Older versions may work but require changes to the `pack.mcmeta`'s `pack_format`).
- `tcminecartvariants.yml` - YAML file for the plugin [TrainCarts][traincarts] which adds saved trains to use ([Instructions](#traincarts)).
- `assets/` - Folder containing the files of the resource. Can be added to plugins such as [ItemsAdder][itemsadder] ([Instructions](#itemsadder)).

## Installation

The resource can be installed in different ways, depending on different conditions.

### Before you start...

Something important to note here is, that the models use the `iron_horse_armor` as their base-item with `CustomModelData` values to change the used model for the item.  
Because of this should you be careful whenever you add the resources to another resource pack (or a plugin) that already uses the aforementioned item.

### Standalone Resource pack

This resource ships with its own Standalone resource pack.  
To add it to your server, download the `TCMinecartVariants-<version>.zip` from the [Releases page][releases], extract the `TCMinecartVariants.zip` file from it and upload it somewhere that allows direct downloads of the resource pack. A personal recommendation is https://mc-packs.net, which not only provides a way to host the resource pack, but also gives a SHA1 code to add to your server's `server.properties` file.

Once you uploaded the resource pack, copy the download URL and add it to the `resource-pack` option in your `server.properties` file. It's recommendet to also add a valid SHA1 code to the `resource-pack-sha1` option.

### Include into own resource pack

To add the models into your own resource pack, download the `TCMinecartVariants-<version>.zip` from the [Releases page][releases], extract the `assets` folder from it and add it to your resource pack's `assets` directory.

Please be aware of the things mentioned in [`Before you start...`](#before-you-start) before you attempt to add it to your stuff.
Also, give proper credit to me and follow the [MIT license][license]

### ItemsAdder

TCMinecartVariants can be added to ItemsAdder, but with certain limitations.

To add it to ItemsAdder, download the `TCMinecartVariants-<version>.zip` from the [Releases page][releases], extract the `assets` folder from it and drag and drop it into `plugins/ItemsAdder/data/resource_pack/`.  
After that run `/iazip` to refresh the Resource pack. Depending on your hosting solution will you need to update the download URL. Refer to the [ItemsAdder Wiki][ia-wiki] for further details.

Note that this resource does NOT add a way for you to obtain the items through the `/ia` GUI, `/iagive` or `/iaget`. You have to use the [vanilla `/give` command](#command) to obtain the items you want to use.

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

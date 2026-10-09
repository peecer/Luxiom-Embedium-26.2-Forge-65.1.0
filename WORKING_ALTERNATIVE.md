# Minecraft 26.2 / Forge 65.1.0 — real graphics alternative (NOT a Luxium port)

## Why the old JAR failed

The `UNIMPLEMENTED-luxiom-embedium-...jar` compiled in this repository is **only empty Forge entrypoint classes**. It contains **zero** Embeddium rendering acceleration, zero Luxium shaders, and zero new effects. **REMOVE IT from your mods folder.** It does not translate or port anything.

The official [Luxium project](https://www.curseforge.com/minecraft/mc-mods/luxium) offers only Minecraft 1.20.1 / Forge builds. The original Embeddium releases [do not target 26.2 Forge](https://modrinth.com/mod/embeddium). Do not mix 1.20.1 Java code or Fabric Sodium JARs into Forge 26.2.

## Actually available option: community Oculus port

For **Minecraft 26.2, Forge 65.1.0, Java 25**, there is a [separate Oculus Community Port beta](https://www.curseforge.com/minecraft/mc-mods/oculus-community-port/files/8661452) named `oculus-forge-26.2-0.3.0-beta.1.jar`.

It implements part of modern shader-pack loading and has been tested with compatible BSL and Complementary final passes. **It is a beta and does not reproduce the complete Luxium renderer or all effects.**

1. Make a NEW Forge 26.2 instance with Forge 65.1.0 and Java 25.
2. Remove the old `UNIMPLEMENTED` combined placeholder JAR and any Sodium/Fabric/old Embeddium/Luxium JARs.
3. Download the **26.2** file from the official Oculus Community Port project above. Use the production mod JAR, not `-sources.jar`.
4. Place it in the client instance's `mods` folder and launch the game.
5. Add a compatible shader pack to `shaderpacks` and configure it through the mod.
6. Add an optional [Dynamic Lights mod/datapack](https://modrinth.com/mod/dynamic-torches) only if its release explicitly lists Forge 26.2.

These are **independent alternatives** and not a port or replacement for Embeddium's full performance optimizations.

## Need an actual Luxium port?

It requires editable original Luxium source/assets, porting the shader and lighting systems to Minecraft 26.2 Forge APIs, replacing old Embeddium integrations, and a client rendering test matrix. The existing binary JARs and Gradle bootstraps are not enough to produce that port.

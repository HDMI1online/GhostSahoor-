# GhostSahoor -and yes, you can hyjack people on cracked servers

> ⚠️ **Legal / ethical notice — read first**
>
> GhostSahoor includes features that impersonate another player's identity on a
> server (see **Account Hijacking / `GetThisPlayer`** below), plus a full cheat
> module set (combat assist, movement exploits, ESP, etc.).
>
> **Only use this on servers you own or administrate, or where every player has
> explicitly agreed to it (e.g. a private friends' mod competition where
> cheating is the agreed-upon ruleset).** Do not use it against players who
> have not consented, and do not use it on a server you don't control. This
> project is published **for educational purposes** — to study Fabric
> modding, Minecraft network internals, anticheat detection techniques, and
> binary-integrity verification. The author takes no responsibility for use
> on servers or against people without authorization; that use may violate a
> server's terms of service and, depending on where you live, the law.
>
> By building or running this client you accept that condition.

---

## What this is

GhostSahoor is a Fabric client mod (Kotlin, Minecraft 1.21.11, Mojang
mappings) built for a private, invite-only mod competition among friends on
their own Paper server, where every participant builds their own client and
cheat modules are the agreed house rules. It is **not** intended for public
servers or for use against unconsenting players.

## Modules — what's in the client and how to use it

**Opening the menu:** default key is **Right Shift** (configurable in the
Client tab). The menu shows pill tabs for each category down the side;
click a tab, then click a module's name to toggle it on/off, or click to
expand it and see its settings (keybind, sliders, toggles, mode pickers).
Almost every module can be bound to its own key independently of the menu.
HUD elements (anything in the HUD tab) are repositioned with the mouse via
the **Anordnen** ("Arrange") module, which opens a drag-and-drop editor.

**Detection rating** (the colored dot next to each module): this is a
rough **anticheat-detectability** estimate (Grim/Vulcan/NCP-style — how
likely a serverside anticheat is to flag it), not a measure of fairness or
how obvious it looks to other players. From safest to most obvious:
🟢 **Undetected** → 🟡 **Selten erkannt** (rarely flagged) → 🟠 **Riskant**
(risky) → 🟠 **Oft erkannt** (often flagged) → 🔴 **Sofort erkannt**
(flagged immediately). Module descriptions below are the exact text shown
in-game (German, like the rest of the client UI).

Settings/configs are saved per server (see the **Configs** module) in the
client's local config folder, independent of this README.

### Client (Einstellungen)

| Module | Detection | What it does |
|---|---|---|
| Menü | — | Opens this menu (default key: Right Shift) |
| Configs | 🟢 | Save/load configs, separate config per server |
| Design | 🟢 | Change the client's colors and look |
| Freunde | 🟢 | Mouse-wheel-click a player = friend (never attacked by combat modules) |
| Panik-Taste | 🟢 | Instantly disables every module (default key: End) |

### Combat (Kampf)

| Module | Detection | What it does |
|---|---|---|
| AimAssist | 🟡 | Pulls the mouse slightly toward the enemy |
| AntiBot | 🟢 | Ignores fake players spawned by anticheats |
| AutoAnchor | 🟢 | Charges and ignites the respawn anchor you just placed yourself |
| AutoClicker | 🟡 | Auto-clicks while the mouse button is held |
| AutoCrystal | 🟢 | Places and detonates end crystals automatically where your crosshair points |
| AutoWeapon | 🟢 | Switches to your best weapon when looking at an enemy |
| BedAura | 🟢 | Hold a key + look at a bed: breaks it |
| ClickAura | 🟡 | Click hits the best target (Legit: turns to face it · Unlegit: instant, 360°) |
| Criticals | 🟡 | Every hit is a critical (jump-based or packet-based) |
| Hitboxes | 🟠 | Enlarges enemy hitboxes |
| KillAura | 🔴 | Attacks everything in range |
| MaceSwap | 🟡 | Mace one-hit: a fall-hit routes itself through the mace |
| NoMiss | 🟢 | Discards clicks that would hit nothing (keeps attack charge) |
| Reach | 🟠 | Extends melee range |
| ShieldBreaker | 🟡 | Breaks enemy shields automatically with an axe, then switches back to sword |
| Surround | 🟡 | Obsidian around your feet (crystal protection) |
| TotemPops | 🟢 | Alerts you when an enemy pops a totem |
| TriggerBot | 🟡 | Attacks automatically when your crosshair is on an enemy |
| Velocity | 🟡 | Less knockback (jump-reset or reduce) |
| WTap | 🟢 | More knockback via sprint-reset on every hit |

### Player (Spieler)

| Module | Detection | What it does |
|---|---|---|
| Rüstungs-Warnung | 🟢 | Warns when armor is close to breaking |
| AutoArmor | 🟢 | Auto-equips your best armor |
| AutoCraft | 🟢 | Repeatedly crafts planks/sticks/torches/crafting table from your inventory |
| AutoEat | 🟢 | Eats automatically when hungry |
| AutoGap | 🟢 | Eats a golden apple at low health |
| AutoPearl | 🟢 | Throws an ender pearl before a fall would be fatal |
| AutoPot | 🟢 | Throws healing potions at low health |
| AutoRespawn | 🟢 | Respawns instantly |
| AutoRestock | 🟢 | Refills a hotbar slot from your inventory automatically |
| AutoTool | 🟢 | Switches to the best tool while mining |
| AutoTotem | 🟢 | Keeps a fresh totem in your offhand automatically |
| AutoXP | 🟢 | Throws XP bottles to repair Mending armor |
| ChestStealer | 🟡 | Empties chests almost instantly |
| Werkzeug-Warnung | 🟢 | Warns or switches before a tool/weapon breaks |
| ElytraSwap | 🟢 | Jumping mid-air = equips elytra, landing = equips chestplate |
| InvManager | 🟢 | Tidies your inventory, throws away junk |

### Movement (Bewegung)

| Module | Detection | What it does |
|---|---|---|
| AutoWalk | 🟢 | Walks forward automatically |
| Blink | 🟠 | Withholds your movement packets, then sends them all at once |
| ElytraFly | 🟢 | Elytra: auto-rockets (legit) or free flight |
| Fly | 🔴 | Flying in Survival, adjustable speed |
| Jesus | 🟢 | Walk on water |
| NoFall | 🟡 | No fall damage (water-bucket MLG or packet-based) |
| NoSlow | 🟠 | No slowdown while eating/blocking |
| Parkour | 🟢 | Jumps ledges automatically |
| SafeWalk | 🟢 | Never walk off an edge |
| Speed | 🟢 | Faster walking (Legit: sprint-bunnyhop) |
| Spider | 🔴 | Climb walls |
| Sprint | 🟢 | Always sprinting |
| Step | 🟢 | Step up full blocks |
| Timer | 🔴 | Speeds up the entire game |
| WindJump | 🟡 | Key press = throws a wind charge at your feet (real vanilla self-launch, no fall-damage risk) |

### Render

| Module | Detection | What it does |
|---|---|---|
| BaseFinder | 🟢 | Finds bases (chest clusters + built-up area around them) and marks them |
| Block ESP | 🟢 | See chosen blocks through walls |
| CameraClip | 🟢 | 3rd-person camera isn't pulled in by walls, adjustable distance |
| Freecam | 🟢 | Move the camera freely while your player stays put |
| Freelook | 🟢 | Hold a key = look around freely, movement direction unaffected |
| Fullbright | 🟢 | Everything bright, even in caves |
| Glow ESP | 🟢 | Glowing outline around players, through walls |
| Hitmarker | 🟢 | Crosshair flash + sound on every hit |
| Hole ESP | 🟢 | Shows safe bedrock/obsidian holes |
| LogoutSpots | 🟢 | Shows where players logged out |
| NameProtect | 🟢 | Hides real player names above their heads (for streaming) |
| Nametags | 🟢 | Names with health & armor above every player |
| NoRender | 🟢 | Hide fire, pumpkin overlay, totem animation, weather |
| PlayerAlert | 🟢 | Alerts you when a player comes into view |
| Player ESP | 🟢 | See players through walls (boxes + lines) |
| Storage ESP | 🟢 | See chests & shulkers through walls |
| Todespunkt | 🟢 | Shows where you last died |
| Tracers | 🟢 | Lines to mobs & items |
| Trajectories | 🟢 | Flight path of arrows, pearls & potions |
| X-Ray | 🟢 | Only ores stay visible |
| Zoom | 🟢 | Zoom in like OptiFine (hold the zoom key) |

### HUD

| Module | Detection | What it does |
|---|---|---|
| Anordnen | — | Drag HUD elements around with the mouse |
| Armor HUD | — | Armor + durability shown on screen |
| Effekt-HUD | — | Active effects with icon + time remaining, chime when one's about to expire |
| Info HUD | — | Coordinates, facing, FPS, ping, speed |
| Item-Zähler | — | Totems, golden apples, pearls, XP … at a glance |
| Modul-Liste | — | Shows which modules are currently active |
| Spectator-Liste | — | Permanently shows who's in spectator mode (like the tab list) |
| Target HUD | — | Info about your current combat target |

### World (Welt)

| Module | Detection | What it does |
|---|---|---|
| AutoBridge | 🟢 | Hold a key = bridges automatically backward (sneaks + places at the right moment) |
| AutoFarm | 🟡 | Harvests mature crops and replants them |
| AutoFish | 🟡 | Fishes automatically |
| AutoMine | 🟡 | Mines automatically wherever you're looking |
| FastPlace | 🟡 | No block-placement cooldown |
| Nuker | 🟠 | Breaks everything around you (Legit: requires looking at it) |
| Scaffold | 🟠 | Places blocks under you automatically |
| Tower | 🟠 | Hold a key = pillars up automatically |

### Misc (Sonstiges)

| Module | Detection | What it does |
|---|---|---|
| AC-Erkennung | 🟢 | Passively detects which anticheat the server is running |
| AutoAuth | 🟢 | Auto-registers/logs in with AuthMe & similar login plugins |
| AutoLog | 🟢 | Disconnects at low health if you have no totem |
| AutoReconnect | 🟢 | Reconnects automatically after being kicked |
| Chat-Logger | 🟢 | Saves chat, joins/leaves, gamemode changes and kicks (searchable) |
| FakePlayer | 🟢 | A test enemy only visible to you |
| GetThisPlayer | 🟢 | Account Hijacking — see its own section above |
| Packet-Logger | 🟢 | Records every packet (live view, searchable, saved to file) |
| Watchdog | 🟢 | Disables risky modules while a flagged player is nearby |

### Operator (only with OP access on the server)

| Module | Detection | What it does |
|---|---|---|
| Operator Tools | 🟢 | One click: fully-enchanted armor, weapons and tools (requires OP) |
| Operator Cheats | 🟢 | Other OP-only convenience cheats (requires OP) |

## Account Hijacking (`GetThisPlayer`)

On a **cracked/offline-mode server**, the server treats a player's chosen
*name* as their identity — there is no Mojang/Microsoft account check. This
module lets the client disconnect, swap its local username (and the
matching offline UUID) to someone else's name, and reconnect — the server
then treats you as that player: same inventory, same permissions, same
"home", etc.

This **only works if**:
- the target server is in offline/cracked mode (this does nothing on a
  server that verifies Mojang/Microsoft accounts), and
- it is not blocked by the server's own protections (whitelist, a
  login-password plugin, IP binding, etc.).

If the real player is online at the same moment, most servers will reject
the second connection ("already online") or kick whichever session was
already connected — this client no longer blocks you from *trying*, but the
server decides whether the join succeeds.

**Again: only do this on your own server, or one where it's an explicitly
agreed rule among all players. On any other server this is impersonation
and can get the real account banned, locked out, or griefed — treat it the
same as you would treat gaining access to someone else's house key.**

## Building

Requires Java 25 to run Gradle/Loom (code compiles for Java 21).

```bash
./gradlew build
```

The dev jar lands in `build/libs/`. Running `./gradlew runClient` launches a
local test instance.

## Integrity / tamper protection

This is the mitigation against the client being handed out "infected" —
i.e. someone taking a built jar, patching malicious bytecode into it, and
redistributing it as if it were still the original:

- `release/signing-key.der` is a private Ed25519 key that **never leaves
  this machine** and is **never committed** (see `.gitignore`).
- `./gradlew signRelease` signs the built jar: it hashes every entry in the
  jar (sorted, content + name) and embeds the signature as `sahoor.sig`.
- At runtime, `Integrity.kt` recomputes that hash from the running jar and
  verifies it against the embedded signature using the matching public key
  (hardcoded in the client). Three possible outcomes:
  - **DEV** — unsigned/loose classes (e.g. running straight from source via
    Gradle). No warning; this is the normal way to build and test your own
    changes.
  - **OFFICIAL** — signature matches exactly. The jar is byte-for-byte what
    was produced by `signRelease` on the key holder's machine.
  - **TAMPERED** — a signed jar whose contents no longer match its
    signature (someone modified it after signing). The client shows an
    unmissable in-game banner and chat warning on startup, so nobody can
    quietly pass around a backdoored build while claiming it's the official
    release.

What this **does** protect against: taking an officially-signed release
jar, injecting code (a RAT, a stealer, anything) into its bytecode or
resources, and redistributing it as "the real thing" — the signature check
fails and the client visibly flags it as tampered.

What this **cannot** protect against, because no purely client-side check
can:
- Someone building their own malicious client from (modified) source and
  signing it with their *own* key pair — the warning only means "not signed
  by this project's key," it can't vouch for a key it doesn't know about.
  Only download/build from this repository or a source you trust.
- Someone removing the `Integrity` check from the source entirely and
  rebuilding — again, trust the source, not just the binary.
- Supply-chain risk in dependencies (Fabric Loader, Fabric API, Kotlin
  stdlib, etc.) — this project pins versions in `gradle.properties` and
  does not fetch anything at runtime, but a compromised upstream artifact
  is outside what any mod-level check can catch.

**Practical rule of thumb:** only ever run a jar you built yourself from
this source, or one you got directly from someone you already trust whose
public key you've verified. Never run a "GhostSahoor" jar someone sends you
unsolicited, even if it shows no tamper warning — a build signed with an
unfamiliar key, or an unsigned dev build, shows no warning either and
proves nothing about its contents.

## Known data stored locally

- `AutoAuth` stores `/login` passwords for cracked servers in plaintext in
  the client's local config folder, for autofill convenience only. Nothing
  is ever sent off this machine — there is no network client code in this
  project outside the Minecraft game connection itself.
- Chat logs, identity/player history, and keybinds are stored locally the
  same way any Fabric client mod stores config.

## License

All rights reserved (see `fabric.mod.json`). Source is shared here for
transparency and for the private competition this was built for — see the
notice at the top of this file for the terms of use.

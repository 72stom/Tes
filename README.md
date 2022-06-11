```# Language file you want to use
Language: EN
Economy:
  # Enable or disable CMI economy in general
  # In case CMIInjector is present, then this will be set to true automatically.
  # Attention! For economy to work properly with other plugins you will need ether an injector or recompiled Vault version. 
  # You can find both option at top of plugins page
  # ATTENTION! If you disabled CMI economy while server was running, you will need to perform full server restart for this to take correct effect and avoid any issues while getting players balances
  Enabled: false
  # Determines if player needs to confirm money payment by clicking on chat message
  Confirmation: false
  # Set to true if you want to log money transfers between players
  LogEnabled: false
  log:
    Unknown: true
    Transfer: true
  Cheque:
    # Determines max amount of cheque player can create
    # Set it to 0 to remove limit
    MaxValue: 1.0E8
    # If set to true player will be required to hold peace of paper to create cheque
    Paper: true
    # When set to true player will be required to have cmi.command.cheque.withdraw permission node to withdraw cheque
    Permission: false
  PaymentWithShorts:
    # When set to true players will be able to make payments by using short amount formats like 10k which results into 10000 and similar
    # In addition 10.2k will result into 10200
    Allow: true
    # List of suffixes we should accept and into what amount it results into
    # Only one letter is acceptable when defining suffix
    values:
    - k-1000
    - m-1000000
    - b-1000000000
    - t-1000000000000
    - q-1000000000000000
  BalTop:
    # List of players to exclude from baltop list
    Exclude:
    - Notch
    # When enabled baltop list will show short money values, like 12.5M instead of 12501234
    DisplayWithShorts: false
    # List of names to exclude from baltop
    # Can be used to filter out towny towns
    ExcludeStartingWith:
    - town_
    - town-
    - towny_
    - towny-
    - debt-
    - debt_
    # When set to true some fake accounts will be included into baltop list
    # This should include some previously marked accounts as fake which have been created for town usage or similar things
    IncludeFakes: false
    # Set to 0 or lower to disable this feature
    # Time in days of player being offline to exclude from being included in balance top list
    ExcludeInactive: 0
  Global:
    # Starting amount of money players will have
    StartingAmount: 100.0
    # Minimal amount, can go into negative if needed
    MinimalAmount: 0.0
    # Maximal amount of money player can have. Set to -1 to disable this limit
    MaximumAmount: 1.0E8
    # Defines amount until player can send to another player
    # This can prevent annoying spam some players would want to create by sending tiny amounts of money
    MinimalPay: 0.5
    # Defines if you want to allow payments with fractions
    # if this is disabled then payments will be limited to whole numbers and in case player provides number with fraction we will round number down
    Fractions: true
    # Currency symbol to be used when showing balance or similar
    CurrencySymbol: €
    # Format used for displaying money
    MoneyFormat: '###,##0.00'
    # Converts long numbers to short ones, like 12305122 to 12.3m
    UseShortNumbers: false
    # Suffixes for short numbers
    ShortNumbersSuffixes:
    - ''
    - k-1000
    - m-1000000
    - b-1000000000
    - t-1000000000000
    - q-1000000000000000
    # Replaces to western format where decimals are separated by , and thousands by . In example 1,000,000.00 changes to 1.000.000,00
    SwitchPlaces: false
    # Placing of currency symbol
    Placing: '[money][symbol]'
FileSave:
  # Change this to true only if you have issues with drives I/O and you need to save players files in async mode to lower waiting time for mc server
  Async: false
InteractiveCommands:
  # Regex used in recognizing public interactive commands used in signs
  # Default format is [ic:[icName]] in example [ic:trash]
  # If you want clean format use regex like: (\[([a-zA-Z0-9]+)\])
  SignRegex: (\[ic:([a-zA-Z0-9]+)\])
  # Sorting of IC list ether by distance from you or alphabetically
  SortByDistance: true
Optimizations:
  # When disabled we wont try to deop fake operator on server starup or unload while at same time disabling asFakeOp! specialized command usage
  UseFakeOperator: true
  # When this set to true any message sent to console will be strip out of any colors
  # In case you have mohochrome console, keep this at true
  MonochromeConsole: false
  # Time in seconds we want to give for playes who joins server a immortality state
  # Set this to 0 to disable
  # Max 60 seconds
  ImmortalityOnJoin: 3
  # Enables or disables maintenance mode
  Maintenance: false
  # Automatically kicks everyone from server when enabling maintenance mode who doesnt have cmi.command.maintenance.bypass permission node
  MaintenanceAutoKick: true
  # When enabled will show bossbar message informing about current maintenance mode being enabled
  MaintenanceBossBar: true
  # When this is set to true features like glow color, player collision, name plates will stop working and CMI will avoid doing anything related to player teams
  # Enable this if you are experiencing issue with other plugins which utilizes players teams for certain features
  DisableTeamManagement: false
  ArmorStands:
    # When set to true, plugin will check if player can manipulate armor stand by sending fake block place event and checking if any plugin would want to prevent this action
    # This can help out to minimize posibility for players to manipulate armor stands when they dont have build permission in area where armorstand is standing
    CheckBlockPlace: false
    Templates:
      # When set to true player will be required to have cmi.command.armorstand.template.[templatename] permission node to deploy saved template
      SpecificPermission: false
  AutoDownload:
    # In case you dont have GeoIP.dat it will be downloaded automatically on server start. Restart can be needed for it to take effect
    GeoIp: false
    # In case you dont have GeoLiteCity.dat it will be downloaded automatically on server start. Restart can be needed for it to take effect
    GeoLiteCity: false
  # When enabled you will see skull owner name in action bar when right clicking it
  ShowSkullOwner: true
  # When enabled you will see beeHive information in action bar when right clicking it
  ShowBeeHiveInformation: true
  # Sets indicator when creating elevator signs. Its case insensitive
  ElevatorIndicator: '[CMIElevator]'
  SignEdit:
    # Defines sign top line by which player will not be able to edit sign with /cmi se command
    BlackList:
    - '[Private]'
    - '[More Users]'
    - '[Everyone]'
    - '[AdminShop]'
    - '[ChestShop]'
    - '[CMIElevator]'
  # Defines elevator type. If this is used on second line of sing, then player will be teleported directly in front of it instead of keeping original players x and z coordinates
  ElevatorStaticIndicator: '[*]'
  # Used to show date in places like mail, checkban, infopage and similar locations
  LongDateFormat2: dd/MM/yy HH:mm:ss
  # Used to show date in places like inv gui and similar locations
  ShortDateFormat: dd/MM/yy
  # Do you want to record sell hand actions into file
  SellLog: true
  # When set to true players with same name but different capitalization will be denyied from joining server to avoid possible issues. In example if on first day player Zrips joined server and on second day player zRips tries to join server, he will be rejected
  # RECOMMENDED to keep this at true
  PreventDifferentCapitalizationNames: false
  # When this set to true by using any command, requiring players name, in case plugin cant determine player by given full name, then partial matches from online players will be used. In example: /cmi heal rips can heal player Zrips 
  # Useful when you have players with complicated names
  PartialPlayerName: false
  # If you want to prioritize online players when using partial player name enable this setting
  # Don't forget to enable PartialPlayerName for this to have full effect
  # Keep in mind that this might block you from accessing offline player with same partial name as some one currently being online
  # For example offline Luuk might no longer be accessible while Luuk666 is online
  # This can be overridden by adding -exa- suffix for a name, so luuk-exa- will return offline player object
  PrioritizeOnlinePlayers: false
  # When set to true, commands in help page will be sorted alphabeticaly
  # If set to false, commands will be sorted by priority
  CommandSorting: true
  # Percentage value (1-100) to pick best command match if command cant be found
  # Example: /cmi spawnmb will have 87.5% match with /cmi spawnmob
  # Set to 0 to disable
  SimilarCommandChecker: 75
  # When set to true, if player enters incorrect command, then command will not gonna be performed
  # But message informing about incorrect usage and best match will be shown in any case
  SimilarCommandPrevention: false
  # When set to true, commands in help page starting with /cmi will get shortened by hiding base command. Example /cmi back becomes /back
  # Keep in mind that this is automatic feature if alias or custom alias is set to that command
  # And keep in mind that this is only cosmetic change and will not impact command usage
  RemoveLabel: false
  # When set to true, all players can see missing permission node by hovering over error message
  # When set to false only players with cmi.permisiononerror permission node can see missing permission node
  # Keep in mind that by default players have acces to permission node, so negate it if you want to hide missing permission nodes from them
  PermisionOnError: true
  # When set to true, each time player tries to use something he doesnthave permission, message will be shown in console
  PermisionInConsole: true
  Teleport:
    # Players need to have cmi.safeteleport permision node to be placed in a safe location when teleporting to target location
    # When true then while checking for safe location, we will try to determin it going down and if it fails, then up from target location
    # When set to false, then first of all location above target location will be checked, then down
    SafeLocationDownThenUp: false
    # Time in seconds player should be invulnerable after teleporting
    # This will prevent player who teleported to damage others for defined time
    # Set this to 0 if you want to disable it
    # Max 60 seconds
    Invulnerability: 5
    # When this set to true each time player teleports to any destination he will be teleported to spawn point
    # This is to prevent from people knowing to which direction you have teleported too
    # As everyone noticed, teleportation doesnt actually teleport you, but moves to targetdestination in short time
    ToSpawnBefore: false
    # Set to true if you want to use tp commands as /cmi tp [WhoYouWantToTeleport] [WhereToTeleport] when its false, its /cmi tp [whereToTeleport] [WhoYouWantToTeleport]
    SwitchPlaces: true
    CurrentLoc:
      # Applies for tpa, tpahere and tpaall only
      # If set to true then player will be teleported to current player position after accepting teleport request
      # If set to false then player will be teleported to player at which teleport request was issued
      tpa: true
      # Applies for tpahere only
      tpahere: true
    # Default distance for jump command. Can be overriden with cmi.command.jump.[amount] permission node
    JumpDefault: 50
    # Defines time in seconds for accepting tpa or tpahere requests
    TpaTime: 60
    # Defines time in seconds for player being teleported after tpa or tpahere is being accepted
    TpaWarmup: 3
    # Defines if player can move when tpa or tpahere is being accepted
    TpaMove: false
    # Defines time in seconds for blocking player teleport offers after denying their request
    TpaBlock: 120
    # Defines time in seconds for bypassing prevented teleportation to unsafe location
    TpBypass: 15
    # When set to true adds accept and deny buttons when sending tpa or tpahere requests
    DenyConfirm: true
    BlackListedItems:
      # Option to prevent player teleportation when he has blacklisted items in his inventory. Can be bypassed with cmi.teleport.bypassblacklist
      Enabled: false
      EnabledFor:
        tp: true
        tpa: true
        tpahere: true
        warp: true
        home: true
        spawn: true
      # Item and amount (if not defined, defaults to 0) we want to protect
      # Separate amount with : in example IronOre:5 what will limit ironOre block in players inventory up to 5, more than that and player cant teleport
      List:
      - Diamond
      - DiamondBlock
      - DiamondOre
      - ironore:5
    # Back location will not be triggered if player teleports closer than defined amount of blocks
    BackMinDistance: 5
    # When set to false we will not include teleport location when teleporting around with worldedit compass
    # When set to true we will include each teleport action, even if you simply jumped around with compass
    BackWithWE: true
    # List of worlds to whichones player can't go back with /back command
    BackBlackList:
    - TeztWorldz
  Hat:
    # When enabled we will not allow to place items into head slot if item has custom lore
    IgnoreLored: false
    # When enable we wont allow to equip items which are not hat type and has enchantment on it
    # This will prevent from players having enchantment effects in head slots which should not be present there
    BlockArmorItems: true
  helpop:
    # When set to true player will not see his sent message to helpop, but rather predefined message informing that his question have been sent to online staff
    feedbackMessage: true
  IP:
    # When set to true, players ip will be recorded for future use, like recognizing players other accounts
    # Some commands will have limited usage when this is disabled
    Record: true
    # How long in second to wait until players ip is being recorded into data base
    # This only applies for offline servers to allow for player first of all to login before recording ip
    # Try to keep this value lower than your login plugin's allowed login time
    delay: 30
  # Max amount of hp you can get when using /cmi maxhp command
  MaxHp: 200
  # When set to true, player play time will be grabbed from user stats file instead of from CMI user data file
  # This can help to get more accurate play time if you have older server and using players stats feature
  PlayTimeFromStats: true
  # Do you want to run auto top playtime updater
  # This is responsible for providing players current top playtimes which gets updated on consistent intervals, useful for placeholders
  PlayTimeAutoUpdater: true
  # When set to true, playtimetop list will be loaded on server startup
  PreloadTopPlaytime: false
  # Do you want to use CMI playtime tracking
  # While this is enabled, player play time will be record for each hour he playied in server
  # This doesnt have effect on rankup or /playtime commands, it will only show more specific playtime by hours when using /cplaytime command
  CMIPlayTimeTracking: false
  # Player names to be excluded from playtimetop list
  PlaytimeTopExclude:
  - Some
  - Names
  - Here
  ItemName:
    # For black listed materials check ItemRenaming.list section

    # When set to true items which name got changed with /itemname command will be marked with NBT data as 'ModifiedName' boolean type
    MarkChanged: false
  ItemLore:
    # List of materials to block from itemName command
    TypeBlackList:
    - gold_nugget
    # When set to true items which lore got changed with itemname command will be marked with NBT data as 'ModifiedLore' boolean type
    MarkChanged: false
  OnDurabilityLoss:
    # Do you want to inform player when item durability gets lower than set threshold
    # Player should have cmi.informDurability
    Tools:
      Use: true
      Percentage: 10
    Armor:
      Use: true
      Percentage: 10
  OnLimitedItemUse:
    # Informs about left uses of item
    Inform: true
  # Can disable messages outputed durring start for world chunk checks
  DisableWorldChunkCheckInfo: false
  # Can prevent animals or monsters entering boats
  PreventEntityBoatEnter:
    Monsters: false
    Animals: false
    Villagers: false
  PreventBedExplosion:
    Nether: false
    TheEnd: false
  # Will teleport players down from nether 'roof'
  PreventPlayersOnNetherRoof: false
  # Will teleport players up from beneeth betrock if they are flying or gliding with elytra over there
  PreventPlayersBelowBedrock: false
  PreventIronGolem:
    # When set to true, iron golems will not drop roses on death
    Roses: false
  # When set to true, fishing rod will not move grabbed entity towards you
  PreventHook: false
  Commands:
    # When set to true player will see full list of posible commands when performing /cmi command without defining specific command
    # When set to false we will return 'No command found' feedback message
    ShowMainHelpPage: true
    Near:
      # Use approximate distances instead of exact
      # This will use separate locale line which includes direction to the player
      # So instead of having something like 123m you will have ~100m
      Approximate: true
      DefaultDistance: 200
      Invisibility:
        # When enabled we will not show players who has invisibility potion effect on them in the list
        Hide: false
        # Only applies when previous Hide option is enabled
        # Will obfuscate players name but stil shows his location in the list
        # Actual players name wont be used, instead generic 8 character name with &k color format gets used to prevent from people realizing who is near by the lenght of his name
        Obfuscate: false
      # When enabled, players can click on each player name and simple /cmi point [location] will be performed which shows particles directing towards target player
      PointTo: true
      # How many lines you want to show when using /near command
      Count: 10
    Inv:
      # List of players which you should not be able to open inventories
      # This can still be bypassed if you are OP
      BlackList:
      - Zrips
    Clear:
      # When set to true, /cmi clear comamnd will require confirmation for it to be finalized
      Confirmation: true
      # List of NBT paths we should check before removing item from inventory. Each line should start with NBT: this is for the future updates which will involve aditional optional checks
      Exclude:
      - NBT:ItemJoin Name
      - NBT:ItemJoin.Name
    List:
      # Sorts players custom groups in Ascending or descending order
      ASCOrder: true
  Multicraft:
    # When set to true, will prevent multicraft servers to spam in console.
    DisableList: false
PlaytimeRewards:
  # Enable or disable playtime rewards.
  # This is required if you want to have auto rewards
  Enabled: false
  # When enabled, while player is in afk mode, repeatable playtime rewards will not increase in playtime
  # ATTENTION! this setting will not have any effect if you have Afk.StopPlayTime set to true
  # When StopPlayTime set to true, afk will be expluded automatically
  ExcludeAfk: false
  # Defines time in minutes to inform player about pending reward which needs to be claimed
  RewardInform: 15
  # Defines how many one time rewards you want to show in list
  # This will show next X amount rewards from your current playtime
  # No point in listing all rewards if player is still far away
  OneTimeAmount: 2
  # When set to true player will be required to have cmi.prewards.[name] permission node to get particular playtime reward
  RequiresPermission: false
Sleeping:
  Speedup:
    # When set to true, players can speedup night by sleeping in bed
    # This will allow to speed up night in percentage depending how many players are sleeping in beds in that world
    Enabled: true
    # List of worlds where this should be applied.
    # Keep in mind that time speed up only works on a normal type world and by default you will have only one
    # Set this list to [] if you want to include all possible worlds
    Worlds: []
    # When this set to true time will be speed up only between 13000 and 24000 ticks of the day
    # When having this set to false players can speed up day durring storms or other events
    OnlyDurringNight: true
    # Type of speedup information, can be: none, title, bossbar
    InfoType: title
    # When set to true, players who are in afk mode will be excluded from speed calculations
    ExcludeAfk: true
    # Defines speed to go throw night, bigger numbers will make it go faster and less players you will need to go throw night
    # 100 will result in 100 times faster time
    BaseSpeed: 100
    # Defines minimal speed to go throw night, this is in case there are more players than base speed and calculation return default speed
    MinSpeed: 5
    # Minimal amount of players sleeping in beds before speeding it up
    # Can be defined in 2 formats. When using clean number like 3, then 3 players will have to be sleeping before speedup kicks in
    # If amount is defined with % like 50% then half of server population will have to be sleeping before speedup kicks in
    MinBeforeSpeeding: 50%
    # When set to true online players will be informed about missing sleeping people count
    Inform: true
    # Time in seconds between information messages can be shown when player starts or stops sleeping
    InformDelay: 30
Compass:
  # Enable EXPERIMENTAL boss bar compass
  # Only for 1.9+ servers
  BossBar: false
  # Requires to hold compass in had to see it
  RequireCompass: false
  # Compass update interval in milliseconds
  UpdateInterval: 200
  # Keep same spacing between each direction. Length can be any you want
  Shape: '------------SW-------------W-------------NW-------------N-------------NE-------------E-------------SE-------------S-'
  Color: '&7'
  ShowHome: true
  Home: ۩
  ShowSpawn: true
  Spawn: ⤋
  ShowDeath: true
  Death: ☠
  ShowCompassTarget: true
  CompassTarget: ꖴ
ExploitPatcher:
  # When enabled this will prevent exp bootles being destroyed on portal edge and duplicating them in result of that
  PreventExpPortals: true
  # When enabled this will prevent players from performing commands which could lead to some bugs
  # By default its disabled to keep vanilla behavior, but is recommended to enable it to avoid issues
  NoCommandsInBed: false
  # Due to major exploit relating to oversized books this is recomended to be enabled
  # While this is set to true players will be limited in how many pages they can create
  # Limitation is determined by cmi.book.pages.§f[20to100]§6 permission node and by default players can create 20 pages
  LimitBooks: true
Vault:
  # If your having issues with vault grabbing correct players' group or balance, consider to turn this to false
  Money: true
  Group: true
Worth:
  # Defines lore that will prevent an item from being sold using /cmi sell.
  # Color codes and capitalization are being ignored
  BadLore:
  - Creative item by Gasha
  # If enabled any item with custom name will not be allowed to be sold with /cmi sell command
  CustomNameBlocking: false
  # If enabled any item with custom lore will not be allowed to be sold with /cmi sell command
  LoreBlocking: false
  # When enabled we will not allow to sell items which are not fully repaired
  RequireFullDurability: false
  # When enabled items which doesnt have full durability will be worth less. 30% left durability will result in items worth going down by 70%
  # This only works while RequireFullDurability is disabled
  DevalueByDurability: false
  AutoGenerate:
    # Value in percentages in how much more we should add to end product while auto calculating items price based on its ingredient worth
    # For examplem one stick is worth 0.1 and diamond 44 then end result as diamond_hoe will be worth 88.2 and with extra 2% this will be changed to 89.96
    # Value can be negative
    PriceIncrease: 0
BossBar:
  # Enables or disbales bossbar hp bar on 1.9+ servers
  # Only players with cmi.bossbar.hpbar permission node can see it
  # Permission node is been rechecked no more often than every minute for efficiency
  HpBarEnabled: true
  # List of mob types which will be excluded from hp boss bar
  HpBarBlackList:
  - Ender_dragon
Ban:
  # When set to true players who are banned will get messages modified by CMI instead of seeing vanilla type of message
  OverrideLoginMessage: false
ReSpawn:
  # Time in seconds to make player immortal after he respawns
  # Can be used to prevent respawn camping
  # Set to 0 if you want to disable it
  # Max 60 seconds
  Immortality: 3
  # If you want 3rd party plugin to handle player respawning, simply set this to false and reload plugin
  Enabled: true
  Global:
    # Defines respawn order if defined world is not present in Specific list
    # Possible respawn locations: anchor, bedLocation, spawn, homeLocation, worldSpawn, warp![warpName]
    # Spawn is preset spawnlocation with /cmi setspawn command, that location should have RespawnLocation set to true
    # bedLocation is location set by interacting with bed, BedInteraction should be set to false and players requires cmi.bedhome to set bed location
    # homeLocation is location set by player which is with default (Home) name, if that one doesnt exist then first in the list will be used if possible
    # worldSpawn is location preset to this world, this is not CMI location but default world spawn location
    # anchor is location defined by interacting with respawn anchor. This in general will only apply when you die in nether world, otherwise bed location is used
    # warp![warpName] can be any valid warp you set for players to be teleported, they will bypass any requirements for that warp
    PriorityOrder:
    - anchor
    - bedLocation
    - spawn
    - homeLocation
    - worldSpawn
  # Defines respawn order for defines worlds
  # Set respawn priority to [] or to random respawn criteria if you want to leave respawn handling for server or 3rd party plugin
  Specific:
    Spawn:
    - anchor
    - bedLocation
    - spawn
    - homeLocation
    - worldSpawn
Afk:
  # Enable or disable auto afk system entirely
  Enabled: false
  # When enabled shows title message informing that player is in afk mode
  TitleMessage: true
  # When enabled shows random subtitle message
  SubTitleMessage: true
  # Prevents jumping in one place to avoid afk status
  PreventJumping: true
  # Prevents damage while afk
  PreventDamage: true
  # Defines how often in seconds plugin will check for afk players state
  CheckInterval: 10
  # When set to true, players playtime counter stops
  # As of nature how this system works you can see +-1second jumping up and down while checking players playtime
  StopPlayTime: false
  # Defines how long to wait after player stops moving to set him as afk
  # Player needs to have cmi.command.afk.auto permission node
  # Set to 0 if you want to disable it
  AutoAfkIn: 300
  # Defines commands to be performed when player enters afk mode automatically while addling
  # Supports specialized commands
  AutoAfkCmds:
  - cmi broadcast !&6[playerDisplayName] &eis now AFK
  # Defines commands to be performed when player enters /cmi afk
  # Supports specialized commands
  ManualAfkCmds:
  - cmi broadcast !&6[playerDisplayName] &eis now AFK
  # Defines commands to be performed when player leaves afk mode
  AfkLeaveCmds:
  - cmi broadcast !&6[playerDisplayName] &eis no longer AFK
  # Defines how long to wait after player stops moving to kick player
  # This is additional timer to AutoAfkIn and in case player entered afk mode manually he will get kicked after AutoAfkIn+AutoKickIn seconds
  # This can be used not only to kick but to perform repeating action every x seconds if needed
  # Keep it at -1 to disable auto kick
  # Can be bypassed with cmi.command.afk.kickbypass permission node
  # Additionally players kick time can be changed with cmi.command.afk.kickOutIn.[seconds] permission node where bigger value takes priority
  AutoKickIn: -1
  # This will define how long to wait before performing kick commands again
  RepeatingAutoKickInterval: 300
  # When set to true, kick command will be repeated each RepeatingAutoKickInterval seconds
  RepeatKickCommand: false
  # Defines commands to be performed when player can be kicked
  # If player is not kicked then commands will be repeated every RepeatingAutoKickInterval seconds
  AutoKickCmds:
  - cmi kick [playerName] &eYou have been kicked for idling more than [time]
  # Defines worlds where players will not be placed into afk mode after they idled for defined time
  DisabledWorlds:
  - oneTestWorld
  - secondTestWorld
  # Disables afk on interaction
  DisableOnInteract: true
  # Prevents player from going bypassing afk mode while continuously holding one button with particular items or on particular blocks
  SmartInteractCheck: true
  # Prevents from players abusing afk by constantly moving in afk machine
  AntiAfkMachines: true
  # EXPERIMENTAL! Prevents players from being pushed around while player is in afk mode
  # Keep in mind that player can still be moved around the same block he is in
  PreventPushing: false
  # Disables afk on inventory click
  DisableOnInventoryClick: true
  # Disables afk on item drop
  DisableOnitemDrop: true
  # Disables afk on command usage
  DisableOnCommand: true
  # Disables afk on public chat message
  DisableOnPublicChat: true
  # Disables afk on private chat message
  DisableOnPrivateChat: true
  # Disables afk on move
  DisableOnMove: true
  # Disables afk on fishing
  DisableFishing: false
  # Disables item pickup while afk
  DisableItemPickup: false
  PreventMobSpawning:
    # When enabled we can prevent mob spawning near players who are afk
    Enabled: false
    # Prevents natural mob spawning
    # This can be more on heavy side of the server as it will try constantly to spawn in monsters near afk players
    Natural: false
    # Prevent mob spawning from spawners
    Spawners: true
    # Usually responsible for spawning in iron golems
    VillageDefence: true
  # Disables exp pickup while afk
  # Attention! Because of weird minecraft handling of exp orbs, best way is to set orb to 0exp and allow it to be obsorbed
  # So by enabling this exp obsorbed by afk players will have no effect
  DisableExpPickup: false
Holograms:
  # Defines in milliseconds how often to check if player entered holograms trigger area
  # Bigger numbers can help slightly lower server load
  # This is not essential to keep in low numbers
  CheckInterval: 2000
  Defaults:
    # Default value for hologram view range
    # This defines from how far holograms will appear for the player or when they will disapear
    viewRange: 16
    # Defines default update interval
    # Bigger this number is better performance we will have
    updateRange: 8
    updateInterval: 0.0
    # Defines default page change interval
    # When value is set to 0 or lower, pages will not be changed
    pageChangeInterval: 0.0
    # Posible values: down, up
    # Defines if we should place lines up from starting position or down
    placeUp: true
Votifier:
  # When set to true votifier votes will be counted for player
  CountVotes: true
  # Number of votes one IP can make in last 24 hours
  # Set it to 0 to have unlimited amount
  MaxVotesInADay: 0
  # Cooldown between votes from same service
  # In most cases voting service will have its own cooldown setup
  # But if you need extra one to prevent rapid voting you can define time in seconds over here
  GeneralCooldown: 0
  # When set to false, commands on sucessfull vote will not be performed
  PerformCommands: true
  # Defines commands to be performed when player votes
  # Supports specialized commands and placeholders
  # [serviceName] variable can be used to insert address
  CommandsOnVote:
  - cmi broadcast !&6[playerDisplayName] &evoted!
  - cmi give [playerName] diamond
  # Keep it at false if you dont want to give out extra rewards
  ExtraRewardsEnabled: false
  # Commands will be performed when player collect determined amount of votes
  ExtraRewards:
    '10':
    - cmi heal [playerName]
    - cmi money give [playerName] 100
    '100':
    - cmi heal [playerName]
    - cmi money give [playerName] 1000
    - cmi give [playerName] diamond 32
  # List of players to be excluded from top voter list
  ExcludeList:
  - None
Ranks:
  # If set to true we will check players rank by his access to rank by permission node and prioritize any rank which has more weight over current one
  # This means that in case player has access to third rank while recorded one is first one, we will prioritize third one
  # While this is active using command like /cmi setrank will set players rank to highest one he has access too, so as long as player has permission access to third rank you cant go lower than this, 
  # you will have to remove access to specific rank by removing permission node before trying to derank him
  PermissionCheck: false
  AutoRankUp:
    # Defines how often in seconds plugin will check for possible player rankups
    # Set it to 0 or less to disable auto rankup checks
    Delay: 60
    # EXPERIMENTAL. When set to true, player rankup checks will be done in async mode
    # In case of errors related to this feature being turned on, turn it off and report issue with error log to github
    Async: false
    # Defines how often in seconds each separate player will be checked for rankup
    # This is different than general check just to avoid couple players ranking up at same time
    # This also defines how often player will be notified about possible rankup and it will proportionaly increase with each time player get notification to avoid annoying spam in chat
    # Keep it longer or same as general delay time
    PlayerDelay: 120
    # Enable or disable progression bar in rank info window
    progressBar: true
  # When set to true, command /cmi ranklist will output ranks from your rankup path which will exclude any rank from different paths or different rankup trees all together
  # When set to false, all set ranks will be shown in the list
  ListSamePathOnly: false
  EffectUp: GColumn
  # When set to true requirements which involve time will be shown in short format like '50 hours' instead of '2 days 2 hours'
  OnlyHours: false
  # When OnlyHours set to true you can add minutes to the output message instead of showing fractions. So you can have '5 hours 30 minutes' instead of 5.5hours'
  includeMinutes: true
Signs:
  # Defines in milliseconds how often to check if player entered Dynamic Sign trigger area
  # Bigger numbers can help slightly lower server load
  # This is not essential to keep in low numbers
  CheckInterval: 3000
  # Defines list sign top lines which cant be edited with shift right click
  # Usually used for preventing shop sign modifications
  editBlackList:
  - '[Shop]'
Skins:
  # Applies skin to player automatically on his login to server if he doesnt have one already set
  # This will always set to skin by target player name
  AutoApply: false
  # Sets player sking to Steve when turning skin off and lets server to handle it
  # If its false, then skin will be changed to online one
  SteveOnOff: true
  # Requests from player specific permission for that skin cmi.command.skin.perm.[skinName]
  RequireSpecificPerm: false
  # Defines time in minutes how offten we want to update skin information from online Mojang servers
  # Keep in mind that your server can only send 1 request every minute, so keep it at a decent amount, hour or more
  # So if you have this set to 1 hour, then player skin information will be updated if player old skin information is older then 1 hour
  # This only triggers when player joins server or changes skin manually
  SkinUpdateTimer: 1320
  # Defines time in minutes how offten we want to send requests to Mojang servers
  # This is to limit amount of requests in specific time to avoid cluter with posible requests
  SkinRequestFrequency: 10
Alert:
  # Time in minutes for how long we want to keep set allert on player when performing /cmi alert command. Default is 24 hours
  Timer: 1440
Notes:
  # When enebled, when player logs in who has alert set on him, staff member will get notification that this player have some notes attached to him
  ShowOnAlertEvent: true
GroundClean:
  # List of item types not to be removed on ground clean action
  WhiteList:
  - itemType
Chat:
  # Will try to modify chat to display it in defined format
  ModifyChatFormat: false
  # When set to true, regular and private messages (excludes clean messages) will have additional information when hovering over it (PlaceHolderAPI supported) and can be clicked for quick reply option
  # To change default hover over messages seen on sent message, go to your locale file to Chat section
  ClickHoverMessages: false
  DiscordSRV:
    # Enables support for DiscordSRV plugin
    Enabled: true
    # Defines name of global chat channel in discordsrv
    GlobalChannel: global
    # Indicator which can be used as {discord} in chat format to indicate that message came from discord and not ingame
    Label: '&2[&7D&2]'
    UnlinkedLabel: '&4[&cD&4]'
  # Enables support for DynMap web chat
  DynMapChat: true
  # When set to false, each time you will use /r you will reply to person you previously sent message directly or to person who sent you message if there is none you have conversion before
  # When this set to true, players with /r will reply to person who last sent private message. This can result in confusion when using /r while getting private messages from multiple players
  ReplyToLastMessenger: false
  # If ReplyToLastMessenger is set to false, then timeOut will be taken into consideration to who you should reply
  # If you had conversation in last 120 seconds (default) then even receiving message from 3rd person, you will still reply to original player
  # If you had conversation in longer then 120 seconds period, then you will reply to latest person who send you a message
  LastMessengerTimeOut: 120
  # When set to true players will need to have cmi.command.msg.[groupname].send where [groupName] is receivers main permission group
  PrivateMessagesGroups: false
  # When set to false, web pge links in a chat will not get shortened to default [LINK] format
  TranslateLink: true
  # Defines regex when replacing url in chat with short word
  # Examples:
  # (https?:\/\/(?:www\.|(?!www))[a-zA-Z0-9][a-zA-Z0-9-]+[a-zA-Z0-9]\.[^\s]{2,}|www\.[a-zA-Z0-9][a-zA-Z0-9-]+[a-zA-Z0-9]\.[^\s]{2,}|https?:\/\/(?:www\.|(?!www))[a-zA-Z0-9]\.[^\s]{2,}|www\.[a-zA-Z0-9]\.[^\s]{2,})
  # ((http|https|ftp|ftps)\:\/\/)?[a-zA-Z0-9\-]+\.[a-zA-Z]{2,3}(\/\S*)?
  # ((http|https|ftp|ftps)\:\/\/)?[a-zA-Z0-9\-]+\.[a-zA-Z]{2,3}(\/\S*)?([^\s]+)
  LinkRegex: ((http|https|ftp|ftps)\:\/\/)?[a-zA-Z0-9\-]+\.[a-zA-Z]{2,3}(\/\S*)?([^\s|^\)]+)
  # When set to true, particular variables in chat will be translated into items player are holding. List of variables belove
  HoverItems: true
  # Defines regex when replacing item line in chat with players item in hand information. Only works when CMI hover over chat format is enabled
  ItemRegex:
  - (\%item\%)
  - (\[item\])
  - (\%i\%)
  # Attention! This will require you to have CMI Bungee plugin which can be found at zrips.net
  # Or direct download https://www.zrips.net/cmi/
  # Do you want to enable private messaging over bungeecord
  BungeeMessages: true
  # Do you want to enable public messaging over bungeecord
  # Player needs to have cmi.bungee.publicmessages.[servername] permission node to be able to send messages to target server
  BungeePublicMessages: true
  # Do you want to enable staff messaging over bungeecord
  BungeeStaffMessages: true
  # Used for simple chat messages. Optional variables: {displayName} {world} {prefix} {suffix} {group} {shout} {message}. Supporting PlaceHolderAPI variables like %player_server%

  # ATTENTION! Dont use gradient colors for {message} variable, if you want to apply gradient for it, utilize GeneralMessageFormat section
  GeneralFormat: '{prefix}&f{displayName}&7: &r{message}'
  # Will define message format itself, this allows to have gradients in messages
  # It NEEDS to contain {message} otherwise we will ignore this setup
  # For 1.16+ servers you can use color gradients like '{#b3a28f>}{message}{#d7b8e6<}'
  # You can have more than 2 colors in gradient. To define it repeat {message} variable. For example '{#b3a28f>}{message}{#5c6999<>}{message}{#d7b8e6<}'
  GeneralMessageFormat: '{message}'
  # Defines range of regular messages to travel
  # Set to -1 to disable range restriction
  GeneralRange: -1
  # Defines range of shout messages to travel
  # Shout messages should start with ! and player should have cmi.chat.shout permission
  # GeneralRange should be enabled
  # set to 0 to shout across all worlds, -1 to disable
  ShoutRange: 200
  # Defines cost for each shout message
  ShoutCost: 0
  # Prefix used to indicate that message should be sent to public chat instead of current players chat room
  # Set it to empty field if you want this feature to be disabled
  ChatRoomShout: '!'
  # Time in seconds you want to keep chat rooms alive before removing them
  # This only applies to empty rooms after last user leaves it
  ChatRoomLife: 3600
  # Defines suggested commands when you click on public, private and similar messages. [playerName], [playerDisplayName] and [playerNickName]  can be used to include players name
  ClickSuggestions:
    pubmsg: '/msg [playerNickName] '
    privmsg: '/msg [playerNickName] '
    staffmsg: '/msg [playerNickName] '
    helpop: '/msg [playerNickName] '
    chatroom: '/msg [playerNickName] '
    discord: '/msg [playerNickName] '
  # Use numeric increments to separate groups from each other. If player has more than one, then line with higher number will be used
  # Add as many lines as you need too
  # cmi.chatgroup.[id] permnission node to use
  # Permission example: cmi.chatgroup.2

  # ATTENTION! Dont use gradient colors for {message} variable, if you want to apply gradient for it, utilize GroupMessageFormat section
  GroupFormat:
    '1': '{prefix}&f{displayName}&f: &r{message}'
    '2': '{prefix}&f{displayName}&7: &r{message}'
    '3': '{prefix}&f{displayName}&8: &r{message}'
  # Use numeric increments to separate groups from each other. If player has more than one, then line with higher number will be used
  # Add as many lines as you need too
  # cmi.chatmessagegroup.[id] permnission node to use
  # Permission example: cmi.chatmessagegroup.2
  GroupMessageFormat:
    '1': '{message}'
    '2': '{message}'
    '3': '{message}'
  Colors:
    # If set to true then all public messages will be filtered from color codes and will allow to colorize them with appropriate permission node
    # cmi.colors.publicmessage.[colorName]
    # Colors: black(&0), darkblue(&1), darkgreen(&2), darkaqua(&3), darkred(&4), darkpurple(&5), gold(&6), gray(&7), darkgray(&8), blue(&9), green(&a), aqua(&b), red(&c), lightpurple(&d), yellow(&e), white(&f), magic(&k), bold(&l), strikethrough(&m), underline(&n), italic(&o), reset(&r)
    PublicMessage: true
    PrivateMessage: true
    # If set to true then /me messages will be filtered from color codes and will allow to colorize them with appropriate permission node
    # cmi.colors.me.[colorName]
    me: true
    # If set to true, then color codes will get removed from text instead of leaving them if player dont have appropriate permission node for that color
    CleanUp:
      publicmessage: true
      privatemessage: true
      me: true
      signs: false
      books: true
      # List of strings to ignore when checking chat for color codes player cant use.
      # This will bypass players colorcode restrictions and will allow usage of particular chat formats
      # Applies only for public and private messages
      WhiteList:
      - '&c❤&7'
    # If set to true then nickName will be filtered from color codes when player changes it
    # cmi.colors.nickname.[colorName]
    NickName: true
  # If set to true, players public message who is in your ignore list will not be shown
  IgnorePublicMessage: true
  Tag:
    # Enable or not tag system. This will inform player with his name mentioning in public chat if name have @ in front of it
    Enabled: true
    # When this is set to true, any player mentionings in public messages will be colorized and player will get informed as usual
    # This is allot more heavier on server than usual tagging with @, so enable if you know what you are doing
    HardCoreMode: false
    # Determines color of taged user name in chat with @ in front of name/nickname. Sender should have cmi.tag.color
    Color: '&c'
    # Commands to be performed when player is tagged
    # Variables like [playerName] will be replaced with tagged player name
    # You can use [senderName] to include player name who tagged
    CommandsOnTag:
    - asConsole! cmi sound BLOCK_NOTE_BLOCK_HARP:3:1 [playerName] -s
    # Will performd tag commands only when player is afk
    OnlyWhenAfk: false
    # When set to true, @ simbol will be removed
    RemoveEta: false
Command:
  CommandFilter:
    Duplicate:
      # When set to true, plugin will prevent spaming of same or similar command in short time range. Can be bypased with cmi.commandfilter.bypass permission
      Use: false
      # How much in percentage command is counted as same
      Percentage: 80
      # Defines how often in seconds you can send same/similar commands
      Interval: 5
      # How many commands you can repeat before stopped for cooldown
      MinAmount: 2
      # Whitelisted commands to ignore
      WhiteList:
      - msg
      - tell
      - login
      - register
  Spy:
    # Delay in seconds for commands spy to turn on after relog
    # This will prevent some one from loging in with admin account and seeing commands before loging in
    # Keep it at same or higher than your login plugin delay for entering password
    # This includes social spy too
    DelayForTrigger: 60
    # Commands in this list will not be shown when command spy is enabled for player for security/privacy reasons
    # This can be bypassed with cmi.command.commandspy.bypass permission node
    BlackListed:
    - register
    - login
    - l
    # Players without cmi.security.admin will only see commands from this list with command spy feature
    CommandList:
    - cmi spawn
    - cmi tp
    - cmi tpa
    - cmi heal
    - cmi feed
    - cmi fly
PlayerNotes:
  # For how long to keep players notes in days
  ExpiresIn: 30
PlayerMail:
  # For how long to keep players mail in days
  ExpiresIn: 30
  # Mailing to all players will send mails to players who loged into server in last x days
  mailAllDays: 7
DisplayName:
  # If you have 3rd party plugin changing players display name, set this to false
  Change: true
  # Format of players display name. By default only nick name will be visible, if its set, if not, then players name
  # Possible custom varibales: {prefix} {suffix} {nicknameprefix}
  # Supports placeholders
  Format: '{nickName}'
  # Defines regex for valid nick name
  # By default only letters and numbers are allowed
  # If you want to allow any letter from any language use [^\p{L}0-9\-\_]
  ValidNicknameRegex: '[^a-zA-Z0-9\-\_]'
NickName:
  # Prevents players to change their nick name to one of defined without permission
  # Use lower case
  # cmi.command.nick.bypassblacklist
  # to bypass protection against already in use name/nickname use cmi.command.nick.bypassinuse
  BlackList:
  - admin
  - administrator
  - server
  - staff
  - staf
  # Min length of nick name, can be bypassed with cmi.command.nick.bypass.length
  MinLength: 4
  # Max length of nick name, can be bypassed with cmi.command.nick.bypass.length
  MaxLength: 16
  # Adds prefix for players nickname to indicate that its not real name. This can be added to display name with {nicknameprefix}
  Prefix: '~'
  # When true, will only add nickname prefix when its not same as original name. This can allow colorization or capitalization change without addign prefix
  PrefixWhenDifferent: false
  TabComplete:
    # When true, online players nick name will be used instead of real name in tabcomplete
    ReplaceReal: true
    # When true, we will include real name on top of nickname. This only has effect when ReplaceName is enabled
    IncludeReal: false
Dye:
  # When set to true colored lether armor will be bound to the player who receives that coloration and will not work on others if he would give it to them
  # Only applies for dynamic armor colors like biome, health and so on
  BoundToPlayer: false
# Shows if there is an available new version on login with cmi.versioncheck permission node
ShowNewVersion: true
Spawners:
  # If you experiencing issues with spawner handling, set this to true to avoid any spawner manipulations from CMI side
  # This will disable features like, spawner placement, spawner drops, spawner charges and so on
  FullDisable: false
  Break:
    # ATTENTION! cmi.dropspawner will be required to get spawner dropping for the player
    # Enable or disable spawner handler for spawner break
    # If enabled player will get spawner if using silktouch pickaxe and have cmi.dropspawner permission node
    # If player has cmi.dropspawner.nosilk permission node, player is not required to use silk touch pickaxe to get droped spawner
    Enabled: false
    # If set to true, player will need to have particular permission node to break and get particular spawner.
    # In example: player should have cmi.dropspawner.pig to break pig spawner and get it dropped, or cmi.dropspawner.zombie to get zombie spawner
    RequiresExactPermission: false
    # When set to false, exp will not be dropped from broken spawner independent if spawner it self is being dropped
    # When set to true exp will be dropped only if spawner is not
    DropExp: false
    # Minimal silktouch level required to get spawner back
    SilkTouchLevel: 1
    # Number in percentage from 0 up to 100 for a spawner to be dropped when you break one
    BaseDropChance: 100
  Place:
    # Enable or disable spawner handler for spawner place
    # If enabled player will place spawner depending from what it is by its type
    # If disabled then spawner will be placed in normal way and it will allow other plugins to handle its placement
    Enabled: true
    # If set to true, player will need to have appropriate permission node to place spawner by its type
    RequiresPermission: false
    # RequiresPermission should be set to true for this to work. If set to true, player will need to have particular permission node to place particular spawner.
    # In example: player should have cmi.placespawner.pig to place pig spawner, or cmi.placespawner.zombie to place zombie spawner
    # If set to false, then player will need to have basic cmi.placespawner permission to place any type of spawner
    RequiresExactPermission: false
  Interact:
    # When set to true, players trying to change spawner with monster egg will require appropriate permission node
    # In example: player should have cmi.egginteract.pig to change spawner into pig, or cmi.egginteract.zombie to change into zombie spawner
    EggRequiresPermission: false
  # If set to true, spawners will have chance to be dropped when destroying with tnt
  TnTExplosionDrop:
    use: false
    # Chance in percentage for spawner to drop
    Chance: 30
  # If set to true, spawners will have chance to be dropped when destroyed by creeper
  CreeperExplosionDrop:
    use: false
    Chance: 30
  Charges:
    # When enabled players will be assigned to particular spawner charges group who have cmi.spawners.charge.[groupName] permission node
    # Players will be limited to how many spawners they can mine
    # StartingCharge will determine how many charges they will have on first time joining group
    # MaxCharge will limit to how many charges you can have at one time
    # Cooldown determines how often new charge will be given
    # Bonus is optional and it will determine by how many seconds to lower cooldown for next charge when placing spawner
    # Option to bypass limitations with cmi.spawners.charge.bypass
    Use: false
    # If set to true when player runs out of spawner charges spawner will be destroyed without droping it
    BreakWithoutCharge: false
    List:
      Noob:
        Use: false
        StartingCharge: 2
        MaxCharge: 5
        Cooldown: 3600
        Bonus: 10
      Advanced:
        Use: false
        StartingCharge: 3
        MaxCharge: 6
        Cooldown: 3000
        Bonus: 10
  Proximity:
    # Allows to limit how tight spawners can be placed from each other
    Use: false
    # Radius in blocks from blaced block. Max range is 16
    # Can bypass with cmi.spawners.proximity.bypass
    Range: 3
ItemRenaming:
  # When set to true, players will be denyied from renaming defined items in anvil or with itemname command
  # Option to define specific name by using regex format
  # Can be bypassed with cmi.anvil.itemrename.bypass
  Prevent: false
  # When set to true item renaming will be disabled in general, with anvil or command independent of renamed material
  # This can be bypassed with previous permission node
  GlobalDisable: false
  # List of materials followed with optional regex code which can prevent specific naming, like renaming mob spawners into another type while still allowing renaming spawner into anything else
  List:
  - mobspawner:([A-z]+ (?i)\w*spawner)
SpawnMob:
  # Defines how many passengers entities can be spawned at once
  MaxQuantity: 10
  MaxPassengers: 10
Counter:
  # Default range to use when performing /counter start
  Range: 10
Mirror:
  # Defines how far in blocks from mirror center you can build
  # This is mainly to protect from forgeting to turn off mirror and starting to build on different side of map
  MaxRange: 50
NetherPortal:
  # Can prevent nether portal creation entirely. Option to bypass with cmi.netherportalbypass
  PreventCreation: false
  # Maximum height nether portal can be created. Vanilla size is 23
  MaxHeight: 23
  # Maximum width nether portal can be created. Vanilla size is 23
  MaxWidth: 23
Portals:
  # Defines in milliseconds how often to check if player entered portal or not
  # Bigger numbers can help slightly lower server load but small portals, 1 block depth without back wall can be passed through without teleportations if player moves fast enought
  CheckInterval: 300
  # Defines in milliseconds how often to check if player entered portal range for particles to apear
  CheckParticleInterval: 500
  Defaults:
    # Should we perform commands without set destination location by default
    # This only effects newly created portal areas
    # When set to true at moment you create portal you can enter it and commands defined belove will be performed without teleporting you anywhere
    # This can be change for each portal independently with ingame portal editor
    PerformCommands: true
    # Commands to be performed on teleport event
    Commands:
    - cmi effect [playerName] blindness 2 1 -s
Animations:
  # Enable sitting on stair block by clicking on them with empty hand or by looking and using command
  # Requires cmi.command.sit.stairs
  SitOnStairs: true
  StairsAsChairs: true
  SlabsAsChairs: true
  CarpetsAsChairs: false
  RemoveFromChairOnDamage: true
  # Player will sit on chair only after rapid double click
  DoubleClick: false
  # Delay in milliseconds between clicks to sit on chair when double click is enabled
  DoubleClickDelay: 200
  # Range in blocks from player to look up for valid chair block
  ChairRange: 4
# All possible damage causes: contact, entity_attack, entity_sweep_attack, projectile, suffocation, fall, fire, fire_tick, melting, lava, drowning, block_explosion, entity_explosion, void, lightning, suicide, starvation, poison, magic, wither, falling_block, thorns, dragon_breath, custom, fly_into_wall, hot_floor, cramming, 
# Syntax should be [permissionNode]:[damageCause]:[multiplier]
# Example: nolavadamage:lava:0 will prevent lava damage with cmi.damagecontrol.nolavadamage permission node
# Negative values will heal player instead of damaging him
# If player have more than one permission node for same damage cause, then last one in list will be used to determine final damage
DamageControl:
- nowalldamage:fly_into_wall:1
- lowermagmacubedamage:hot_floor:0.9
Totem:
  # When this set to true, on players death totem will be used even if he is not holding it in hand
  RemoveFromInventory: false
  Cooldown:
    # When this set to true player can use totem only every X second's
    Use: false
    Time: 600
  Warmup:
    # When this set to true player can use totem to have X amount of second's, during which he can die and be resurected
    # Totem will be consumed durring activation and wont be returned even if resurection is not used during warmup time
    Use: false
    Time: 10
  # If player falls into void while having totem, he will be teleported to respawn location and totem gets consumed
  ProtectFromVoid: true
  Effects:
    # Time in seconds effect needs to be applied to the player. Set it to 0 if you want to disable it
    Regeneration: 45
    FireResistance: 40
    Absorbtion: 5
Elytra:
  # cmi.elytra - allows usage of elytra
  # cmi.elytra.boost - allows usage of boost
  # cmi.elytra.superboost - allows ussage of super boost
  # cmi.elytra.speedometer - allows to see speedometer
  Boost:
    # Max speed until player wont get any boost
    SpeedLimit: 200
    # When enabled items/exp wont be consumed if player is over speed limit
    SpeedLimitStop: false
    # Do you want to show decimals in speed
    SpeedDecimals: true
    # By how much boost player on each use
    GeneralMultyplier: 0.1
    # By how much boost player on each super boost use
    # Use shift while using simple boost
    SuperMultyplier: 0.3
    # Uses defined items instead of exp
    UseItems: false
    # Item material name
    # Defines item which will be consumed for each boost event
    ConsumedItem: STONE
    # Item material name
    # Set it to AIR if you want to allow boost without holding any particular item in your hand
    # Keep in mind that you still need to hold any item or click left mouse button for it to work when its set to AIR
    Item: FEATHER
    # Item material name
    # Set it to AIR if you want to allow launch to be performed without holding any particular item in your hand
    # Keep in mind that you still need to hold any item or look at a block for it to work properly when its set to AIR
    LaunchItem: FEATHER
    # Requires to hold defined item in hand. Only when UseItems is set to false
    RequiresItem: true
    # Amount of exp consumed on each boost
    Amount: 1
    # Amount of exp consumed on each super boost
    SuperAmount: 5
    # Shows particles when flying
    ShowParticles: true
  Launch:
    Time: 2
  # 1.13+ servers. Do you want to disable riptide enchant usage while flying with elytra and trident which has riptide enchant
  # This combination is dangerous as player can reach extreme speed's if allowed to use it
  DisableRiptide: false
  Fix:
    # Disables option to damage yourself while flying with arrows to boost up
    PreventSelfDamage: false
    # Disables option to use rockets to boost yourself while flying with elytra
    PreventRocketUsage: false
FlightCharge:
  # By default boss bar message will be shown with remaining charges. If disabled then bossbar will only appear when flight charge was modified but not when its depleating while flying
  ShowBossBar: true
  # When set to true, each time player gets flight charge or relogs, his fly mode will be toggled on
  # If set to false, then players will have to manually turn on flight with /cmi flyc
  EnabledByDefault: true
  # When set to true, in event of player changing his game mode from survival/adventure to creative/spectator his flight charge  mode will get disabled
  # Same applies when changing game mode from creative/spectator to survival/adventure
  AutoSwitch: false
  # How much it costs for one recharge point in exp points. Value can be in decimals, like 0.2 but it cant be equal or lower than 0
  # Set to 0 to disable this type of recharge
  ExpRechargeCost: 1.0
  # How much it costs for one recharge point. Value can be in decimals, like 0.2 but it cant be equal or lower than 0
  # Set to 0 to disable this type of recharge
  MoneyRechargeCost: 1.0
  # Defines maximum amount of charge player can have
  # One charge is one traveled block while flying
  # if player doesn't move, then one charge for each second while hovering
  MaxChargeLevel: 1000
  # Defines multiplier when player doesn't move but is hovering. For each second player hovers.
  # Set to 0 to disable
  DeductOnIdling: 1.0
  # If this is set above 0, then player will loose defined amount of charges each second they are flying instead of traveled blocks
  # Set to 0 to disable, which will deduct charges for traveled blocks
  DeductOnlyForTime: 0.0
  AutoRecharge:
    # Value in percentage when we should automatically recharge players flight charges if player enabled autorecharge with /autorecharge command
    From: 10.0
    # Value in percentage of charges we need to recharge
    # 25 will result into 25% of max allowed charges being recharged each time auto recharge is triggered
    Amount: 25.0
  # Defines multiplier when player falls down of charge to be taken
  # This only effects when player falls from above 3 blocks of hight
  # In example if player falls from 10 blocks height, then 7 * 2 = 14 charges will be taken
  # This is to prevent avoiding no penalty from jumping from cliffs
  # Set to 0 if you want to disable it
  DeductOnFallMulti: 2
  # Defines if you want to damage player when he falls down from higher than 3 blocks height
  # This will not kill player even if he would drop from 200 block height, but will leave him with 1 hp
  # This will only effect players who jumped down and not those who disabled fly mode in mid air
  DamageOnFall: true
  # DamageOnFall should be enabled for this to work
  # This will define if you want to damage player when he deactivates fly mode in mid air
  DamageOnToggle: false
  # DamageOnFall should be enabled for this to work
  # This will define if you want to kill player if fall damage if higher than his health amount
  KillOnFall: false
  # When color name is defined then at moment player starts flying with flight charges, he will start glowing
  # Set this to 'none' if you want to disable it
  GlowColor: none
Point:
  # Default particle for point command. Options: fireworks_spark, crit, magic_crit, potion_swirl, potion_swirl_transparent, spell, instant_spell, witch_magic, note, portal, flying_glyph, flame, lava_pop, footstep, splash, particle_smoke, explosion_huge, explosion_large, explosion, void_fog, small_smoke, cloud, coloured_dust, snowball_break, waterdrip, lavadrip, snow_shovel, slime, heart, villager_thundercloud, happy_villager, large_smoke, water_bubble, water_wake, suspended, barrier, mob_appearance, end_rod, damage_indicator, sweep_attack, totem, spit, squid_ink, bubble_pop, current_down, bubble_column_up, nautilus, dolphin, water_splash, campfire_signal_smoke, campfire_cosy_smoke, sneeze, composter, flash, falling_lava, landing_lava, falling_water, dripping_honey, falling_honey, landing_honey, falling_nectar, soul_fire_flame, ash, crimson_spore, warped_spore, soul, dripping_obsidian_tear, falling_obsidian_tear, landing_obsidian_tear, reverse_portal, white_ash, light, falling_spore_blossom, spore_blossom_air, small_flame, snowflake, dripping_dripstone_lava, falling_dripstone_lava, dripping_dripstone_water, falling_dripstone_water, glow_squid_ink, glow, wax_on, wax_off, electric_spark, scrape, block_marker, sonic_boom, sculk_soul, sculk_charge_pop, 
  DefaultParticle: COLOURED_DUST
Messages:
  Login:
    # If set to true, login message wont be shown
    Disabled: false
    # Defines number of players from which to automatically start hiding join messages
    # Set to -1 to disable this
    AutoHideFrom: -1
    Custom:
      # If set to true, custom login message will be used. cmi.messages.disablelogin can be used to disable message for player
      Use: false
      # When enabled and you have bungeeserver with CMIB on it we will try to detect where player went and we will show switch server message instead of login if posible
      ServerSwitch: true
  Logout:
    # If set to true, logout message wont be shown
    Disabled: false
    # Defines number of players from which to automatically start hiding logout messages
    # Set to -1 to disable this
    AutoHideFrom: -1
    Custom:
      # If set to true, custom logout message will be used. cmi.messages.disablequit can be used to disable message for player
      Use: false
      # When enabled and you have bungeeserver with CMIB on it we will try to detect where player went and we will show switch server message instead of logout if posible
      ServerSwitch: true
  # Check locale file for translation and custom placeholders: [playername], [totalUsers], [onlinePlayers]
  FirstJoinMessage:
    Use: false
Books:
  # Defines default creator name for books when using getbook command
  DefaultAuthor: Server
  # When set to true books write date will be added
  AddDate: false
# Defines name of customtext on players login to server. To disable just set name to non existing customText
Motd: welcomeMessage
Warnings:
  Default:
    LifeTime: 86400
    Points: 1
    DefaultReason: '&7Violated server rules'
  Categories:
    Swear:
      LifeTime: 86400
      Points: 3
      DefaultReason: '&7Swearing'
    Grief:
      LifeTime: 86400
      Points: 10
      DefaultReason: '&7Griefing'
    Bug:
      LifeTime: 86400
      Points: 30
      DefaultReason: '&7Using bugs'
    Cheat:
      LifeTime: 86400
      Points: 50
      DefaultReason: '&7Using cheats'
  Perform:
    '3':
    - cmi mute [playerName] 10m
    - cmi msg [playerName] !&cMuted for &710 &cminutes for getting &73 &cwarnings!
    '5':
    - cmi kick [playerName] &cKicked for getting 5 warnings!
    '10':
    - cmi tempban [playerName] 5m &cTemporary banned for getting 10 warnings!
Spawn:
  # Forces players to login in defined spawn point when logging into server
  # Can be bypasses with cmi.spawnonjoin.bypass permission node
  SpawnOnJoin: false
  # List of worlds which should be ignored and players joining in those servers will not be teleported to appropriate spawn point but will login at their log out location
  IgnoredWorlds: []
  # Defines players spawn point after death if set to true, if not, then it will be used only for /cmi spawn command
  # RespawnLocation will indicate if you want to use this location as possible respawn point for player after death
  Main:
    World: None
    X: 0.0
    Y: 0.0
    Z: 0.0
    Pitch: 0.0
    Yaw: 0.0
    RespawnLocation: false
    Rng: 0
  # Defines players first spawn point when he logs into server for the first time
  FirstSpawn:
    Use: true
    World: None
    X: 0.0
    Y: 0.0
    Z: 0.0
    Pitch: 0.0
    Yaw: 0.0
Newbie:
  # Kit name to give for new players joining server
  Kit: Newbie
Kits:
  # When set to true, kit list will be shown in GUI instead of chat list
  GUI: true
  # When set to true, kit selection gui empty fields will get filled with definet item
  FillEmptyFields: true
  Buttons:
    Cooldown: Watch
    Usages: STONE_PLATE
    Money: GOLD_INGOT
    Exp: EXP_BOTTLE
    Desc: WOOL:13
    Back: Fence
  Complex:
    CloseButton:
      Use: true
      Slot: 9
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNmNjYmY5ODgzZGQzNTlmZGYyMzg1YzkwYTQ1OWQ3Mzc3NjUzODJlYzQxMTdiMDQ4OTVhYzRkYzRiNjBmYyJ9fX0=
      Commands:
      - closeinv!
    InfoButton:
      # Extra button to be used in case you want to provide any aditional information when clicking on it
      Use: false
      Slot: 1
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDZiYTYzMzQ0ZjQ5ZGQxYzRmNTQ4OGU5MjZiZjNkOWUyYjI5OTE2YTZjNTBkNjEwYmI0MGE1MjczZGM4YzgyIn19fQ==
      Commands:
      - closeinv!
Warps:
  # When set to true, warps list will be shown in GUI instead of chat list
  GUI: true
  # Automatically opens GUI when created new warp point
  GUIOnCreation: true
  # Minimal length of warp name
  MinLength: 4
  # Maximal length of warp name
  MaxLength: 16
  # How many warps to show in each page
  perPage: 50
  # Do you want to show creator in warp list
  showCreator: false
  # When set to true, new warps by default will require permission node to use them
  requirePerm: false
  Complex:
    CloseButton:
      Use: true
      Slot: 9
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNmNjYmY5ODgzZGQzNTlmZGYyMzg1YzkwYTQ1OWQ3Mzc3NjUzODJlYzQxMTdiMDQ4OTVhYzRkYzRiNjBmYyJ9fX0=
      Commands:
      - closeinv!
    InfoButton:
      # Extra button to be used in case you want to provide any aditional information when clicking on it
      Use: false
      Slot: 1
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDZiYTYzMzQ0ZjQ5ZGQxYzRmNTQ4OGU5MjZiZjNkOWUyYjI5OTE2YTZjNTBkNjEwYmI0MGE1MjczZGM4YzgyIn19fQ==
      Commands:
      - closeinv!
DynamicViewRange:
  # By setting to true will enable dynamic view range feature. Its still in beta stage and can result in some CPU load increase.
  # Don't enable if you are not using this feature on your server
  Enabled: false
WorldLimits:
  # By setting to true fly and gamemode limitations per world will be aplied for player on world change if they dont have appropiate permission node
  Enabled: false
  # World list with default game modes
  # If player will have cmi.worldlimit.gamemode.bypass permission node, game mode wont be changed
  # Possible modes: creative, survival, adventure, spectator, 
  Gamemode:
  - testWorld:Survival
  # If player will have cmi.worldlimit.fly.bypass permission node, fly mode wont be changed
  Fly:
  - testWorld:False
  # If player will have cmi.worldlimit.elytra.bypass permission node, elytra flight will not be prevented
  # Players joining worlds with disable elytra flight will get their elytra dismounted if posible
  ElytraFlight:
  - worldName:False
  # When set to false, only players with cmi.worldlimit.fly.aboveroof can fly above world build limit
  FlyAboveRoof: true
  # When set to false, only players with cmi.worldlimit.fly.aboveroof can fly above world build limit
  FlyAboveRoofLimitations:
  - Spawn-256
  # If player will have cmi.worldlimit.god.bypass permission node, god mode wont be changed
  GodMode:
  - testWorld:False
  # Prevents particular entity spawn reasons in defined worlds. All possible reasons: NATURAL, JOCKEY, CHUNK_GEN, SPAWNER, EGG, SPAWNER_EGG, LIGHTNING, BUILD_SNOWMAN, BUILD_IRONGOLEM, BUILD_WITHER, VILLAGE_DEFENSE, VILLAGE_INVASION, BREEDING, SLIME_SPLIT, REINFORCEMENTS, NETHER_PORTAL, DISPENSE_EGG, INFECTION, CURED, OCELOT_BABY, SILVERFISH_BLOCK, MOUNT, TRAP, ENDER_PEARL, SHOULDER_ENTITY, CUSTOM, DEFAULT
  SpawnReasons:
    Spawn:
    - None
# Checks and shows on players login if he have been changed hes name over Mojang
# Looks to be working only with online servers, duhhhh
CheckForNameChange:
  OnLogin: false
  AmountToShow: 3
  OnInfoShow: true
  # Do you want to perform commands
  PerformCommandsOnNewName: false
  # Command list to be performed in case player logs in with new name
  NameChangeCommands:
  - 'asConsole! cmi broadcast !&2[oldname] logged in with new name: [newname]'
inv:
  # Do you want to save the player's inventory on his death
  SaveOnDeath: false
  # When set to true, empty inventories (no items in inventory) will not be saved on players death
  IgnoreEmpty: false
  # If set to true then player should have cmi.saveinv permission node for inventory to be saved on death
  RequiresPermission: false
  # How many inventories, we will keep for each player
  SavedInventories: 5
  restore:
    # Set to false if you don't want to restore hp state on inventory load with /cmi invload command
    HP: true
    # Set to false if you don't want to restore players experience points
    XP: true
    # Set to false if you don't want to restore food state
    Food: true
    # Set to false if you don't want to restore saturation level
    Saturation: true
    # Set to false if you don't want to restore potion effects
    Potions: true
    # Set to false if you don't want to restore items
    Items: true
hunger:
  # Do you want to give more than 20 hunger for players
  overide: false
heal:
  RemoveNegative:
    # Do you want to remove negative potion effects from player on heal
    use: false
    List:
    - blindness
    - confusion
    - harm
    - hunger
    - poison
    - slow
    - slow_digging
    - weakness
    - wither
Cuff:
  # When set to false will allow players to talk who is cuffed
  Mute: true
  AllowedCommands:
  - msg
  - r
  - tell
Mute:
  # When set to true, player will not be allowed to send private messages while he is muted
  DenyPrivateMessages: true
Dispose:
  # defines how big is dispose ui 1-6
  UILines: 4
ItemRepair:
  RepairShare:
    # When neabling you will need to perform full server restart for it to take effect
    # When enabled will prevent players repairing items for others in anvil regular way. They still can use items and repairs normaly for them selfs
    # Can be bypassed with cmi.command.repair.repairshare.bypass
    ProtectNormalRepair: false
    # When enabled will prevent players repairing items for others with CMI command. They still can use items and repairs normaly for them selfs
    ProtectCommandRepair: false
    # Sets durability on item when another picks it up or selects in inventory. Set to 0 or less if you don't want to change durability
    # Attention! Keep this number above 0, otherwise item will get removed without option for the player to repair it throw some means, unless this is what you actually want
    Durability: 1
    # When set to true, player who have cmi.command.repair permission will bypass this protection and can use other user repaired items without any additional actions
    BypassWithRepairPermission: true
    # When enabled additional lore line will be added when player can't use that item. This will not be shown for owner of item
    AddLore: true
    # When set to true, interact event will be canceled to prevent item usage
    CancelEvent: true
    # When set to true, player will get message informing about item usage he dint repaired him self
    InformWithMessage: true
  Repair:
    # List of custom model data id's we should not allow to be repaired with /repair command
    BlockedCustomDataID:
    - 298785423
    # When item costs money, player will be required to confirm repair action by clicking message in chat
    Confirmation: true
    # When set to true, item repair with /cmi repair will cost money depending on setup
    # Player who performs command will pay repair cost
    # If command gets performed from console, then player whose items are repaired will be paying
    CostsMoney: false
    # Base price to repair item
    # If you have enabled durability check, then this value will wary depending on items condition
    BasePrice: 100.0
    # Item repair cost will depend on how baddly item is damaged
    CheckDurability: true
    # Adds extra cost to repair depending on items cost set in /cmi setworth
    # Value should be set from 0 to 100 range
    WorthPercentage: 10.0
    # Adds extra cost to repair depending on items enchantment cost set in /cmi setenchantworth
    # Value should be set from 0 to 100 range
    # If item has more then one enchantment, then prices will be added up
    enchantWorthPercentage: 10.0
Cooldowns:
  # You can enable any command cooldown to prevent instant usage of it
  # cmi heal:180 means that player can use /cmi heal command only once every 180 seconds
  # if cooldown set to -1 then this command can be performed only one time
  # Administration can bypass limitations with cmi.cooldownbypass.[commandname] permission node
  # Always use full command name and not its alias
  # ----------
  # Alternatively you can use cmi.cooldown.[some_command].[timer] permission node. For example: cmi.cooldown.cmi_heal.30 which will set 30 second cooldown on /cmi heal command
  # If you want to apply cooldown on command when variable is provided, add extra _ at end. For example cmi.cooldown.cmi_heal_.30 which will only use this cooldown when healing some one else
  # KEEP IN MIND that for permission to work you need to set base command cooldown in this list, otherwise permission node will have no effect
  # -----
  # ATTENTION! If you have command like "/cmi home" and you want to prevent teleportation to home but allow gui opening without restrictions, use space after command, in example "cmi home :10"
  Enabled: false
  List:
  - cmi heal:180
  - cmi feed:120
Combat:
  # Defines combat timer to be used in particular features
  Timer: 15
  # When enabled we will allow for players to be damaged in safe zone if they are tagged for pvp
  safeZoneDamage: false
  # If set to true, then attacked player will be included into combat mode even if he doesnt fight back
  # If set to false then only attacker will be marked for pvp mode
  IncludeVictim: true
  Player:
    # If set to true, then player who gets placed into combat mode will get its fly mode disabled
    # This will disable players fly mode which will result in player dropping down and will disable option to start flying
    # This can be bypassed by player performing fly command if he has access to it and commands durring combat are not blocked
    # Can be bypassed with cmi.pvp.PFlyBypass permission node
    DisableFlight: false
    # If set to true player whose fly mode got disabled will not suffer fall damage, once
    DisableFallDamage: false
    # When set to true player will see boss bar message indicating how long until combat mode ends
    # This only applies for pvp type combat
    ShowBossBar: false
    # Prevents damage from players with god mode enabled
    # Can be bypassed with cmi.pvp.godBypass permission node
    noGodDamage: false
    # Informs player that he cant damage players while in god mode
    noGodDamageInform: false
    # When set to true players will be only able to use commands defined in the list
    # This only applies for pvp type combat
    BlockCommands: false
    AllowedCommands:
    - msg
    - r
    - tell
    # When set to true AllowedCommands become black list which will define which commands player cant use
    MakeBlackList: false
  Mob:
    # If set to true, then player who gets placed into combat mode will get its fly mode disabled
    # Can be bypassed with cmi.pvp.MFlyBypass permission node
    DisableFlight: false
    # If set to true player whose fly mode got disabled will not suffer fall damage, once
    DisableFallDamage: false
    # When set to true player will see boss bar message indicating how long until combat mode ends
    # This only applies for pve type combat
    ShowBossBar: false
    # Prevents damage from players with god mode enabled
    # Can be bypassed with cmi.pve.godBypass permission node
    noGodDamage: false
    # Informs player that he cant damage mobs while in god mode
    noGodDamageInform: false
    # When set to true players will be only able to use commands defined in the list
    # This only applies for pve type combat
    BlockCommands: false
    AllowedCommands:
    - msg
    - r
    - tell
    # When set to true AllowedCommands become black list which will define which commands player cant use
    MakeBlackList: false
  Heads:
    Player:
      Drop: false
      # Percentage from 0 to 100 for head to be dropped. Decimals are acceptable, like 0.2
      # 100 will mean that head will be dropped every time player kills another player
      # 1 will mean that there is 1% that player will drop head if he is killed by another player
      Percentage: 1.0
      # Percentage from 0 to 100 for lowering chance in getting second head of same player
      # This will reset on each server restart
      LowerChanceOfterDrop: 50.0
      # When enabled player heads will have bigger chance to drop when using tools with looting enchantment
      # Value is in % and it will add appropriate percentage to current drop chance by using drop chance itself
      # For example player who has head drop change of 1% with looting 3 which has 30% bonus will have 1.3% as end value (default values)
      # This only applies for player heads
      # You can add as many levels as you want, simply duplicate line and set new number, in example
      # Lvl33: 35.5
      LootBonus:
        Enabled: true
        Lvl1: 5.0
        Lvl2: 15.0
        Lvl3: 30.0
      # List of worlds where we should drop player heads. Keep it empty if you want to include all posible ones
      Worlds: []
    Mob:
      # Enables custom mob heads dropping from mobs with particular chance
      # Check customHeads.yml for customization by entityType
      Drop: false
      # List of worlds where we should drop mob heads. Keep it empty if you want to include all posible ones
      Worlds: []
ShulkerBoxes:
  # When set to true, players will not have option to open shulker boxes while in combat
  # Combat timer can be defined under combat section
  PreventInCombat: true
Vanish:
  # Defines default states of vanish edit options for players
  # This will not have any effect if player already edited his vanish mode with vanishedit command
  Defaults:
    damageToEntity: false
    playerDamage: false
    itemPickup: false
    mobAggro: false
    interaction: false
    noisyChest: false
    informOnLeave: false
    informOnJoin: false
    nightVision: true
    bossbar: true
    afkcommands: false
    PrivateMessages: false
    relogDisable: false
    noMessages: false
    fakeJoinLeave: false
    mobSpawning: false
    stopPlaytime: true
    sleepIgnore: true
    joinVanished: false
Player:
  Options:
    CloseButton:
      Use: true
      Slot: 9
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNmNjYmY5ODgzZGQzNTlmZGYyMzg1YzkwYTQ1OWQ3Mzc3NjUzODJlYzQxMTdiMDQ4OTVhYzRkYzRiNjBmYyJ9fX0=
      Commands:
      - closeinv!
    InfoButton:
      # Extra button to be used in case you want to provide any aditional information when clicking on it
      Use: false
      Slot: 1
      Material: head:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDZiYTYzMzQ0ZjQ5ZGQxYzRmNTQ4OGU5MjZiZjNkOWUyYjI5OTE2YTZjNTBkNjEwYmI0MGE1MjczZGM4YzgyIn19fQ==
      Commands:
      - closeinv!
    # Defines default states for player options
    # This will not have any effect if player already edited his options with /cmi options command
    Defaults:
      visibleHolograms: true
      shiftSignEdit: true
      totemBossBar: true
      bassBarCompass: true
      tagSound: true
      # !Strongly not recommended to be enabled!
      chatSpy: false
      # !Strongly not recommended to be enabled!
      cmdSpy: false
      # !Strongly not recommended to be enabled!
      signSpy: false
      acceptingPM: true
      acceptingTPA: true
      acceptingMoney: true
WarmUps:
  # You can enable any command warmup to prevent instant command usage
  # tp:5:false means that when player performs /tp command he will need to wait 5 sec
  # false variable is optional and when its set to false player cant move while warmup is counting
  # If you dont want to deny empty warp command but want to deny any extra variable after that, then just add space, in example 'warp :5:false'
  # When setting warmups for CMI commands, use full command name and not allias, in example 'cmi warp:5false'
  # Administration can bypass limitations with cmi.warmupbypass.[commandname] permission node
  # ATTENTION! cmi home command is being handled in special way and to prevent double warmup, add space, example: - cmi home :5:false
  # Experimental: add GlyphHead to the warmup to show particle effect while command is on warmup period. Like
  # - cmi warp :3:false:GlyphHead
  Enabled: false
  InformOnNoMove: true
  showCounterBarInfo: false
  showBossBarInfo: false
  List:
  - cmi tp :5:false
  - cmi back:3:true
  - cmi warp :3:false
  - cmi home :3:false
Jail:
  # Defines in milliseconds how often to check if player leaves jail area
  # Bigger numbers can help slightly lower server load
  CheckInterval: 500
  # Defines default jail time when time is not povided with command
  DefaultTime: 300
  # Chat range in blocks while player is in jail
  # Set to 0 to allow talking
  # set to -1 to prevent talking in general while jailed
  ChatRange: 20
  # When set to true jail time will decreese while player is offline
  # When set to false jail time will only be counted while player is online
  CountWhileOffline: false
  # When set to true jail time will not decreese if player gets into afk mode while being jailed
  # When set to false, time will pass normally
  NoAfk: false
  # Do you want to prevent players damage while he is in jail
  PreventDamage: true
  # Do you want to prevent players hunger while he is in jail
  PreventHunger: true
  WhiteListedCmds:
  - cmi msg
  - cmi reply
scan:
  # Tps cap from which to start adjusting scan speed
  SoftCap: 19.0
  # Staring speed when scanning. Range from 1 to 30
  DefaultSpeed: 15
  # When this set to true, when using scan feature and not providing range, whole map will be scanned
  GlobalRangeByDefault: false
  # Range in chunks. 2 is 25 chunks, 1 is 9 and 0 is only chunk you are standing in
  DefaultRange: 2
  # When this set to true, all found items in containers will be removed automatically durring scan. Ex: /scan id 7 purge
  EnablePurge: false
search:
  # When this set to true, all found items in inventories will be deleted durring search. Ex: /cmi search id 7 purge
  EnablePurge: false
lfix:
  # Tps cap from which to start adjusting light fix speed
  SoftCap: 19.0
  # Staring speed when fixing light. Range from 1 to 100
  DefaultSpeed: 15
# Removeuser command will use same configurations when removing player data files or moving them to new place
purge:
  # Cleans files on server startup
  CleanOnStart: false
  # How long player should be offline for his data to be moved
  OfflineDays: 90
  PlayerData:
    # Do you want to enable player data file cleaning
    Enabled: true
    # Source folder to take files from
    SourceFolder: Spawn/playerdata
    # When this is false, data files will be moved to backup folder. When its true files will be deleted
    DeleteFiles: false
    # Target folder to put files into if DeleteFiles set to false
    DestinationFolder: Spawn/playerdata_backup
  PlayerStats:
    # Do you want to enable player stats file cleaning
    Enabled: true
    # Source folder to take files from
    SourceFolder: Spawn/stats
    # When this is false, data files will be moved to backup folder. When its true files will be deleted
    DeleteFiles: false
    # Target folder to put files into if DeleteFiles set to false
    DestinationFolder: Spawn/stats_backup
  PlayerAdvancements:
    # Do you want to enable player Advancements file cleaning
    Enabled: true
    # Source folder to take files from
    SourceFolder: Spawn/Advancements
    # When this is false, data files will be moved to backup folder. When its true files will be deleted
    DeleteFiles: false
    # Target folder to put files into if DeleteFiles set to false
    DestinationFolder: Spawn/Advancements_backup
  Essentials:
    # Do you want to enable essentials playerdata file cleaning
    Enabled: false
    # Source folder to take files from
    SourceFolder: plugins/Essentials/userdata
    # When this is false, data files will be moved to backup folder. When its true files will be deleted
    DeleteFiles: false
    # Target folder to put files into if DeleteFiles set to false
    DestinationFolder: plugins/Essentials/userdata_backup
  LWC:
    # Do you want to enable lwc protection cleaning
    Enabled: false
Selection:
  # Tool id to use for selection actions
  Tool: wooden_shovel
Time:
  # Defines preset time
  Day: '12:00'
  Night: '24:00'
  Morning: 06:00
  Dusk: '18:00'
  AutoTime:
    # Time in seconds time in game will be adjusted to match real
    # Keep it at arround one minute
    Interval: 60
    # Enables by default smooth sun transition to new time
    # You can always override this setting with -smooth variable in time command
    Smooth: true
    # Speed of smooth transition
    # 100 will mean that sun moves 100 times faster than usual until it reaches target time
    SmoothSpeed: 100
    # Worlds effected by autotime adjustment
    Worlds:
    - ''
  # Allows you to change vanilla time speed to your own liking and needs
  TimeSpeed:
    # Time is defined in seconds. Vanilla 24 hour ingame duration is 1200 seconds of real time
    Spawn:
      Enabled: false
      # Default value: 600 Starts from tick: 0 Ends at tick: 12000
      day: 600
      # Default value: 90 Starts from tick: 12000 Ends at tick: 13800
      sunset: 90
      # Default value: 420 Starts from tick: 13800 Ends at tick: 22200
      night: 420
      # Default value: 90 Starts from tick: 22200 Ends at tick: 24000
      sunrise: 90
RandomTeleportation:
  # If this set to true we will generate random teleport default settings for all detected worlds
  # Setting to false will not longer generate world setups, but you can add them manually if needed
  AutoGenerateWorlds: true
  Worlds:
    # World name to use this feature. Add annother one with appropriate name to enable random teleportation
    Spawn:
      Enabled: true
      # Max coordinate to teleport, setting to 1000, player can be teleported between -1000 and 1000 blocks between defined center location
      # For example having centerX at 2000 and centerZ at 3000 while MaxRange is set to 1500 we will teleport player between x:500;z:1500 and x:3500;z:4500 coordinates
      MaxRange: 1000
      # If maxcord set to 1000 and mincord to 500, then player can be teleported between -1000 to -500 and 1000 to 500 coordinates
      MinRange: 500
      CenterX: 0
      CenterZ: 0
      Circle: false
      IgnoreWater: true
      IgnoreLava: true
      minY: 0
      maxY: 256
  # How long force player to wait before using command again.
  Cooldown: 5
  # How many times to try find correct location for teleportation.
  # Keep it at low number, as player always can try again after delay
  MaxTries: 20
  # List of biomes to exclude from random teleportation
  ExcludedBiomes:
  - Ocean
  - Deep ocean
Enchanting:
  enchantLimits:
    # By disabling this, no limitation to enchanting will be applied
    # This only applies for enchant command not for natural enchanting
    Enabled: true
    MaxLevel:
      protection_environmental: 4
      protection_fire: 4
      protection_fall: 4
      protection_explosions: 4
      protection_projectile: 4
      oxygen: 3
      water_worker: 1
      mending: 1
      thorns: 3
      vanishing_curse: 1
      depth_strider: 3
      frost_walker: 2
      binding_curse: 1
      damage_all: 5
      damage_undead: 5
      damage_arthropods: 5
      knockback: 2
      fire_aspect: 2
      loot_bonus_mobs: 3
      sweeping_edge: 3
      dig_speed: 5
      silk_touch: 1
      durability: 3
      loot_bonus_blocks: 3
      arrow_damage: 5
      arrow_knockback: 2
      arrow_fire: 1
      arrow_infinite: 1
      luck: 3
      lure: 3
  # When set to true, players will be required to have cmi.enchantments.[enchantname] permission node
  RequireSpecificPermission: false
  # When set to true, players will be required to have cmi.enchantments.[enchantname].[maxlevel] permission node to be abble to enchant item to defined max level
  # Higest permission will be taken if player has more then one
  # Keep in mind that this will not prevent player from enchanting item to lower levels then permission was set too
  # And keep in mind that players without defined permission node will have access to level 1 enchants by default
  PermissionLevelLimit: false
Scavenge:
  ItemBreak:
    # Defined percentage for item to break when salvaging it
    # Value can be from 0 to 100, where 100 means that each time player extract enchant, item breaks
    # This can allow player to extract enchantments without breaking item itself
    # Set it to 100 if you want to always break item
    # Keep in mind that broken item will go throw ingredient return process
    # Attention! Items without enchants will have 100% break chance
    Base: 8.0
    # Adds extra chance to break item depending on how many enchants item has
    # In example having base chance of 8% and having this set to 2 while having item with 3 enchants will result into 8+(2*3)=14% chance to break item
    ForEachEnchant: 2.0
    # Adds extra chance to break item depending on enchant level
    # This will take into consideration enchantment max and current levels
    # Having this set to 7.5 means, that enchantment at max level will have 7.5% extra chance to to break item
    # But if you have sharpness 2 which has max level of 5, then only 3% fail chance will be added
    ForEachEnchantLevel: 2.0
    # Defines in percentage a max chance to break item when extracting enchants
    # This can limit chance to particular one in case it gets to 100% and it would always break
    MaxBreakChance: 100.0
    # Value between 0 and 100 which defines extra fail chance when items doesnt have max durability
    # Having this set to 50 will mean that item at 1 left durability will have fail chance increase by 50%
    # Items which are not damaged will not experience any fail chance increase
    BreakDurabilityCheck: 50.0
    # When set to true, items durability will be taken into consideration when extracting ingredients
    # In example if item has 100 max durability and current is at 50, then only half of ingredients will be considered for extraction
    # This doesnt mean that player gets 50% of them, it only means that half of posible ingredients will go throw IngredientReturn process
    DurabilityCheck: true
    IngredientReturn:
      # Defines in percentage a max chance to return ingredients of item if it fails extraction process
      # This will apply for each ingredient that item has
      # Recipe to make that item should exist in database, or it will not return any ingredients
      Base: 25.0
  EnchantExtractionFail:
    # Adds base chance to fail enchantment extraction
    # When enchantment fails, player will not get enchant book with appropriate enchantment
    Base: 10.0
    # Adds extra chance to fail enchantment extraction depending on enchantment level
    # This will take into consideration enchantment max and current levels
    # Having this set to 75 means, that enchantment at max level will have 75% chance to fail extraction process
    # But if you have sharpness 2 which has max level of 5, then only 30% chance to fail will get applied
    # While enchants like Aquaaffinity will always have max fail chance as you can only have it at level 1
    ForEachLevel: 10.0
    # Defines in percentage a max chance to fail enchantment extraction
    # This can limit chance to particular one in case it gets to 100% and it would always fail
    MaxFailChance: 75.0
    LevelLower:
      # Defines a chance lowering enchant level if it fails extraction
      # This is secondary step when extraction fails and will only apply when it does
      # If Enchant is at level 1 already, then player will not get enchanted book at all
      # If you want to avoid lowering level of enchant when it fails extraction, set this to 100
      # If you want to always lower level down when extracting enchantments, then set EnchantExtractionFail.Base to 100 and set this to 100
      Base: 50.0
      # Will adjust level lowering chance depending on enchant level to defined max amount at max level
      # This will mean that higher levels will have higher chance to be lowered
      ForEachLevel: 5.0
      # Will adjust level lower chance depending on enchant level to defined max amount at max level
      MaxChance: 75.0
  Cost:
    # Defined base cost of extraction. Set to 0 if you want to make it free
    Base: 100.0
    # Extra cost which depends on enchantment worth which can be defined with /cmi setenchantworth 
    # This value is in percentage from worth value of that each enchantment and item
    # So if you have base cost of 100, extra cost of 5% and you are trying to extract sharpness 5 which worth is 1000 and item sell hand worth is 100, then you will have to pay 155 for extraction process
    Extra: 5.0
  # List of materials to block from being scavenged
  BlackList:
  - diamond
  - ironingot
  - goldingot
  - coal
  # When set to true, balck list becomes whitelist and will allow scavanging of items defined in a blacklist only
  BlackToWhiteList: false
  # When set to false while player have open scavange UI they will not be able to pickup item from ground
  AllowItemPickups: false
  # When enabled items, likes swords, after being salvagted if they dint broke then their repair cost will be reset so players can enchant it as like its a new one instead of making it to dificult to be enchanted
  ResetRepairCost: true
BungeeCord:
  # You can disable bungeecord support entirely if you are exrperiencing issues with it
  # When setting this to false some features like public messages over bungee cord, private messages over bungeecord, portals over bungecoord and other features will stop working
  # Keep in mind that regular behavior of those features will remain intacted
  Enabled: true
  # When set to true player names from entire bungee network will be included into tab complete
  NamesInTabComplete: false
# If you want to disable particular sound entirely, set it to "" 
Sounds:
  Enabled: true
  WarpGuiOpen: entity_bat_takeoff:0.5:1
  TeleportHome: block_beacon_activate:2:1
  TeleportWarp: entity_enderman_teleport:0.5:1
  TeleportFail: entity_villager_no:2:1
  PrivateMessage: entity_endermite_death:2:1
  TpaRequest: block_anvil_land:0.5:2
  MailNotification: entity_creeper_hurt:1:0.5
  TeleportUp: entity_enderman_teleport:2:1
  TeleportDown: entity_enderman_teleport:0.2:1
# If you want to disable particular particle entirely, set it to "" 
# More information how to set up this one can be found at https://www.zrips.net/cmi/extra/particles/
Particles:
  Enabled: true
  TotemHalo: circle;effect:reddust;c:255,255,10;twist;part:3;offset:0,2,0;pitch:90;radius:0.3;interval:2
  Healing: circle;effect:heart;dur:0.1;part:1;offset:0,1.7,0;radius:0.3
  GlyphHead: circle;effect:flying_glyph;dur:5;pitchc:15;part:10;offset:0,1.7,0;radius:0.5;yawc:12;color:rs;pitch:90
  tpaWarmup: circle;effect:flying_glyph;dur:5;pitchc:15;part:10;offset:0,1.7,0;radius:0.5;yawc:12;color:rs;pitch:90
  GColumn: circle;c:0,255,0;twist;part:5;r:0.75;pitch:90;move:0,0.1,0;rc:-0.02
  SmallBoop: circle;effect:flying_glyph;yaw:[playerName];pitch:[playerName];r:0.1;part:3;rc:0.03;mr:0.3;twist
  HologramInteraction: circle;effect:flying_glyph;yaw:[playerName];pitch:[playerName];r:0.1;part:3;rc:0.03;mr:0.3;twist
  HologramNewInteraction: circle;effect:reddust;r:0;part:2;rc:0.2;mr:1;color:rs;yaw:[playerName];a:90
  HologramHover: circle;effect:crit;r:0;part:1;
  TpUp: circle;c:200,50,210;twist;part:5;r:0.5;pitch:90;move:0,0.33,0;offset:0,-0.2,0
  TpDown: circle;c:150,50,10;part:5;r:0.5;pitch:90;move:0,-0.33,0;offset:0,2.2,0
  # From custom1 to custom30 are free to use particle presets which can be utilized for things like command warmups
  custom1: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom2: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom3: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom4: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom5: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom6: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom7: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom8: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom9: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom10: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom11: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom12: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom13: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom14: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom15: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom16: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom17: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom18: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom19: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom20: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom21: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom22: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom23: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom24: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom25: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom26: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom27: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom28: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom29: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
  custom30: circle;effect:reddust;dur:5;pitchc:5;part:10;offset:0,1,0;radius:1;yawc:4
# Defined animated particles will be shown on player teleportation on particular action from place and to destination
# if you don't want it to be shown then set it to empty field
# Animation names should be used from Particles section from above like TpUp
TeleportEffects:
  Unknown:
    From: ''
    To: ''
  Elevator:
    From: ''
    To: ''
  SafeLogin:
    From: ''
    To: ''
  Spawn:
    From: ''
    To: ''
  NetherRoof:
    From: ''
    To: ''
  BelowBedrock:
    From: ''
    To: ''
  Back:
    From: ''
    To: ''
  DBack:
    From: ''
    To: ''
  Home:
    From: ''
    To: ''
  Jump:
    From: ''
    To: ''
  Patrol:
    From: ''
    To: ''
  Portal:
    From: ''
    To: ''
  WarmUp:
    From: ''
    To: ''
  Biome:
    From: ''
    To: ''
  FlightCharge:
    From: ''
    To: ''
  InvEdit:
    From: ''
    To: ''
  TimedCommand:
    From: ''
    To: ''
  TpaAll:
    From: ''
    To: ''
  Tp:
    From: ''
    To: ''
  Top:
    From: ''
    To: ''
  TpAll:
    From: ''
    To: ''
  TpHere:
    From: ''
    To: ''
  TpPos:
    From: ''
    To: ''
  Warp:
    From: ''
    To: ''
  JoinSpawn:
    From: ''
    To: ''
  Totem:
    From: ''
    To: ''
  randomTp:
    From: ''
    To: ''
  World:
    From: ''
    To: ''
  HoloEdit:
    From: ''
    To: ''
PotionEffects:
  # When set to true player poition effect will expire even if player is offline
  # Keep in mind that player potion effect durability will be updated on players login event so by checking players potions effect while he is offline can show incorrect state
  DeductWhileOffline: false

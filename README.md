```# # # # # # # # # # # # # # # # # # # # # # 
#           Made by Wazup92               #
#     If you really like the plugin       #
#     Then please dont forget to leave    #
#        A positive 5 stars review!       #
# # # # # # # # # # # # # # # # # # # # # # 
# Shop chances format is -> 'Chance:Price'
# Shop special blocks format is -> 'ItemID:Durability : <Price>'
# Durability isn't needed.
# --------------------
# Executed commands on Arena-Start -> %world% %arena%
# Achievements format -> 'amount:prize'
# Chat-Modification variables -> %rank% %exp% %coins% and you can have all of them at once
# Karma-Shop format -> 'karma:coins' which refers to how much karma needed to exchange for the coins amount
# Anti Seeker Quit is an option to make it so if the last seeker in a game LEFT the arena, and there are more than or same as x hider, pick a random hider and make them the seeker
# x is replaced with 'Anti-Seeker-Quit-Activation-Hiders-Required'
# If you enable Check-For-General-Notifications, I will be able to send you in-game notifications of events such as plugin sales or important messages.
# These notifications only show once every 6 hours upon joining the server.

Check-For-Updates: true
Check-For-General-Notifications: true
Disguise-Players-As-Blocks: true
Fall-Damage-Enabled: false
Starting-Hider-Chance: 60
Ending-Length: 10
Leap-Cooldown: 12
Leap-Multiplier: 1.8
Update-Block-Behind-Sign: true
Anti-Seeker-Quit: true
Anti-Seeker-Quit-Activation-Hiders-Required: 5
Throwable-Tnt-Cooldown: 15
Disguise-Detector-Cooldown: 60
Seekers-Initial-Spawn-Delay: 20
Seekers-Respawn-Delay: 15
Join-Gui-Enabled: true
Reward-Starting-Seekers: true
Teleport-To-Global-Lobby-On-Leave: false
Display-Arena-State-On-Block: true
Arena-Scoreboard-Enabled: true
Modify-Chat: true
Chat-Modification: '&7[%rank%]'
Spectate-Full-Games: false
Top-Signs-Update-Every: 20
use-UUID: false
use-Vault: false
Karma-Enabled: true
Send-Message-On-Seekers-Release: true
Coins-Earned:
  Hider-Kill-Seeker: 5
  Seeker-Kill-Hider: 3
Exp-Earned:
  Hider-Kill-Seeker:
    Min: 3
    Max: 6
  Seeker-Kill-Hider:
    Min: 2
    Max: 5
Karma-Earned:
  Saying-GG:
    Min: 10
    Max: 20
Coins-Timer:
  Give-Coins-Every-In-Seconds: 45
  Amount: 5
Commands-Executed-On-Winners:
- has coins add %player% 15
Trails:
  enabled: true
  size: 2
  interval: 3
Fireworks:
  Amount-Per-Game: 5
  Given-Coins: 3
  Cooldown: 10
  Delay-In-Between: 3
Sounds:
  onHit:
    enabled: true
Saving-Task:
  Enabled: true
  Save-Every-Minutes: 15
MySQL:
  enabled: false
  table: HideAndSeek
  host: localhost
  port: 3306
  database: database
  username: root
  password: root
Titles:
  player_join:
    enabled: true
    text: '&bYou have joined the game'
  player_leave:
    enabled: true
    text: '&bYou have left the game!'
  achievement_unlock:
    enabled: true
    text: '&aAchievement Unlocked!'
  game_end:
    enabled: true
    text: '&aThanks for playing!'
BungeeMode:
  enabled: false
  voting_enabled: true
  min_players: 3
  lobby_time: 120
  skip_time_at: 5
  skip_time_to: 30
  lock_votes_at: 20
  amount_of_randomised_maps: 5
  hub-name: lobby
  amount_of_games_till_restart: 5
  executed_commands_to_restart:
  - restart
Shop:
  Chances:
  - 80:10000
  - 75:7500
  - 70:5000
  - 65:2500
  - 60:2000
  - 55:2500
  - 50:5000
  - 45:7500
  - 40:10000
  Special_Blocks:
  - 'LAPIS_BLOCK : 1000'
  - 'EMERALD_BLOCK : 1000'
  - 'DIAMOND_BLOCK : 1000'
  - 'REDSTONE_BLOCK : 1000'
  - 'GOLD_BLOCK : 1000'
  - 'COAL_ORE : 1000'
  - 'GOLD_ORE : 1000'
  - 'DIAMOND_ORE : 1000'
  - 'OBSIDIAN : 1000'
  - 'ANVIL : 1000'
  - 'LAPIS_ORE : 1000'
  - 'FURNACE : 1000'
  - 'BEACON : 1000'
  - 'GLOWSTONE : 1000'
  - 'MELON : 1000'
  - 'BEDROCK : 1000'
  - 'MOSSY_COBBLESTONE : 1000'
  - 'SPONGE : 1000'
  - 'HAY_BLOCK : 1000'
  Perks:
    disguise_selector:
      enabled: true
      cost: 3000
      item: 'CHEST : 1 : name:&cDisguise Selector! : lore:&7Allows you to select your
        : lore:&7disguise'
    disguise_changer:
      enabled: true
      cost: 3000
      item: 'CRAFTING_TABLE : 1 : name:&cDisguise Changer! : lore:&7Allows you to
        change your : lore:&7disguise while in game'
    insta_solid:
      enabled: true
      cost: 4000
      item: 'DIAMOND_BLOCK : 1 : name:&cInsta Solid! : lore:&7Instantly become solid'
    disguise_detector:
      enabled: true
      cost: 3000
      item: 'COMPASS : 1 : name:&cDisguise Detector! : lore:&7Right click to detect
        : lore:&7nearby hiders'
    seeker_speed:
      enabled: true
      cost: 2000
      item: 'ENCHANTING_TABLE : 1 : name:&cInfinite Speed I!'
    throwable_tnt:
      enabled: true
      cost: 3000
      item: 'TNT : 1 : name:&cThrowable TNT! : lore:&7Get some tnt that you : lore:&7can
        throw to damage hiders'
  Karma-Shop:
  - 500:100
  - 1000:300
  - 2000:500
Items:
  book:
    enabled: true
  leave:
    enabled: true
    item: 'MAGMA_CREAM : 1 : name:&cQuit'
  inventory_back:
    enabled: true
    item: 'SLIME_BALL : 1 : name:&cBack!'
  shop:
    enabled: true
    item: 'DIAMOND : 1 : name:&bShop'
  vote:
    item: 'BEACON : 1 : name:&bVote!'
  trails:
    item: 'ENCHANTED_BOOK : 1 : name:&eTrails &6[VIP]'
Allowed-Commands:
- hideandseek
- has
- tell
- t
- r
- helpop
Executed-Commands:
  Arena-Countdown:
  - broadcast Arena %arena% is about to start in %seconds% seconds!
  Arena-Start:
  - time set 1000 %world%
Achievements:
  enabled: true
  seekers-killed:
  - 10:100
  - 50:500
  - 100:1000
  - 200:2000
  - 500:6000
  hiders-killed:
  - '10:50'
  - 50:250
  - 100:500
  - 200:1000
  - 500:3000
  win:
  - 1:100
  - 10:500
  - 50:1000
  - 100:3000
  - 200:5000
  games-played:
  - '1:10'
  - '5:30'
  - 20:100
  - 50:300
  - 100:1000
  - 200:3000
  - 500:7000
  purchased-perks:
  - 1:300
  - 3:600
  - 6:2000
Arena-Starting-Warn-At:
- 120
- 90
- 60
- 30
- 15
- 5
- 4
- 3
- 2
- 1
Custom-Maps:
  Winner-Map:
    enabled: true
    texts:
    - Congratulations
    - '   For winning!!!'
    image: https://i.imgur.com/FrgIjmJ.png
  Loser-Map:
    enabled: true
    texts:
    - '  Thank you for'
    - '   Participation!'
    image: ''
Play-Again-Message:
  enabled: true
  header: '&b&m---------&e Hide and Seek &b&m---------'
  content:
  - ' '
  - '          &6Click to play again!'
  - ' '
  footer: '&b&m--------------------------------'

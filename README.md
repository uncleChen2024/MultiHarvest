# MultiHarvest
A feature-rich Minecraft auto-harvest plugin that combines auto-tree chopping and chain mining functionality, providing players with an efficient resource collection experience.
<img width="1536" height="864" alt="主图" src="https://github.com/user-attachments/assets/8fa3b5d2-8c54-4a93-9930-214d0b90e487" />
Plugin Overview
MultiHarvest is a versatile auto-harvest plugin designed for Minecraft servers, primarily offering two core features: auto-tree chopping and chain mining. The plugin supports extensive configuration options, allowing server administrators to flexibly adjust parameters according to their needs, while providing players with an intuitive interface and detailed statistics.
Key Features
1. Auto Tree Chopping

Tool Requirement: Must use an axe to trigger the auto tree chopping feature

Tree Detection: Supports all vanilla tree types, including special trees with branches like acacia

Leaf Handling: Configurable option to automatically clear leaves

Root Detection: Auto tree chopping only triggers when cutting from the bottom of the tree

Drop Collection: All drops are collected near the first broken block

2. Chain Mining

Tool Requirement: Must use a pickaxe to trigger the chain mining feature

Ore Support: Supports all vanilla ores, including deepslate ores and nether ores

Drop Handling: Correctly generates ore drops without resource loss

Drop Collection: All drops are collected near the first broken block

3. Usage Restrictions

Cooldown: Configurable cooldown times for regular players and VIP players

Usage Limits: Daily usage limits with higher limits for VIP players

Permission Control: Supports multiple permission nodes for fine-grained control

World Restrictions: Configure which worlds to enable/disable features (whitelist/blacklist modes)

4. Notification System

Multiple Notification Methods: Supports chat, action bar, and boss bar notifications

Remaining Uses Alert: Shows remaining tree chopping or mining uses

Notification Configuration: Toggle whether to always show notifications

5. Configuration System

Graphical Interface: Intuitive GUI for configuration

Block Configuration: Add or remove block types for auto processing via GUI

World Control: Control feature availability per world via GUI or commands

Multi-language Support: Supports Chinese and English, with extensibility for other languages

6. Statistics System

Usage Statistics: Records number of trees cut and ores mined by players

Block Type Statistics: Detailed counts of each block type broken

Auto-save: Periodically auto-saves statistical data

7. Tool Durability Management

Reduced Consumption: Configurable option to reduce tool durability usage

Consumption Factor: Adjustable ratio for durability consumption

Command System

Basic Commands

/mh - Open main menu

/mh toggle tree - Toggle auto tree chopping

/mh toggle mine - Toggle chain mining

/mh stats - View harvesting statistics

/mh limits - View usage limits

/mh lang <language code> - Switch language (e.g., /mh lang zh_CN or /mh lang en_US)

Admin Commands

/mh reload - Reload configuration

/mh world - Open world control GUI

/mh world list - List all worlds and their status

/mh world toggle <world name> - Toggle feature status for specified world

/mh world mode - Switch between whitelist/blacklist mode

Permission Nodes

Permission Node	Description	Default

multiharvest.use	Basic permission to use the plugin	true

multiharvest.tree	Allow use of auto tree chopping	true

multiharvest.mine	Allow use of chain mining	true

multiharvest.admin	Admin permission to modify configurations	op

multiharvest.vip	VIP permission with shorter cooldowns and higher limits	false

multiharvest.infinitydurability	Unlimited durability - tools won't break	false

multiharvest.unlimited.tree	Unlimited auto tree chopping without daily limits	false

multiharvest.unlimited.mine	Unlimited chain mining without daily limits	false

multiharvest.unlimited.all	Unlimited use of all features without daily limits	false

Configuration Files

config.yml - Main configuration file containing all plugin settings

lang/zh_CN.yml - Chinese language file

lang/en_US.yml - English language file

player_languages.yml - Player language preferences

Technical Information

Compatible Versions

Minimum Version: Minecraft 1.13+

Best Compatibility: Minecraft 1.16 - 1.21

API Dependencies

Bukkit/Spigot API

No NMS code used, improving cross-version compatibility

Special Features

Unicode character support to resolve Chinese garbled text in console

Action bar and boss bar notifications

Custom block type configuration

Support for Nether Update blocks (e.g., CRIMSON_STEM, WARPED_STEM)

Support for deepslate ores (e.g., DEEPSLATE_DIAMOND_ORE)

Support for copper ore (COPPER_ORE)

Installation

Download the latest version of the plugin JAR file

Place the JAR file in your server's plugins folder

Restart the server or use the /reload command (not recommended for production servers)

The plugin will automatically generate default configuration files

Modify configurations as needed, then use /mh reload to load new settings

Screenshots
<img width="1127" height="683" alt="普通玩家界面" src="https://github.com/user-attachments/assets/f99ba299-8b56-4999-87f2-7c1edcd16e5d" />
<img width="1127" height="683" alt="普通玩家界面-禁用" src="https://github.com/user-attachments/assets/581f583d-7ca0-4624-8a29-0ac55c329034" />
<img width="1127" height="683" alt="普通玩家界面-禁用2" src="https://github.com/user-attachments/assets/b4be20ba-3e79-48c2-9212-91123e8534bc" />
<img width="1127" height="683" alt="管理员界面" src="https://github.com/user-attachments/assets/f91b39b8-e351-4c50-b061-db9cdb152bc3" />
<img width="1127" height="683" alt="砍树配置1" src="https://github.com/user-attachments/assets/b4e4fabf-b46d-4a97-808f-8058a93d2a07" />
<img width="1127" height="683" alt="砍树配置2" src="https://github.com/user-attachments/assets/96b6cb4e-d4ff-4406-91e1-4cf4e6520229" />
<img width="1127" height="683" alt="挖矿配置1" src="https://github.com/user-attachments/assets/614ca211-0513-4c20-8b09-9ce897d5e4cd" />
<img width="1127" height="683" alt="挖矿配置2" src="https://github.com/user-attachments/assets/07f83956-2007-4431-b6d0-4509dbad7f11" />
<img width="1127" height="683" alt="挖矿配置3" src="https://github.com/user-attachments/assets/224ed304-fd39-4036-b852-0a4748641ab9" />
<img width="1127" height="683" alt="世界控制" src="https://github.com/user-attachments/assets/90c1fa3f-ccf8-44cc-9c52-018ef663873b" />
<img width="1127" height="683" alt="砍树教程-根部" src="https://github.com/user-attachments/assets/1b454a0b-a679-4699-a8a3-02e727b818a8" />
<img width="1127" height="683" alt="砍树教程-非根部" src="https://github.com/user-attachments/assets/e0cb7a4f-341c-4bb1-8a42-c427fd87e9e5" />
<img width="1127" height="683" alt="次数显示" src="https://github.com/user-attachments/assets/fe5dbded-6c11-4e5c-8549-d1bfb3f3ece9" />

Config List：
'''
# MultiHarvest 插件配置文件
# MultiHarvest Plugin Configuration File

# 语言设置
# Language settings
language:
  default: zh_CN # 默认语言，可选值: zh_CN, en_US
                 # Default language, available options: zh_CN, en_US

# 冷却时间设置（秒）
# Cooldown settings (seconds)
cooldown:
  normal: 5 # 普通玩家冷却时间
            # Cooldown time for regular players
  vip: 2 # VIP玩家冷却时间
         # Cooldown time for VIP players

# 最大处理方块数限制
# Maximum number of blocks processed limit
limits:
  max-tree-blocks: 200 # 单次自动砍树最大处理方块数
                       # Maximum blocks processed in one auto tree chop
  max-ore-blocks: 64 # 单次连锁挖矿最大处理方块数
                     # Maximum blocks processed in one chain mine

# 使用次数限制（每天）
# Usage limits (per day)
usage-limits:
  tree-chop:
    enabled: true # 是否启用次数限制
                  # Whether to enable usage limits
    default: 50 # 默认每天可使用次数
                # Default daily usage count
    vip: 100 # VIP玩家每天可使用次数
             # Daily usage count for VIP players
    notification: # 次数提醒方式
                  # Notification method for remaining counts
      type: ACTION_BAR # 提醒类型：CHAT（聊天框）, ACTION_BAR（动作栏）, BOSS_BAR（Boss栏）
                       # Notification type: CHAT, ACTION_BAR, BOSS_BAR
      always-show: false # 是否总是显示（如果为false，则只在使用功能时显示）
                         # Whether to always show notifications (if false, only show when using the feature)
      boss-bar-color: GREEN # Boss栏颜色（仅在type为BOSS_BAR时有效）：BLUE, GREEN, PINK, PURPLE, RED, WHITE, YELLOW
                            # Boss bar color (only effective if type is BOSS_BAR): BLUE, GREEN, PINK, PURPLE, RED, WHITE, YELLOW
      boss-bar-time: 3 # Boss栏显示时间（秒）
                       # Boss bar display duration (seconds)
  chain-mine:
    enabled: true # 是否启用次数限制
                  # Whether to enable usage limits
    default: 30 # 默认每天可使用次数
                # Default daily usage count
    vip: 60 # VIP玩家每天可使用次数
            # Daily usage count for VIP players
    notification: # 次数提醒方式
                  # Notification method for remaining counts
      type: ACTION_BAR # 提醒类型：CHAT（聊天框）, ACTION_BAR（动作栏）, BOSS_BAR（Boss栏）
                       # Notification type: CHAT, ACTION_BAR, BOSS_BAR
      always-show: false # 是否总是显示（如果为false，则只在使用功能时显示）
                         # Whether to always show notifications (if false, only show when using the feature)
      boss-bar-color: BLUE # Boss栏颜色（仅在type为BOSS_BAR时有效）：BLUE, GREEN, PINK, PURPLE, RED, WHITE, YELLOW
                           # Boss bar color (only effective if type is BOSS_BAR): BLUE, GREEN, PINK, PURPLE, RED, WHITE, YELLOW
      boss-bar-time: 3 # Boss栏显示时间（秒）
                       # Boss bar display duration (seconds)

# 世界设置
# World settings
worlds:
  enabled-worlds:
  - world
  - world_nether
  - world_the_end
  # 如果为true，则只有列表中的世界可以使用功能；如果为false，则列表中的世界不能使用功能
  # If true, only worlds in the list can use the features; if false, worlds in the list cannot use the features
  whitelist-mode: true

# 功能设置
# Feature settings
features:
  tree-chop:
    require-axe: true # 是否需要斧子才能触发自动砍树
                      # Whether an axe is required to trigger auto tree chop
    clear-leaves: true # 是否清理树叶
                       # Whether to clear leaves
    must-chop-bottom: true # 是否必须从树的底部开始砍
                           # Whether to must chop from the bottom of the tree
    collect-drops: true # 是否将掉落物归集到第一个被破坏的方块附近
                        # Whether to collect drops near the first broken block
  chain-mine:
    require-pickaxe: true # 是否需要镐子才能触发连锁挖矿
                          # Whether a pickaxe is required to trigger chain mine
    collect-drops: true # 是否将掉落物归集到第一个被破坏的方块附近
                        # Whether to collect drops near the first broken block

# 方块类型配置
# Block type configuration
blocks:
  # 可自动砍伐的树木方块类型
  # Tree block types that can be auto-chopped
  tree-blocks:
  - JUNGLE_LOG
  - ACACIA_LOG
  - MANGROVE_LOG
  - CHERRY_LOG
  - SPRUCE_LOG
  - CRIMSON_STEM
  - WARPED_STEM
  - OAK_LOG
  - BIRCH_LOG
  - DARK_OAK_LOG
  
  # 树叶方块类型（用于自动砍树时判断）
  # Leaf block types (used for auto tree chop judgment)
  leaf-blocks:
  - JUNGLE_LEAVES
  - CHERRY_LEAVES
  - MANGROVE_LEAVES
  - DARK_OAK_LEAVES
  - WARPED_WART_BLOCK
  - OAK_LEAVES
  - BIRCH_LEAVES
  - SPRUCE_LEAVES
  - NETHER_WART_BLOCK
  - ACACIA_LEAVES
  
  # 可连锁挖掘的矿石方块类型
  # Ore block types that can be chain-mined
  ore-blocks:
  - NETHER_QUARTZ_ORE
  - ANCIENT_DEBRIS
  - DEEPSLATE_DIAMOND_ORE
  - DEEPSLATE_REDSTONE_ORE
  - COAL_ORE
  - DEEPSLATE_GOLD_ORE
  - DEEPSLATE_IRON_ORE
  - IRON_ORE
  - EMERALD_ORE
  - LAPIS_ORE
  - DIAMOND_ORE
  - DEEPSLATE_COPPER_ORE
  - DEEPSLATE_EMERALD_ORE
  - REDSTONE_ORE
  - GOLD_ORE
  - DEEPSLATE_LAPIS_ORE
  - NETHER_GOLD_ORE
  - COPPER_ORE
  - DEEPSLATE_COAL_ORE

# 效果设置
# Effect settings
effects:
  particles: true # 是否显示粒子效果
                  # Whether to show particle effects
  sounds: true # 是否播放音效
               # Whether to play sound effects

# 工具耐久度设置
# Tool durability settings
durability:
  reduced_consumption: true # 是否减少耐久度消耗
                            # Whether to reduce durability consumption
  factor: 0.2 # 耐久度消耗因子，值越小消耗越少
              # Durability consumption factor, smaller value means less consumption

# 统计设置
# Statistics settings
statistics:
  enabled: true # 是否启用统计功能
                # Whether to enable statistics function
  auto_save: true # 是否自动保存统计数据
                  # Whether to auto-save statistical data
  save_interval: 300 # 自动保存间隔（秒）
                     # Auto-save interval (seconds)
'''


License
This plugin is open source under the MIT License. See the LICENSE file for details.
Author
Golden_Dragon
For any questions or suggestions, please submit an issue on GitHub or contact the plugin author.

Tips：If the console fails to display plugin information properly, please add the following code at the beginning of start.bat to ensure correct display:

chcp 65001

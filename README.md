# MultiHarvest

多功能 Minecraft 自动采集插件，整合了自动砍树和连锁挖矿功能，为玩家提供高效的资源收集体验。

A feature-rich Minecraft auto-harvest plugin that combines auto-tree chopping and chain mining functionality, providing players with an efficient resource collection experience.



![MultiHarvest Banner](https://github.com/user-attachments/assets/8fa3b5d2-8c54-4a93-9930-214d0b90e487)

## 插件概述 (Plugin Overview)

MultiHarvest 是一款为 Minecraft 服务器设计的多功能自动采集插件，主要提供自动砍树和连锁挖矿两大核心功能。插件支持丰富的配置选项，允许服务器管理员根据自身需求灵活调整参数，同时为玩家提供直观的操作界面和详细的统计信息。

MultiHarvest is a versatile auto-harvest plugin designed for Minecraft servers, primarily offering two core features: auto-tree chopping and chain mining. The plugin supports extensive configuration options, allowing server administrators to flexibly adjust parameters according to their needs, while providing players with an intuitive interface and detailed statistics.

## 核心功能 (Key Features)

### 1. 自动砍树 (Auto Tree Chopping)



*   **工具要求**：必须使用斧子才能触发自动砍树功能

    **Tool Requirement**: Must use an axe to trigger the auto tree chopping feature

*   **树木检测**：支持所有原版树木类型，包括金合欢树等带分支的特殊树木

    **Tree Detection**: Supports all vanilla tree types, including special trees with branches like acacia

*   **树叶处理**：可配置是否自动清理树叶

    **Leaf Handling**: Configurable option to automatically clear leaves

*   **根部检测**：只有从树的底部开始砍才会触发自动砍树功能

    **Root Detection**: Auto tree chopping only triggers when cutting from the bottom of the tree

*   **掉落物收集**：所有掉落物会被归集到第一个被破坏的方块附近

    **Drop Collection**: All drops are collected near the first broken block

### 2. 连锁挖矿 (Chain Mining)



*   **工具要求**：必须使用镐子才能触发连锁挖矿功能

    **Tool Requirement**: Must use a pickaxe to trigger the chain mining feature

*   **矿石支持**：支持所有原版矿石，包括深层矿石和下界矿石

    **Ore Support**: Supports all vanilla ores, including deepslate ores and nether ores

*   **掉落物处理**：正确生成矿石掉落物，不会丢失资源

    **Drop Handling**: Correctly generates ore drops without resource loss

*   **掉落物收集**：所有掉落物会被归集到第一个被破坏的方块附近

    **Drop Collection**: All drops are collected near the first broken block

### 3. 使用限制 (Usage Restrictions)



*   **冷却时间**：可为普通玩家和 VIP 玩家设置不同的冷却时间

    **Cooldown**: Configurable cooldown times for regular players and VIP players

*   **使用次数**：可限制每日使用次数，VIP 玩家可设置更高的限制

    **Usage Limits**: Daily usage limits with higher limits for VIP players

*   **权限控制**：支持多种权限节点，可精细控制玩家权限

    **Permission Control**: Supports multiple permission nodes for fine-grained control

*   **世界限制**：可配置在哪些世界启用或禁用功能（白名单 / 黑名单模式）

    **World Restrictions**: Configure which worlds to enable/disable features (whitelist/blacklist modes)

### 4. 通知系统 (Notification System)



*   **多种通知方式**：支持聊天框、动作栏和 Boss 栏三种通知方式

    **Multiple Notification Methods**: Supports chat, action bar, and boss bar notifications

*   **剩余次数提醒**：显示玩家剩余的砍树或挖矿次数

    **Remaining Uses Alert**: Shows remaining tree chopping or mining uses

*   **通知配置**：可配置是否总是显示通知

    **Notification Configuration**: Toggle whether to always show notifications

### 5. 配置系统 (Configuration System)



*   **图形界面**：提供直观的 GUI 界面进行配置

    **Graphical Interface**: Intuitive GUI for configuration

*   **方块配置**：可通过 GUI 添加或移除可自动处理的方块类型

    **Block Configuration**: Add or remove block types for auto processing via GUI

*   **世界控制**：可通过 GUI 或命令控制在哪些世界启用功能

    **World Control**: Control feature availability per world via GUI or commands

*   **多语言支持**：支持中文和英文，可扩展其他语言

    **Multi-language Support**: Supports Chinese and English, with extensibility for other languages

### 6. 统计系统 (Statistics System)



*   **使用统计**：记录玩家砍伐的树木和挖掘的矿石数量

    **Usage Statistics**: Records number of trees cut and ores mined by players

*   **方块类型统计**：详细记录每种方块类型的破坏数量

    **Block Type Statistics**: Detailed counts of each block type broken

*   **自动保存**：定期自动保存统计数据

    **Auto-save**: Periodically auto-saves statistical data

### 7. 工具耐久度管理 (Tool Durability Management)



*   **减少消耗**：可配置减少工具耐久度消耗

    **Reduced Consumption**: Configurable option to reduce tool durability usage

*   **消耗因子**：可调整耐久度消耗的比例

    **Consumption Factor**: Adjustable ratio for durability consumption

## 命令系统 (Command System)

### 基本命令 (Basic Commands)



| 命令 (Command)      | 描述 (Description)                                          |
| ----------------- | --------------------------------------------------------- |
| `/mh`             | 打开主菜单 (Open main menu)                                    |
| `/mh toggle tree` | 切换自动砍树功能 (Toggle auto tree chopping)                      |
| `/mh toggle mine` | 切换连锁挖矿功能 (Toggle chain mining)                            |
| `/mh stats`       | 查看采集统计 (View harvesting statistics)                       |
| `/mh limits`      | 查看使用次数限制 (View usage limits)                              |
| `/mh lang <语言代码>` | 切换语言（如`/mh lang zh_CN`或`/mh lang en_US`）(Switch language) |

### 管理员命令 (Admin Commands)



| 命令 (Command)             | 描述 (Description)                                        |
| ------------------------ | ------------------------------------------------------- |
| `/mh reload`             | 重新加载配置 (Reload configuration)                           |
| `/mh world`              | 打开世界控制 GUI (Open world control GUI)                     |
| `/mh world list`         | 列出所有世界及其状态 (List all worlds and their status)           |
| `/mh world toggle <世界名>` | 切换指定世界的功能状态 (Toggle feature status for specified world) |
| `/mh world mode`         | 切换白名单 / 黑名单模式 (Switch between whitelist/blacklist mode) |

## 权限节点 (Permission Nodes)



| 权限节点 (Permission Node)            | 描述 (Description)                                                                   | 默认值 (Default) |
| --------------------------------- | ---------------------------------------------------------------------------------- | ------------- |
| `multiharvest.use`                | 使用插件的基本权限 (Basic permission to use the plugin)                                     | true          |
| `multiharvest.tree`               | 允许使用自动砍树功能 (Allow use of auto tree chopping)                                       | true          |
| `multiharvest.mine`               | 允许使用连锁挖矿功能 (Allow use of chain mining)                                             | true          |
| `multiharvest.admin`              | 管理员权限，可以修改配置 (Admin permission to modify configurations)                           | op            |
| `multiharvest.vip`                | VIP 权限，享有更短的冷却时间和更多的使用次数 (VIP permission with shorter cooldowns and higher limits) | false         |
| `multiharvest.infinitydurability` | 无限耐久度权限，工具不会损坏 (Unlimited durability - tools won't break)                          | false         |
| `multiharvest.unlimited.tree`     | 无限制使用自动砍树功能，不受每日次数限制 (Unlimited auto tree chopping without daily limits)           | false         |
| `multiharvest.unlimited.mine`     | 无限制使用连锁挖矿功能，不受每日次数限制 (Unlimited chain mining without daily limits)                 | false         |
| `multiharvest.unlimited.all`      | 无限制使用所有功能，不受每日次数限制 (Unlimited use of all features without daily limits)            | false         |

## 配置文件 (Configuration Files)



*   `config.yml` - 主配置文件，包含所有插件设置 (Main configuration file containing all plugin settings)

*   `lang/zh_CN.yml` - 中文语言文件 (Chinese language file)

*   `lang/en_US.yml` - 英文语言文件 (English language file)

*   `player_languages.yml` - 玩家语言偏好设置 (Player language preferences)

## 技术信息 (Technical Information)

### 兼容版本 (Compatible Versions)



*   **最低兼容版本**：Minecraft 1.13+ (Minimum Version: Minecraft 1.13+)

*   **最佳兼容版本**：Minecraft 1.16 - 1.21 (Best Compatibility: Minecraft 1.16 - 1.21)

### API 依赖 (API Dependencies)



*   Bukkit/Spigot API

*   未使用 NMS 代码，提高了跨版本兼容性 (No NMS code used, improving cross-version compatibility)

### 特殊功能 (Special Features)



*   支持 Unicode 字符显示，解决控制台中文乱码问题 (Unicode character support to resolve Chinese garbled text in console)

*   支持动作栏和 Boss 栏通知 (Action bar and boss bar notifications)

*   支持自定义方块类型配置 (Custom block type configuration)

*   支持下界更新中添加的方块（如 CRIMSON\_STEM、WARPED\_STEM 等）(Support for Nether Update blocks)

*   支持深层矿石（如 DEEPSLATE\_DIAMOND\_ORE）(Support for deepslate ores)

*   支持铜矿（COPPER\_ORE）(Support for copper ore)

## 安装方法 (Installation)



1.  下载插件的最新版本 JAR 文件 (Download the latest version of the plugin JAR file)

2.  将 JAR 文件放入服务器的`plugins`文件夹中 (Place the JAR file in your server's `plugins` folder)

3.  重启服务器或使用`/reload`命令（不推荐在生产服务器使用）(Restart the server or use the `/reload` command)

4.  插件会自动生成默认配置文件 (The plugin will automatically generate default configuration files)

5.  根据需要修改配置，然后使用`/mh reload`加载新配置 (Modify configurations as needed, then use `/mh reload` to load new settings)

## 截图 (Screenshots)



| 功能 (Feature)                            | 截图 (Screenshot)                                                                                                 |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 玩家界面 (Player Interface)                 | ![Player Interface](https://github.com/user-attachments/assets/f99ba299-8b56-4999-87f2-7c1edcd16e5d)            |
| 玩家界面（禁用状态）(Player Interface (Disabled)) | ![Player Interface (Disabled)](https://github.com/user-attachments/assets/581f583d-7ca0-4624-8a29-0ac55c329034) |
| 管理员界面 (Admin Interface)                 | ![Admin Interface](https://github.com/user-attachments/assets/f91b39b8-e351-4c50-b061-db9cdb152bc3)             |
| 砍树配置 (Tree Chop Configuration)          | ![Tree Chop Configuration](https://github.com/user-attachments/assets/b4e4fabf-b46d-4a97-808f-8058a93d2a07)     |
| 挖矿配置 (Mine Configuration)               | ![Mine Configuration](https://github.com/user-attachments/assets/614ca211-0513-4c20-8b09-9ce897d5e4cd)          |
| 世界控制 (World Control)                    | ![World Control](https://github.com/user-attachments/assets/90c1fa3f-ccf8-44cc-9c52-018ef663873b)               |
| 砍树演示（根部）(Tree Chop Demo (Root))         | ![Tree Chop Demo (Root)](https://github.com/user-attachments/assets/1b454a0b-a679-4699-a8a3-02e727b818a8)       |
| 次数显示 (Usage Limit Display)              | ![Usage Limit Display](https://github.com/user-attachments/assets/fe5dbded-6c11-4e5c-8549-d1bfb3f3ece9)         |

## 配置示例 (Configuration Example)



```
\# MultiHarvest 插件配置文件

\# MultiHarvest Plugin Configuration File

\# 语言设置

\# Language settings

language:

&#x20; default: zh\_CN # 默认语言，可选值: zh\_CN, en\_US

&#x20;                \# Default language, available options: zh\_CN, en\_US

\# 冷却时间设置（秒）

\# Cooldown settings (seconds)

cooldown:

&#x20; normal: 5 # 普通玩家冷却时间

&#x20;           \# Cooldown time for regular players

&#x20; vip: 2 # VIP玩家冷却时间

&#x20;        \# Cooldown time for VIP players

\# 最大处理方块数限制

\# Maximum number of blocks processed limit

limits:

&#x20; max-tree-blocks: 200 # 单次自动砍树最大处理方块数

&#x20;                      \# Maximum blocks processed in one auto tree chop

&#x20; max-ore-blocks: 64 # 单次连锁挖矿最大处理方块数

&#x20;                    \# Maximum blocks processed in one chain mine
```

## 许可证 (License)

本插件基于 MIT 许可证开源。详情请参见 LICENSE 文件。(This plugin is open source under the MIT License. See the LICENSE file for details.)

## 作者 (Author)

Golden\_Dragon

如有任何问题或建议，请在 GitHub 上提交 issue 或联系插件作者。(For any questions or suggestions, please submit an issue on GitHub or contact the plugin author.)

## 提示 (Tips)

如控制台无法正常显示插件信息，请在`start.bat`的开头加上以下代码以正确显示：(If the console fails to display plugin information properly, add the following code at the beginning of `start.bat`:)



```
chcp 65001
```

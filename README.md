# Introduction

以下是一个简单的 Minecraft 打雷提示数据包：

1. 在游戏中创建一个新的文件夹，命名为 `thunder_pack`。

2. 在 `thunder_pack` 文件夹中创建一个新的文本文件，命名为 `pack.mcmeta`。在该文件中输入以下内容：

```json
{
    "pack": {
        "pack_format": 7,
        "description": "Thunder Pack"
    }
}
```
这个文件用于指定数据包的名称和版本等信息。

3. 在 `thunder_pack` 文件夹中创建一个新的文件夹，命名为 `data`。

4.  在 `data` 文件夹中创建一个新的文件夹，命名为 `minecraft`。

这个文件夹用于存放 Minecraft 内置的资源文件。

5. 在 `minecraft` 文件夹中创建一个新的文件夹，命名为 tags。

6. 在 `tags` 文件夹中创建一个新的文件夹，命名为 `functions`。

这个文件夹用于指定执行函数的条件。

7. 在 `functions` 文件夹中创建一个新的文本文件，命名为 `tick.json`。在该文件中输入以下内容：
```json
{
  "values": [
    "thunder_pack:thunder"
  ]
}
```
这个文件用于指定每个游戏刻应该执行的函数。

8. 在 `functions` 文件夹中创建一个新的文本文件，命名为 `thunder.mcfunction`。在该文件中输入以下命令：
```less
tellraw @a [{"text":"打雷了","color":"gold"}]
playsound minecraft:entity.arrow.hit_player master @a
```
这个文件用于指定当打雷时应该执行的命令。第一行命令将会在所有玩家聊天框中发送 "打雷了" 的信息，并且该信息为金色。第二行命令将会给所有玩家播放一个 "箭：击中玩家" 的声音。

9. 保存所有文件。

10. 在 Minecraft 中输入 `/reload`，重新加载数据包。

11. 当游戏中打雷时，所有玩家将会收到 "打雷了" 的信息，并且该信息为金色，并且播放一个 "箭：击中玩家" 的声音。

请注意，此数据包仅能在 Minecraft 1.13 及更高版本中使用。如果您使用较旧版本的 Minecraft，请参考相应版本的 Minecraft 命令语法编写数据包。

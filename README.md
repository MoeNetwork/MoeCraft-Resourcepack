# MoeCraft-Resourcepack
Moecraft Public Resourcepack

本资源包会被实时打包并通过更新器应用于Moecraft客户端。您可以上传自己的图片或乐曲。

### 构建状态

资源包构建状态: ![Build Status](https://dev.azure.com/MoeCraft/ResourcePack/_apis/build/status/MoeNetwork.MoeCraft-Resourcepack?branchName=master)

CDN 构建状态: ![Build Status](https://dev.azure.com/MoeCraft/MoeCraft/_apis/build/status/MoeCraft?branchName=master)


# 如何上传您的资源

## 上传BiblioCraft自定义画

BiblioCraft的自定义画在`assets/bibliocraft/textures/custompaintings/`中，格式为png。文件名不得含有中文。

## 上传自定义音乐（添加）

将文件转换至128kbps的`.ogg`格式，并按照`音乐名.ogg`的格式存储在`assets/minecraft/sounds/目录名/`中，同时在`assets/minecraft/sounds.json`的最后一行末尾加一个半角逗号`,`并在下一行添加如下字段：

`{"目录名.音乐名": {"category": "master", "replace": true, "sounds":[{"name": "目录名/音乐名", "stream": true}]}}`

注：在游戏中播放这些音乐需要OP指令/playsound，命令为`/playsound 目录名.音乐名 播放形式 玩家/选择器 x y z`。如有播放需求请联系OP。

## 上传自定义音乐（更换BGM等声音事件）

请先[至此](https://minecraft-zh.gamepedia.com/Sounds.json#Java.E7.89.88.E6.95.B0.E6.8D.AE.E5.80.BC)找到需要替换的声音事件，将自定义音乐重命名为被替换的声音事件，放在资源包相对被替换的声音事件相同的路径内，同时在`assets/minecraft/sounds.json`的最后一行末尾加一个半角逗号`,`并在下一行添加如下字段：

`{"声音事件": {"category": "种类", "replace": true/false, "sounds":[{"name": "路径", "stream": true/false}]}}`

其中，`replace`为`true`时声音事件会替换预设声音，为`false`时声音事件会被添加到预设声音中；
`stream`仅在`category`为`music` 或`record`时为`true`。

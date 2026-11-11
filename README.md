# RPGSharp

类似`RPG Maker`系列的低代码可视化游戏编辑器。  
程序中表示为`RPGSharp`,本项目亦可叫`RPG#`

## 为什么有本项目 ==> 源于对 RPG Maker Unite 的失望

我朋友一直喜欢玩《重装机兵》,但觉得里面的剧情不完美,并不符合预期。希望有机会能重新塑造一个自己的游戏。而我与他一样,虽觉得游戏结局不完美但也算有趣。直到他后来找到我,希望我们重制《重装机兵》,于是我们先尝试了`RPG Maker MV`,但其编辑器不开源、不免费且插件系统不尽人意,最终导致项目搁浅。后来听说出了`RPG Maker Unite`,于是又尝试了`RPG Maker Unite`并抱有很大期望,但其引擎未能与`Unity`良好结合导致卡顿频频,问题不断,并且Unity后来与Unity中国分家(二次搁浅~)。后来我本科即将毕业,正好需要做一个毕业设计,于是我决定自己写一个类似的游戏编辑器来解决我们的问题,并将 TA 取名为`RPG#`。

## 目前的功能及想法(不排除画饼嫌疑~)

- 引擎构成:基于`Blazor`实现编辑器部分,并输出特定格式文件(可能包含如:JSON/XNB/数据库(sqlite3)或其他IR格式的集合体,参考unitypackage),`MonoGame`提供实现解析这些文件并运行游戏。*项目基于数据驱动。*
- 模块组成:

| 模块名 | 功能 | 备注 |
| ----- | ----- | ----- |
| RPGSharp.Test | 测试用例 | |
| RPGSharp.Standards | 引擎编译阶段扩展 | netstandard2.0 |
| RPGSharp.Bases | 引擎基础支持 | |
| RPGSharp.Entities | 引擎内部的所有实体 | |
| RPGSharp.Repositories | 引擎数据库支持 | Sqlite3 & EFCore |
| RPGSharp.Specs | 引擎内部所必要的抽象与抽象实现 | |
| RPGSharp.Runtime.MonoGame | 基于 MonoGame 实现 | |
| RPGSharp.Runtime.Mod | 游戏运行时模组支持 | (选择性实现) |
| RPGSharp.Runtime | 运行时支持 | |
| RPGSharp.Editor.Plugins | 编辑器插件支持 | (选择性实现)仅支持桌面端 |
| RPGSharp.Editor | 编辑器实现 | 仅支持桌面端 |

- 支持功能:
  - JSON/XNB/数据库数据
  - 插件支持
  - 2D数据
  - 可能会有C#脚本
  - 可能支持javascript脚本,基于[jint](https://github.com/sebastienros/jint)
- 支持平台(请使用最新版本):
  - Windows Only
  - ...
- 支持多人协作模式(或许会有~)
- 基于`dotnet 11`出预览版,`dotnet 12`出正式版`1.0`。`我尽量不摸鱼🐟`

## 注意

`本人本科毕业设计。并不保证后续更新,代码仅供参考`

- 将从零开始提交代码
- [设计、指南](./doc/)其基于[mdBook](https://github.com/rust-lang/mdBook)
- 本项目目前需要 dotnet 11 及以上版本编译
- 目前仅支持中文
- 仅支持 2D
- ...

## 在寻找类似的项目?

- [RPGCreator](https://github.com/Ward727a/RPGCreator)
- [RPGReactor](https://github.com/Psychronic-Games/RPGReactor)

## 开源协议

本项目发布于[Microsoft Public License](https://opensource.org/license/ms-pl-html)协议下,更多信息请参阅[LICENSE](./LICENSE)。项目中所使用的第三方库遵守其各自的许可证,并与本项目兼容。请参阅这些库以获取其所用许可证的详细信息。

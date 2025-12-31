# RPG Sharp

程序中表示为`RPGSharp`但是本项目叫`RPG#`

## 本人本科毕业设计。并不保证后续更新,切勿用在商业项目。在找类似的项目?或许你可以参考[RPGCreator](https://github.com/Ward727a/RPGCreator)

### 为什么有本项目 --- 源于对 RPG Maker Unite 的失望

我朋友一直喜欢玩《重装机兵》,但觉得里面的剧情不完美,并不符合预期。希望有机会能重新塑造一个自己的游戏。而我与他一样,虽觉得游戏结局不完美但也算有趣。直到他后来找到我,希望我们重制《重装机兵》,于是我们先尝试了`RPG Maker MV`,但其编辑器不开源、不免费且插件系统不尽人意,最终导致项目搁浅。后来听说出了`RPG Maker Unite`,于是又尝试了`RPG Maker Unite`并抱有很大期望,但其引擎未能与`Unity`良好结合导致卡顿频频,问题不断(我真是服了)。最终我决定自己写一个类似的游戏编辑器来解决我们的问题,并将 TA 取名为`RPG#`。

### 目前的功能及想法(不排除画饼嫌疑~)

- 引擎构成:使用`Avalonia`提供编辑器部分,并输出JSON/XNB/数据库(sqlite3)格式文件,`MonoGame`提供实现解析这些文件并运行游戏。*项目基于数据驱动。*
- 模块组成:

| 模块名 | 功能 | 备注 |
| ----- | ----- |-----|
| RPGSharp.Test | 测试用例 | |
| RPGSharp.Bases | 引擎基础支持 | netstandard2.0 |
| RPGSharp.Entities | 引擎内部的所有实体 | |
| RPGSharp.Repositories | 引擎数据库支持 | Sqlite3 & EFCore |
| RPGSharp.Specs | 引擎内部所必要的抽象与实现 | |
| RPGSharp.Impls | 基于 MonoGame 实现 | 可自定义实现,用于桌面端预览 |
| RPGSharp.Editor.Uis | Avalonia 实现视图部分 | 支持扩展 |
| RPGSharp.Editor | 编辑器可视化 | 仅支持桌面端 |
| RPGSharp.Runtime | 游戏运行时 | MonoGame 实现 |

- 支持功能:
  - 强大的C#脚本系统!
  - js支持,基于Jint。*你依然可以使用MV/MZ的编程思想,但已经不再推荐了。更推荐C#,或许后续会支持ts :)*
  - JSON/XNB/数据库数据
  - 插件支持
  - 2D数据
  - ...
- 支持平台(请使用最新版本):
  - Windows
  - ...
- 支持多人协作模式(或许会有~)
- 基于`dotnet 11`出预览版,`dotnet 12`出正式版`1.0`。`我尽量不摸鱼🐟`

### 注意

- 将从零开始提交代码
- [设计、指南](./guide/)其基于[docfx](https://github.com/dotnet/docfx)
- 本项目目前需要 dotnet 11 及以上版本编译
- 目前仅支持中文
- 仅支持 2D
- ...

### 开源协议

本项目发布于[Microsoft Public License](https://opensource.org/license/ms-pl-html)协议下,更多信息请参阅[LICENSE](./LICENSE)。项目中所使用的第三方库遵守其各自的许可证,并与本项目兼容。请参阅这些库以获取其所用许可证的详细信息。

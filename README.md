# PCL2 非线上更新 & 可下载版（Non-Online-Update & DownloadAvailable）

基于 [Plain Craft Launcher](https://github.com/Meloong-Git/PCL) 官方开源仓库的自构建分支，针对「遗尘往事」整合包场景做两处调整：

## 改动说明

| 项目 | 官方行为 | 本分支 |
|---|---|---|
| **MC 下载功能** | 按政策移除（`RestrictMcDownload = True`，下载渠道关闭）| **恢复**（`RestrictMcDownload = False`，下载/安装整合包、MC 版本可用）|
| **启动器自动更新** | 正式版存在更新推送 | **无**（基于开源分支，更新功能天然 stub，不会自动更新）|

> 其余身份常量（微软登录 ClientId、注册表分支 `PCL`、遥测 URL）与官方正式版一致，可继承既有登录/设置。

## 构建

工程目标 `.NET Framework 4.8`，需要 VS 2022 MSBuild + net48 参考程序集。仓库内含 `toolchain/`（.NET SDK + ref assemblies，本机构建用，不入 git）。

## 上游

包含 PCL 的大部分源代码，包括 UI 库、动画模块、下载模块、Minecraft 启动模块等！<br/>
代码并不是实时更新的，它会在每次 PCL 发布更新时同步一次。<br/>
非常感谢社区的大力支持！

<br/>

### 相关资源
- [PCL 下载](https://meloong.com/pcl)：下载可免费使用的正式版 PCL！
- [PCL 功能投票](https://github.com/Meloong-Git/PCL/discussions/2)：来参加投票吧，开发者会优先处理票数较高的项目！
- [帮助文档库](https://github.com/LTCatt/PCL2Help)：PCL 内置帮助文档的存储库

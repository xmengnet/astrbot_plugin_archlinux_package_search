# Arch Linux 软件包搜索插件 for AstrBot

该 AstrBot 插件允许用户搜索 Arch Linux 官方仓库和 Arch 用户仓库（AUR）中的软件包。

## 功能

- 按名称搜索 Arch Linux 官方仓库和 AUR 中的软件包。
- 可选指定官方仓库进行搜索。
- 提供软件包的详细信息，包括：
  - 仓库
  - 软件包名称
  - 版本
  - 描述
  - 打包者（官方软件包）/维护者（AUR 软件包）
  - 上游 URL
  - 最后更新日期
  - AUR 链接（AUR 软件包）
  - 投票数（AUR 软件包）
  - 过时状态（AUR 软件包）

## 使用方法

要使用该插件，请向机器人发送以下命令：

```
pkg <软件包名称> [仓库]
```

- `<软件包名称>`：要搜索的软件包名称。
- `[仓库]`（可选）：要搜索的仓库（例如 core、extra、community）。如果不指定，插件将先搜索所有官方仓库，然后搜索 AUR。

示例：

```
pkg linux core
pkg firefox
```

## 依赖项

- aiohttp
- asyncio
- datetime
- json
- astrbot

这些依赖项列在 `requirements.txt` 文件中。

## 安装

1. 安装所需的依赖项：

```bash
pip install -r requirements.txt
```

2. 将插件文件（`main.py`、`metadata.yaml` 等）放置在适当的 AstrBot 插件目录中。

## 配置

无需配置。

## 错误处理

该插件处理各种错误，包括：

- 查询 Arch Linux 仓库或 AUR 时的网络错误。
- 解析 API 响应时的 JSON 解码错误。
- API 响应中的意外数据结构。
- API 响应中的无效时间戳。

错误通过 AstrBot 日志记录器记录。

## 贡献

欢迎贡献！请提交包含错误修复、新功能或文档改进的拉取请求。

## 许可证

该插件根据 AGPL 许可证授权。有关详细信息，请参阅 `LICENSE` 文件。
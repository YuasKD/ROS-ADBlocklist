# RouterOS AdBlock List (Auto-Updated)

本项目利用 **GitHub Actions** 每日自动拉取国际知名的去广告域名列表 (Yoyo AdList)，并将其转换为 RouterOS (ROS) 可直接导入的 `.rsc` 脚本文件。

## ✨ 特性

  * **零负载更新**：所有文本解析、格式转换工作均在 GitHub 云端完成。路由器仅需下载成品文件，**无需**消耗 CPU 循环处理数千行文本。
  * **格式优化**：自动生成 `.rsc` 脚本，将广告域名解析至 `127.0.0.1`。脚本包含 `remove` 旧列表指令，防止规则重复堆积。
  * **数据精准**：上游数据源自老牌的 [pgl.yoyo.org](https://pgl.yoyo.org/adservers/)，体积适中（约 2500+ 条），误杀率极低，非常适合路由器使用。
  * **全自动**：每天北京时间凌晨 **04:00** 自动更新并发布到 GitHub Release (Tag: `rolling`)。

## 📥 下载链接

| 📦 项目 | 📄 文件名 | 🐙 GitHub Release | 🚀 国内加速 (推荐) | 🔧 适用范围 |
| :--- | :--- | :--- | :--- | :--- |
| **ROS AdBlock** | `yoyo_adblock.rsc` | [点我下载]([https://www.google.com/search?q=https://github.com/%3C%E4%BD%A0%E7%9A%84%E7%94%A8%E6%88%B7%E5%90%8D%3E/%3C%E4%BB%93%E5%BA%93%E5%90%8D%3E/releases/download/rolling/yoyo_adblock.rsc](https://github.com/YuasKD/ROS-ADBlocklist/releases/download/rolling/yoyo_adblock.rsc)) | [可疑链接已删除] | RouterOS DNS Static |

## 📥 如何使用

### 方式一：手动导入

1.  进入本项目的 **Releases** 页面。
2.  下载最新的 `yoyo_adblock.rsc` 文件。
3.  打开 WinBox，将文件拖入 **Files** 窗口。
4.  在 Terminal 执行：`/import yoyo_adblock.rsc`。

## 🤝 致谢

  * **核心数据来源**：[Peter Lowe's Adservers](https://pgl.yoyo.org/adservers/) - 感谢维护这份高质量的屏蔽列表。
  * **发布工具**：[softprops/action-gh-release](https://github.com/softprops/action-gh-release)

## 📄 License

本项目遵循 GPL-3.0 开源协议。

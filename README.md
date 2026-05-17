# Loon

自用 Loon 插件与脚本。

当前包含：

- WeTalk 自动化签到 + 视频奖励
- PingMe 自动化签到 + 视频奖励

## 目录结构

```text
Loon
├── JavaScript
│   ├── WeTalk.js
│   └── PingMe.js
└── Plugin
    ├── WeTalk.lpx
    ├── PingMe.lpx
    └── WeTalk_PingMe.lpx
```

## 插件链接

单独使用：

```text
https://raw.githubusercontent.com/KuaiCode/Loon/main/Plugin/WeTalk.lpx
https://raw.githubusercontent.com/KuaiCode/Loon/main/Plugin/PingMe.lpx
```

合并使用：

```text
https://raw.githubusercontent.com/KuaiCode/Loon/main/Plugin/WeTalk_PingMe.lpx
```

## 使用方法

1. 在 Loon 中添加 `.lpx` 插件。
2. 开启插件、重写、MITM，并确认对应 hostname 已启用证书解密。
3. 打开对应 App，进入会触发余额查询的页面。
4. 看到“账号参数已入库 / 账号参数已更新”通知后，说明抓取成功。
5. 后续由 Loon 定时任务自动执行签到和视频奖励。

## 定时任务

| 插件 | 执行时间 |
| --- | --- |
| WeTalk | 每天 08:20、20:20 |
| PingMe | 每天 08:30、20:30 |

## 失效处理

如果出现未抓到账号、登录失效、签到失败等情况：

1. 确认插件和 MITM 已启用；
2. 重新打开 App 触发抓取；
3. 等待通知提示账号参数更新；
4. 手动运行对应签到脚本测试。

## 免责声明

本仓库内容仅供个人学习和自用。使用前请自行确认相关 App 的服务条款和风险。

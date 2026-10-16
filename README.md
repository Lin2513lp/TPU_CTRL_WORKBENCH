# TPU_CTRL 工作台

[打开在线工作台](https://lin2513lp.github.io/TPU_CTRL_WORKBENCH/)

TPU_TOP / TPU_CTRL 设计报告、源码查看、Verdi 仿真波形与设计资料。
当前发布版本：`ctrl-error-logic-20261016`。

- `index.html`：在线首页，独立 HTML，也可下载后离线打开。
- `TPU_CTRL_WORKBENCH.html`：同一工作台的固定文件名入口。
- `code/`：页面内嵌的18份源码与工程文件快照，包含最新 CTRL 错误检测/计数逻辑、寄存器 RTL 和 TB。
- `assets/tpu-system-connections.svg`：可单独打开的系统连接图。
- `source-manifest.json`：本地工作台、发布文件及源码快照的 SHA-256。

在线页面仅将本地系统连接图链接改为相对链接，设计内容、源码、波形与本地最新版一致。
`code/` 是供查阅的快照，包含上下游参考文件，不是完整 TPU 编译工程。

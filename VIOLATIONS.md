# 违规清单 — Sonarr

本版本故意违反 **3** 条审核条目,逐条落地方式如下:

| 条目 | 落地方式 |
|---|---|
| **H6** | compose 使用具名卷而非 `/Volume*/DockerAppData/` 绑定挂载;postrm 不做清理 → 卸载后残留 |
| **H12** | `DEBIAN/postinst` 执行 `apt-get install` / `pip install` / `curl | bash` 等网络操作 |
| **I2** | compose 使用 `privileged: true` |

## 说明

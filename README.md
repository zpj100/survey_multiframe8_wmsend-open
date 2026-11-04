# survey_multiframe8_wmsend-open

**`survey_multiframe8_wmsend` 的版本清单仓库（公开）。**

本仓库**只放版本信息 JSON**，供程序「检查更新」匿名读取。
**不包含任何源码、配置、口令或采集数据。** 源码在私有仓库 `survey_28read485_wmsend`（多帧脚本为其 B 线产品）。

## 文件

| 文件 | 说明 |
|---|---|
| `survey_multiframe8_wmsend.json` | 当前版本、日期、更新说明 |

```json
{
  "name": "survey_multiframe8_wmsend",
  "version": "1.0.2",
  "date": "2026-11-04",
  "tag": "mf8-v1.0.2",
  "notes": "……",
  "files": []
}
```

`version` **不带 `v` 前缀**，与源码里的 `SCRIPT_VERSION` 一致。

## 程序如何读取

按顺序尝试，取版本号最高者与本地 `SCRIPT_VERSION` 比较：

1. `https://gitee.com/zpj100/survey_multiframe8_wmsend-open/raw/master/survey_multiframe8_wmsend.json`
2. `https://raw.giteeusercontent.com/zpj100/survey_multiframe8_wmsend-open/raw/master/survey_multiframe8_wmsend.json`
3. jsdelivr CDN（`fastly` / 普通）
4. Gitee Releases API
5. `https://raw.githubusercontent.com/zpj100/survey_multiframe8_wmsend-open/master/survey_multiframe8_wmsend.json`
6. GitHub Releases API

## 发版时怎么改

只改 `survey_multiframe8_wmsend.json` 的 `version` / `date` / `tag` / `notes`，提交推到 master 即可。

## 版本历史

| 版本 | 日期 | 主要变化 |
|---|---|---|
| 1.0.2 | 2026-11-04 | 取消保持状态（无新值即 0.000，状态列「无新值」）；修复 MQTT `NoneType.publish` 崩溃；新增「最后收数」诊断 |
| 1.0.1 | 2026-11-03 | MQTT 按需短连接；client_id 改 `wavemesh-3322-mf8`（修复与 28 路同机 1 秒互踢） |
| 1.0.0 | 2026-11-03 | 8 × 224 子帧 / 32 路解析；8 线程同步解析；数据库上传开关 |

## 关联仓库

| 用途 | Gitee | GitHub |
|---|---|---|
| 私有源码 | <https://gitee.com/zpj100/survey_28read485_wmsend> | <https://github.com/zpj100/survey_28read485_wmsend> |
| 版本清单（本仓） | <https://gitee.com/zpj100/survey_multiframe8_wmsend-open> | <https://github.com/zpj100/survey_multiframe8_wmsend-open> |
| 28 路清单（A 线） | <https://gitee.com/zpj100/survey_28read485_wmsend-open> | <https://github.com/zpj100/survey_28read485_wmsend-open> |

# 拍拍小怪兽（等你来）· 建模文件

本仓库收录桌面求助器的 3D 打印模型、STL、Python 生成源码、装配说明与网格检查。**下载 3MF 后可直接用 Bambu Studio 打开**；所有尺寸单位为毫米，不含 G-code、APP、固件、手机数据或打印机凭据。

## 优先选择最新版

| 文件 | 内容 | 使用说明 |
| --- | --- | --- |
| [01-enclosure-v3-wide-two-parts.3mf](01-enclosure-v3-wide-two-parts.3mf) | **V3 加宽方形主体 + 匹配后盖** | 主壳名义宽 98 mm；后检修口 80×56 mm；保留原插线口。通用模型，按实际设备切片。 |
| [10-esp32-holder-open-sides-v2-generic.3mf](10-esp32-holder-open-sides-v2-generic.3mf) | **ESP32 托底 V2：无螺丝、双侧开放走线** | 参考板 52×28 mm；凹槽 52.6×28.6 mm；两长边及底部各让出走线通道。通用模型。 |
| [11-esp32-holder-open-sides-v2-Bambu.3mf](11-esp32-holder-open-sides-v2-Bambu.3mf) | 同上，Bambu 模型工程 | 打印前重选实际打印机、喷嘴和耗材，再切片；含模型工程设置，没有打印任务或凭据。 |
| [05-button-support-roomier-13-parts-generic.3mf](05-button-support-roomier-13-parts-generic.3mf) | **加大按钮小底托 + 12 件可调承托柱** | 凹槽 31.6×21.6 mm；13 件已排在同一盘；通用模型。 |
| [04-button-support-roomier-13-parts-P2S-0.4.3mf](04-button-support-roomier-13-parts-P2S-0.4.3mf) | 同上，P2S 0.4 mm Bambu 工程 | 换机时重选实际配置并切片。 |
| [07-black-pupils-two.3mf](07-black-pupils-two.3mf) | 两只黑眼珠 | Bambu 保存模型，打印前重选实际配置。 |
| [08-black-smile.3mf](08-black-smile.3mf) | 黑色笑嘴 | 通用模型。 |
| [06-adjustable-support-12-parts-generic.3mf](06-adjustable-support-12-parts-generic.3mf) | 单独 12 件可调承托柱 | 不含按钮小底托；支承高度 10–60 mm，另有垫片。 |

**绿色头顶按钮帽 STL** 在 [07-original-interface-and-pupils.zip](07-original-interface-and-pupils.zip) 中。V3 沿用原按钮帽、眼珠与笑嘴接口。V3 顶棚和按钮导向结构需在切片预览中核对支撑。

ESP32 托底与按钮小底托是两个零件。新 ESP32 托底四个短柱仅用于定位，没有卡扣；接头若从底下伸出，主壳内部仍需另留高度，不能把托底压在接头上。

## 历史版本参考

| 文件 | 内容 |
| --- | --- |
| [02-esp32-holder-with-fasteners.3mf](02-esp32-holder-with-fasteners.3mf) | 旧 ESP32 托座 + 2 螺丝 + 2 压片；最新无螺丝版见上方。 |
| [03-button-holder-with-fasteners.3mf](03-button-holder-with-fasteners.3mf) | 原尺寸按钮托座，凹槽 30.6×20.6 mm，带螺丝与压片。 |
| [09-enclosure-v2-reference-two-parts.3mf](09-enclosure-v2-reference-two-parts.3mf) | 旧 V2 主体与后盖；不能和 V3 后盖混用。 |

## 分类 ZIP：STL、源码和说明

| 压缩包 | 内容 |
| --- | --- |
| [00-models-instructions-and-build-tools.zip](00-models-instructions-and-build-tools.zip) | 完整模型 README、清单、复建顺序、依赖、解压及辅助脚本。 |
| [01-enclosure-v3-wide-source-and-stl.zip](01-enclosure-v3-wide-source-and-stl.zip) | 最新 V3 主体/后盖 STL、生成源码、检查与真实网格预览。 |
| [08-esp32-holder-open-sides-v2-source-and-stl.zip](08-esp32-holder-open-sides-v2-source-and-stl.zip) | **最新无螺丝双侧走线 ESP32 托底**的 STL、源码、说明、预览与检查。 |
| [03-adjustable-support-and-roomier-tray.zip](03-adjustable-support-and-roomier-tray.zip) | 轻量承托柱、加大按钮底托的 STL、源码、说明与检查。 |
| [07-original-interface-and-pupils.zip](07-original-interface-and-pupils.zip) | **绿色按钮帽 STL**、眼珠 STL/源码与原始几何生成工具。 |
| [06-black-smile-source-and-stl.zip](06-black-smile-source-and-stl.zip) | 笑嘴 STL、源码和实际网格装配预览。 |
| [02-board-holders-and-fasteners.zip](02-board-holders-and-fasteners.zip) | 历史 ESP32/按钮托座、自定义打印螺丝、压片。 |
| [04-enclosure-v2-reference-source.zip](04-enclosure-v2-reference-source.zip) | V2 源码与说明，供历史工程复建。 |
| [05-four-plate-rebuild-source.zip](05-four-plate-rebuild-source.zip) | 旧 V2 四盘工程的复建源码。 |

ZIP 内路径全部从 `models/` 开始；解压到同一个位置即可合并目录。ZIP 不重复存放直接展示的 11 个 3MF。两件大 STL 使用无损 `.stl.gz`，还原后可运行 `python3 models/extract_stl.py` 解压。全部单文件小于 25 MB。

## 一次恢复完整目录

将本页全部文件下载到同一个文件夹，运行：

```bash
python3 restore_models.py
```

脚本先校验平铺文件哈希，再合并全部 ZIP、恢复 11 个 3MF 到原路径，最后逐件校验完整 **90 个模型文件**。已有文件内容不一致时停止，不会直接覆盖。也可用 `--output 路径` 指定还原位置；之后打开 `models/README.md` 阅读详细说明。

[model-file-map.json](model-file-map.json) 记录公开 3MF 的原路径；[models-manifest.json](models-manifest.json) 是完整模型目录的逐件 SHA-256 清单；[web-manifest.json](web-manifest.json) 是本页平铺交付清单。

本包保留数字网格检查证据；实际板厚、焊点、接头、按钮触发与回弹、打印收缩及承托稳定性仍需实物核对。打印螺丝为自定义螺纹，不是标准 M3/M6。当前外壳没有扬声器孔或安装座。

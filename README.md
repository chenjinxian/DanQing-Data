# DanQing-Data — DanQing 演示数据包 / Demo data packages

[中文](#中文) | [English](#english)

## English

Prebuilt tile-capture data packages ("rpc-dumps") for the
[DanQing](https://github.com/chenjinxian/DanQing) graphics-engine demo app.
Download from the **[data-v1 release](../../releases/tag/data-v1)** assets.

| Package | Model | Raw size | Package |
|---|---|---|---|
| `DanQing-Data-v1-joeshouse.zip` | Joe's House (10-tree residence, 173,931 tiles) | 353 MB | 173 MB |
| `DanQing-Data-v1-housemodel.zip` | House_Model (textured house, 106,719 tiles) | 579 MB | 242 MB |
| `DanQing-Data-v1-baytown.zip` | Baytown (OpenPlant process plant, 81,329 tiles) | 849 MB | 334 MB |
| `DanQing-Data-v1-instances60.zip` | 60 Instances (instancing showcase, 3,595 tiles) | 305 MB | 135 MB |
| `DanQing-Data-v1-bridge-edit-base.zip` | Bridge Edit (1.5 km bridge — base views) | 660 MB | 199 MB |
| `DanQing-Data-v1-bridge-edit-sweep-part1..3of3.zip` | Bridge Edit full-tree sweep (380,738 tiles; extract all three parts into the same folder) | 5.1 GB | 1.8 GB total |

**Usage**

- Repo clone: run `powershell -ExecutionPolicy Bypass -File scripts/data/download_dumps.ps1`
  from a DanQing checkout — it downloads, sha256-verifies, and extracts into
  `third_party/tile-sample-assets/rpc-dumps/` (`-Model instances60` for a single model).
- Prebuilt app package: extract the zips into `data\rpc-dumps\` next to `run.cmd`.

Integrity: sha256 per asset in [checksums.md](checksums.md) (also embedded in the
download script's manifest). Provenance: these are tile captures of itwinjs
(MIT-licensed) sample iModels recorded through itwinjs display-test-app; per-root
details live in the main repo's `third_party/tile-sample-assets/rpc-dumps/README.md`.
Provided for demo and testing purposes.

## 中文

[DanQing](https://github.com/chenjinxian/DanQing) 图形引擎示例程序的瓦采集
数据包（"rpc-dumps"）。从 **[data-v1 release](../../releases/tag/data-v1)**
资产区下载。

| 包 | 模型 | 原始体量 | 包体 |
|---|---|---|---|
| `DanQing-Data-v1-joeshouse.zip` | Joe's House（10 树住宅，173,931 瓦） | 353 MB | 173 MB |
| `DanQing-Data-v1-housemodel.zip` | House_Model（纹理住宅，106,719 瓦） | 579 MB | 242 MB |
| `DanQing-Data-v1-baytown.zip` | Baytown（OpenPlant 工艺厂，81,329 瓦） | 849 MB | 334 MB |
| `DanQing-Data-v1-instances60.zip` | 60 Instances（实例化演示，3,595 瓦） | 305 MB | 135 MB |
| `DanQing-Data-v1-bridge-edit-base.zip` | Bridge Edit（1.5km 桥梁——基础视图） | 660 MB | 199 MB |
| `DanQing-Data-v1-bridge-edit-sweep-part1..3of3.zip` | Bridge Edit 全树 sweep（380,738 瓦；三段解压到同一目录叠加） | 5.1 GB | 共 1.8 GB |

**用法**

- 源码仓：在 DanQing 检出根运行
  `powershell -ExecutionPolicy Bypass -File scripts/data/download_dumps.ps1`——
  自动下载、sha256 校验、解包到 `third_party/tile-sample-assets/rpc-dumps/`
  （`-Model instances60` 单取一个模型）。
- 预编译包：解压到 `run.cmd` 旁的 `data\rpc-dumps\`。

完整性：每资产 sha256 见 [checksums.md](checksums.md)（下载脚本 manifest 内嵌
同款）。数据渊源：itwinjs（MIT）示例 iModel 经 itwinjs display-test-app 采集的
瓦数据；逐根明细见主仓 `third_party/tile-sample-assets/rpc-dumps/README.md`。
仅供演示与测试用途。

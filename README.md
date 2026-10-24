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
| `DanQing-Data-v1-newbridge-v1.zip` | New Bridge (10 km bridge — base manifests) | — | <1 MB |
| `DanQing-Data-v1-newbridge-sweep-v1-part1..12of12.zip` | New Bridge sweep (d1–d8, 5,407 tiles — the browsing core; extract all twelve parts into the same folder) | 20.5 GB | 6.4 GB total |
| `DanQing-Data-v1-newbridge-d9-v1.zip` + `d9b` | New Bridge d9 layers | 2.2 GB | 0.7 GB |
| `DanQing-Data-v1-newbridge-d10-v1-part1..4of4.zip` | New Bridge d10 (19,910 tiles) | 5.7 GB | 1.9 GB |
| `DanQing-Data-v1-newbridge-d11-v1-part1..4of4.zip` | New Bridge d11 (43,986 tiles) | 6.9 GB | 2.4 GB |
| `DanQing-Data-v1-newbridge-d12-v1-part1..4of4.zip` | New Bridge d12 (56,859 tiles) | 7.0 GB | 2.5 GB |
| `DanQing-Data-v1-newbridge-d13-v1-part1..3of3.zip` | New Bridge d13 (41,657 tiles — deepest published layer) | 5.2 GB | 1.9 GB |

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

### Git channel (this repo's working tree — no extraction needed)

The same data also lives in this repo's git tree, root-layout identical to the
main repo's `rpc-dumps/`:

```bash
git clone git@github.com:chenjinxian/DanQing-Data.git   # SSH — works without a proxy
# then point the demo app at it:
#   set DANQING_RPC_DUMP=<clone dir>        (or extract into the prebuilt package's data\rpc-dumps)
```

Two differences vs. the release zips (GitHub 100 MB/file limit):

- `bridge-edit-sweep-v1/files/12.imdl` (134 MB) is **absent** — the engine's
  parent-LOD fallback covers it; the release zip `sweep-part1of3` contains it.
- `bridge-edit-sweep-v1/manifest.json` is a **compact form** (145.6 → 37.2 MB;
  per-tile guid/iModelId/changesetId/sha256 dropped — the engine reads
  treeId/contentId/byteLength/file only). The byte-exact original ships in the
  release zip `sweep-part1of3` and as LFS in the main repo.
- **New Bridge is release-only** (not in this git tree): dozens of tiles exceed
  100 MB (up to 316 MB), 47.5 GB total.

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
| `DanQing-Data-v1-newbridge-v1.zip` | New Bridge（10km 大桥——基础 manifests） | — | <1 MB |
| `DanQing-Data-v1-newbridge-sweep-v1-part1..12of12.zip` | New Bridge sweep（d1–d8，5,408 瓦——浏览核心；十二段解压到同一目录叠加） | 20.5 GB | 共 6.4 GB |
| `DanQing-Data-v1-newbridge-d9-v1.zip` + `d9b` | New Bridge d9 层 | 2.2 GB | 0.7 GB |
| `DanQing-Data-v1-newbridge-d10-v1-part1..4of4.zip` | New Bridge d10（19,910 瓦） | 5.7 GB | 1.9 GB |
| `DanQing-Data-v1-newbridge-d11-v1-part1..4of4.zip` | New Bridge d11（43,986 瓦） | 6.9 GB | 2.4 GB |
| `DanQing-Data-v1-newbridge-d12-v1-part1..4of4.zip` | New Bridge d12（56,859 瓦） | 7.0 GB | 2.5 GB |
| `DanQing-Data-v1-newbridge-d13-v1-part1..3of3.zip` | New Bridge d13（41,657 瓦——最深发布层） | 5.2 GB | 1.9 GB |

**用法**

- 源码仓：在 DanQing 检出根运行
  `powershell -ExecutionPolicy Bypass -File scripts/data/download_dumps.ps1`——
  自动下载、sha256 校验、解包到 `third_party/tile-sample-assets/rpc-dumps/`
  （`-Model instances60` 单取一个模型）。
- 预编译包：解压到 `run.cmd` 旁的 `data\rpc-dumps\`。

### Git 通道（本仓工作树——免解压）

同一份完整数据也在本仓 git 树里，目录布局与主仓 `rpc-dumps/` 一致：

```bash
git clone git@github.com:chenjinxian/DanQing-Data.git   # SSH——免代理可用
# 然后让示例程序指向它：
#   set DANQING_RPC_DUMP=<克隆目录>      （或把内容放进预编译包的 data\rpc-dumps）
```

与 release zip 的两点差异（GitHub 单文件 100MB 硬门所致）：

- `bridge-edit-sweep-v1/files/12.imdl`（134MB）**缺席**——引擎父瓦 LOD 兜底
  覆盖；release zip `sweep-part1of3` 内含该瓦。
- `bridge-edit-sweep-v1/manifest.json` 为**紧凑形**（145.6→37.2MB；逐瓦
  guid/iModelId/changesetId/sha256 字段删减——引擎只读
  treeId/contentId/byteLength/file）。字节级原件在 release zip
  `sweep-part1of3` 与主仓 LFS。
- **New Bridge 仅走 release**（不在本 git 树）：数十个瓦超 100MB（最大
  316MB），总量 47.5GB。

完整性：每资产 sha256 见 [checksums.md](checksums.md)（下载脚本 manifest 内嵌
同款）。数据渊源：itwinjs（MIT）示例 iModel 经 itwinjs display-test-app 采集的
瓦数据；逐根明细见主仓 `third_party/tile-sample-assets/rpc-dumps/README.md`。
仅供演示与测试用途。

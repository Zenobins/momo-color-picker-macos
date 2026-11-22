# Momo Color Picker 1.1.0 (macOS)

macOS 版（非官方 fork），面向 Krita 5.3.x + macOS（Apple Silicon / arm64）。

## 这个包是什么

- 插件源码与上游 1.1.0 一致，**业务逻辑未改动**
- 内置 `numpy 2.3.0`（`cp313` / `macosx_11_0_arm64`），与 Krita 5.3.4 内嵌的 Python 3.13 匹配
- 附带 `install_macos.sh`：自动定位 `krita.app`，安装到 `~/Library/Application Support/krita`，并把包内 numpy 换成 macOS wheel

## 安装

1. 解压 zip
2. 运行 `./install_macos.sh`
3. 启动 Krita → **设置 → 配置 Krita → Python 插件管理器**，勾选「馍馍拾色器」
4. 重启 Krita → **设置 → 面板列表 → 馍馍拾色器**，或按 `Shift+B`

卸载：`./install_macos.sh --uninstall`

## 兼容性

- Krita **5.3.x** + macOS **arm64**（实测：macOS 15.8 + Krita 5.3.4.1）
- Intel Mac：`FORCE_PLATFORM=macosx_10_9_x86_64 ./install_macos.sh`（Krita 需以 Rosetta 运行，未实测）
- Krita 6（Qt6 / PyQt6）未适配

## 链接

- 上游源码：<https://github.com/zmom0/momo-color-picker>
- 本仓库：<https://github.com/Zenobins/momo-color-picker-macos>

## English

macOS build (unofficial fork) for Krita 5.3.x on Apple Silicon. Plugin sources are identical to upstream 1.1.0; the package bundles `numpy 2.3.0` (`cp313` / `macosx_11_0_arm64`) and ships `install_macos.sh`, which installs into `~/Library/Application Support/krita` and swaps in the macOS numpy wheel. Tested on macOS 15.8 + Krita 5.3.4.1.

# 自定义枪械永续MC包构建工具 | CGC Minecraft Pack Build Kit

[中文](#自定义枪械永续MC包构建工具) | [English](#cgc-minecraft-pack-build-kit)

# 自定义枪械永续MC包构建工具

## 介绍

[自定义枪械永续](https://github.com/XColorful/Custom-Gun-Continued)的 Minecraft 枪包构建工具，一键构建兼容多个 Minecraft 版本的枪包（`.jar 模组`/`数据包`/`资源包`）。

## 使用说明

### ⭐准备Java环境（1️⃣/3）

- 本工具使用 Java 17 进行构建，请确保本地已安装 Java 17

> 可以使用以下命令检查 Java 版本：
> ```shell
> java --version
> ```

### ⭐初始配置（2️⃣/3）

1. 配置`gradle.properties`：
	- 根据文件中的注释修改相关配置
2. 修改命名空间：
	- 将`assets/example`、`data/example`分别重命名为`assets/{namespace}`和`data/{namespace}`

### ⭐构建方式（3️⃣/3）

任选以下一种方式：
- 在 Windows 下运行`build.cmd`
- 或者，在 Intellij IDEA 中用 JDK 17 执行 Gradle 的 `build` 任务

构建产物将输出至`build/libs`：
- `{file_name}.jar`：模组（同时包含数据包+资源包）
- `{file_name}-datapack.zip`：数据包
- `{file_name}-resourcepack.zip`：资源包

## 从旧格式迁移

1. 将`assets/{namespace}/gunpack_info.json`移至`assets/{namespace}/cgc_info/gunpack_info.json`
2. 将`gunpack.meta.json`移至`data/{namespace}/cgc_meta/gunpack.meta.json`

# CGC Minecraft Pack Build Kit

## Introduction

A build tool for [Custom Gun Continued](https://github.com/XColorful/Custom-Gun-Continued) that lets you build gun packs (`.jar mod`/`data pack`/`resource pack`) compatible with multiple Minecraft versions.

## Usage

### ⭐ Set Up Java (1️⃣/3)

- This tool requires Java 17 for building. Make sure Java 17 is installed on your system.

> Run the following command to check your Java version:
> ```shell
> java --version
> ```

### ⭐ Configure the Project (2️⃣/3)

1. Configure `gradle.properties`:
	- Adjust the settings according to the comments in the file.
2. Set the namespace:
	- Rename `assets/example` and `data/example` to `assets/{namespace}` and `data/{namespace}`, respectively.

### ⭐ Build the Pack (3️⃣/3)

Choose either of the following methods:
- Run `build.cmd` on Windows.
- Alternatively, open the project in IntelliJ IDEA and run the Gradle `build` task using JDK 17.

Build artifacts will be generated in `build/libs`:
- `{file_name}.jar`: Mod (includes both the data pack and resource pack).
- `{file_name}-datapack.zip`: Data pack.
- `{file_name}-resourcepack.zip`: Resource pack.

## Migrating from the Legacy Format

1. Move `assets/{namespace}/gunpack_info.json` to `assets/{namespace}/cgc_info/gunpack_info.json`.
2. Move `gunpack.meta.json` to `data/{namespace}/cgc_meta/gunpack.meta.json`.

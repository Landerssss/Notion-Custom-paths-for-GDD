# Notion-Custom-paths-for-GDD
# Notion Custom Installation Guide for Windows
# Windows版 Notion 自定义路径安装指南

> **Status:** Working as of 2025
> **OS:** Windows 10 / 11

## 🧐 Why / 为什么搞这个？

As a developer (or just a tidy person), installing software into the default deep `AppData` directory is unacceptable because:
作为一个开发者（或者单纯有强迫症的人），把软件默认装进深不见底的 `AppData` 目录是不可接受的，原因如下：

1.  **Unsightly (不雅观)**: My C drive is for the OS, not for user apps cluttering up the hidden folders. (C盘是留给系统的，不是藏污纳垢的地方)
2.  **Disk Space (体积膨胀)**: Notion caches a lot of data. Over time, it eats up C drive space aggressively. (Notion 缓存极大，时间久了C盘会被吃干抹净)
3.  **No Choice (没得选)**: The official installer acts like a silent script—no "Browse" button, no respect. (官方安装包根本不给你“浏览”选路径的机会，双击即装，毫无尊严)

---

## 🚀 Method : The CMD Argument
## 方法：命令行参数法

This method uses the standard NSIS installer argument to force a destination path.
利用安装程序的标准参数强制指定解压路径。

### Steps / 步骤

1.  **Download**: Get the latest installer from [Notion Official Site](https://www.notion.so/desktop).
    *   下载最新的安装包。
2.  **Locate**: Move the `.exe` file to a folder (e.g., `D:\Downloads`).
    *   把安装包放到一个文件夹里。
3.  **Open CMD**: Click the address bar of that folder, type `cmd`, and hit `Enter`.
    *   在文件夹地址栏输入 `cmd` 并回车，直接在当前目录打开终端。
4.  **Execute**: Run the following command (replace the version name with yours):
    *   输入以下指令（注意替换你的文件名）：

```bash
# Syntax: "InstallerName.exe" /D=TargetDir
# 语法："安装包名.exe" /D=目标路径

"Notion Setup 3.0.0.exe" /D=D:\Notion

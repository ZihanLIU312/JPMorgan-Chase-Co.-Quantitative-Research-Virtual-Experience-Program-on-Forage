# 在自己的 Windows 电脑上安装 C++ 开发环境

需要装两样东西:编辑器(VS Code)和编译器(g++)。

## 1. 安装 VS Code

从 [code.visualstudio.com](https://code.visualstudio.com) 下载并安装。安装时保持勾选 **"Add to PATH"**,这样命令行里才能用 `code` 命令。

## 2. 安装 MSYS2

从 [msys2.org](https://www.msys2.org) 下载安装包,按默认路径 `C:\msys64` 安装。它是用来在 Windows 上获取 g++ 的工具。

## 3. 安装 g++

打开开始菜单里的 **"MSYS2 UCRT64"**,输入下面的命令,提示时按 `Y` 确认:

```
pacman -S mingw-w64-ucrt-x86_64-gcc
```

## 4. 添加到 PATH

1. 在 Windows 搜索框输入 **"环境变量"**,打开 **"编辑账户的环境变量"**。
2. 选中 `Path`,点 **"编辑"**。
3. 点 **"新建"**,填入:

   ```
   C:\msys64\ucrt64\bin
   ```

4. 一路点 **"确定"** 保存。

## 5. 验证

新开一个 Command Prompt(必须是新开的,旧窗口不会读到新的 PATH),输入:

```
g++ --version
```

能显示版本号就说明装好了。

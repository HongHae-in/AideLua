# Aide Lua
![icon](https://github.com/HongHae-in/AideLua/blob/9f4c682854f3d72cfb7e879fd2a9695f71e88726/ic_cover-aidelua.png)

## 简介
Aide Lua 是一款依赖 Aide 的 Lua 编辑器

## 下载
[![Download the app](https://img.shields.io/github/v/release/HongHae-in/AideLua?label=Download%20app&color=2563eb)](https://github.com/HongHae-in/AideLua/releases/latest)
## 使用须知
1. 本软件默认开启自动保存代码且无法关闭（自动保存触发条件：切换到其他应用、点击二次打包以及打包运行、打开其他文件、关闭文件、打开侧滑（大屏除外）、点击标签栏等）

2. 此软件不能用来开发大型项目

3. 此软件必须搭配编译器，不管你用的是真正的Gradle还是仿Gradle（AIDE属于仿Gradle）

## 使用教程


### 一、配置AIDE
  1. 进入“设置-高级设置-工程相关”

  2. 关闭“启用alert调试文件”，打开“重定义Apk构建路径”

  3. 重启AIDE

### 二、初次打包
  1. 在AideLua点击新建项目，在填写与选择完成后点击“新建”

  2. 用AIDE打开项目，点击“构建刷新”

  3. 点击AideLua的“打包运行”按钮（或“二次打包”，手动签名）并安装，测试是否可以正常打包

  4. 点击AideLua的“运行”按钮，测试是否正常通过已安装的应用调试

## 注意事项
1. AIDE必须使用AIDE高级设置版本，否则无法打开重定义Apk路径

2. AIDE必须打开重定义Apk路径，否则会导致APK混乱

3. AIDE最好关闭adrt调试文件

4. 不是必须用AIDE编译，只不过用AIDE编译会更好一些

## 高级玩法
.aidelua/config.lua用法
| 键(key) | 类型 | 推荐值（[...]为已省略或自定义的内容） | 默认值 | 说明 |
| ---- | ---- | ---- | ---- | ---- |
| tool | table | {[...]} | {} | 二次打包工具信息 |
| tool.version | string | "1.1" | "1.0" | 二次打包工具的版本号 |
| appName | string | / | / | 应用名（仅供AideLua显示） |
| packageName | string | / | / | 应用包名（仅供AideLua显示和更好的调试） |
| debugActivity | string | / | "com.androlua.LuaActivity" | 调试的Activity名(不是标签)（仅供AideLua更好的调试） |
| include | table | {"project:app",[...]"project:androlua"} | / | 要编译lua的库，第一个为主程序 |
| main (已废除) | string | "app" | "app" | 主程序（仅1.0版本） |
| compileLua | boolean | true | true | 编译Lua |
| icon | table/string | {[...]} | / (智能判断) | 项目图标配置（仅供AideLua显示，相对路径为项目路径） |
| icon.day | string | "ic_launcher-aidelua.png" | / (智能判断) | 亮色模式图标 |
| icon.night | string | "ic_launcher_night-aidelua.png" | / (智能判断) | 深色模式图标 |


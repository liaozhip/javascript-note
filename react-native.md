# React-Native

## 创建一个 typescript 项目

`npx react-native init projectName --template react-native-template-typescript`

## 如何修复第三方插件等的问题

- 查看是否有更新的测试版或者未发布版本
- fork
  - 自己修改后发布，或者直接安装github地址
  - 可以向原作者贡献补丁
- patch-package
  - 如果是修改原生第三方，先生成补丁，在编译
- 用yarn resolutions修复间接依赖

## 如何设置 APP 名称、图标和启动页

### 1. APP 名称

#### Android

- 编辑 `android/app/src/main/res/values/strings.xml` 文件。
```xml
<resources>
-    <string name="app_name">oldName</string>
+    <string name="app_name">newName</string>
</resources>
```

#### IOS

- 编辑 `ios/projectName/Info.plist` 文件。
```plist
  <key>CFBundleDisplayName</key>
- <string>oldName</string>
+ <string>newName</string>
```

### 2. APP 图标

#### Android

- 找到 `android/app/src/main/res` 目录下的对应 `mipmap-*` 文件夹, 替换。
- 可以直接使用: [图标工厂](https://icon.wuruihong.com) 来生成图标。

#### IOS

- 找到 `ios/test/Images.xcassets/AppIcon.appiconset` 文件夹下。
- 直接用 [图标工厂](https://icon.wuruihong.com) 生成的图标替换。

### 3. 添加启动页

- 添加启动页可以使用 `react-native-splash-screen` 库, 通过它可以控制启动页的显示和隐藏

# React-Native

## 创建一个 typescript 项目

`npx react-native init projectName --template react-native-template-typescript`

### 如何修复第三方的问题

- 查看是否有更新的测试版或者未发布版本
- fork
  - 自己修改后发布，或者直接安装github地址
  - 可以向原作者贡献补丁
- patch-package
  - 如果是修改原生第三方，先生成补丁，在编译
- 用yarn resolutions修复间接依赖

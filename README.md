# 短信私密增强版
<img alt="Logo" src="graphics/icon.webp" width="120" />

这是基于 Fossify Messages 修改后的个人版本，重点放在通知操作隐私保护和短信界面优化。

## 版本说明

这个仓库展示的是我修改后的版本，不是原版仓库首页说明。

本版本主要目标：

- 阻止外部应用伪造短信通知快捷操作
- 收紧通知相关安全细节
- 优化会话列表和搜索结果的界面显示

## 主要修改内容

### 1. 通知操作隐私保护

- 将通知里的“标为已读”“直接回复”“删除短信”接收器改成 `exported=false`
- 防止外部应用直接发送同名广播来控制短信行为
- 收紧通知 `PendingIntent` 的创建方式，降低被外部篡改利用的风险

### 2. 界面优化

- 会话列表增加更自然的左右留白
- 会话卡片增加更清晰的层次感
- 搜索结果项同步做了间距和卡片风格统一
- 主界面底部区域和列表阅读体验更清爽

## 关键修改入口

- `app/src/main/AndroidManifest.xml`
- `app/src/main/kotlin/org/fossify/messages/helpers/NotificationHelper.kt`
- `app/src/main/res/layout/activity_main.xml`
- `app/src/main/res/layout/item_conversation.xml`
- `app/src/main/res/layout/item_search_result.xml`

## 发行说明

GitHub Release 中上传的是当前修改版构建产物。

注意：

- 当前 Release 附件为 `unsigned` APK
- 原因是当前构建环境没有正式签名证书
- 如果需要可直接安装的正式版，需要再使用你自己的签名证书重新打包

## 仓库说明

- 默认分支：`private-ui-edition`
- 这个分支保存的是我当前这套隐私增强和界面优化修改
- 原版 Fossify 项目请以官方仓库为准

<div align="center">
<img alt="App image" src="fastlane/metadata/android/en-US/images/phoneScreenshots/1_en-US.png" width="30%">
<img alt="App image" src="fastlane/metadata/android/en-US/images/phoneScreenshots/2_en-US.png" width="30%">
<img alt="App image" src="fastlane/metadata/android/en-US/images/phoneScreenshots/3_en-US.png" width="30%">
</div>

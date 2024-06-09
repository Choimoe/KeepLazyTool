# KeepTool

本生成器仅适用于运动后手机不在身边，需要截图打卡的情形，请不要不运动而生成截图！😣

同时请不要在有关 Keep 的平台与各平台的官方动态下讨论任何关于本项目内容，感谢合作！🥺 

[TOC]

## 使用教程

首先需要下载本项目，在电脑端支持 `canvas` 的浏览器中打开 `./keep_draw.html`：

2. 绘制路径，然后将绿色起点和红色终点图标拖到相应位置
3. 填写头像、昵称、日期、天气、温度、距离与运动数据，其中有些数据会自动计算，详见页面右侧提示栏。
4. 进行截图。

## 更新日志

### Jun 9, 2024 ---- 适配新版UI

本次更新重构了代码，适配了新版UI。存在一些不影响最终效果的小 bug，因作者时间原因不进行修改。

针对操作上的优化与新增加的功能有：

- 将原先使用的 `<input>` 框改为 `contenteditable="true"` 的文本，方便直接修改。
- 将所有可以修改的文本框在输入时存储到 `localStorage`，在开始访问时读取。
- 添加路径辅助图层及开关、方便绘制路径。
- 添加自定义昵称与自定义头像。
- 自动计算 `平均配速`、`运动消耗`；自动填充 `总时长`；自动填充随机 `累计爬升`、`平均步频`、`运动负荷`。

目前新增加的一些问题：

- `平均配速` 由于自动计算，与读取 `localStorage` 的顺序冲突，首次显示不正常。
- 如上条，在修改自动随机填充的部分也会冲突，导致无法再次随机填充。

## 一些问题

### 我不在山青怎么办？

可以对本项目的图片素材（位于 `.\assets\`）进行修改：

- `beg.png` 与 `end.png`：手绘的起点终点素材。
- `anime_girl_avatar.png`：小女孩头像，因版权原因上传时删除了。
- `abstract_red_shapes.png`：路径辅助图片。
- `fitness_app_interface.png`：运动截图。

将你的截图去除轨迹后替换 `fitness_app_interface.jpg` 即可，需要大致对齐位置。

### 可以拿去用吗？

除盈利外用途是被允许的，可以对代码进行任何更改，但请勿用作商业发售！
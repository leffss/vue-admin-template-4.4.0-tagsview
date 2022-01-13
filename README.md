# 说明

基于 https://github.com/PanJiaChen/vue-admin-template release 4.4.0 版本修改：

1. 添加 tagsView（src/settings.js 可设置是否启用），并新增`关闭左边`和`关闭右边`功能

2. 修正原版 tagsView 存在的问题：`关闭其他`或者`关闭所有`时会触发 `affix: true` 的标签也重新刷新

3. router 新增 `confirm` 选项（关闭或者刷新标签时是否弹出确认框），详见 src/router/index.js 注释

4. src/settings.js 新增 `openedMenu` 设置（默认打开的左侧导航）

5. 实验性的加入 `vue-aplayer` 实现音乐播放器（src/settings.js 可设置是否启用）

**注意事项：使用 tagsView 时需要注意 router 设置 name 的值必须和相应的 vue 组件的 name 相同，否则
keep-alive 功能会失效，即每次点击已打开的 tag 都会触发刷新**


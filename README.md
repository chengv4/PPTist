# 🎨 PPTist
> 一个基于 Vue3.x + TypeScript 的在线演示文稿（幻灯片）应用，还原了大部分 Office PowerPoint 常用功能，支持 文字、图片、形状、线条、图表、表格、视频、音频、公式 几种最常用的元素类型，每一种元素都拥有高度可编辑能力，同时支持丰富的快捷键和右键菜单，支持导出本地 PPTX 文件，您可以在此基础上搭建自己的在线幻灯片应用。

在线体验地址：[https://pipipi-pikachu.github.io/PPTist/](https://pipipi-pikachu.github.io/PPTist/)

如果网络状态不佳，可以访问国内镜像（非实时更新）：[https://pptist.gitee.io/](https://pptist.gitee.io/)


# 👀 前排提示
1. 本项目的目标是打造一个 “在线幻灯片应用” ，而非 “低代码平台”、“H5 编辑器” 或 “图片编辑工具” 等。
2. 本项目的目标受众是<b>有【Web 幻灯片】开发需要的开发者</b>，提供的链接只是一个演示地址，并不能作为工具使用，也不提供任何在线服务。
如果你只是需要一个服务或工具，可以选择更优秀和成熟的产品，例如：[石墨文档](https://shimo.im/)、[金山文档](https://www.kdocs.cn/)、[Slidev](https://sli.dev/)、[revealjs](https://revealjs.com/) 等。
3. 本项目是基于 DOM 的渲染方案，好处是简单。但是相比 Canvas 渲染的方案，在复杂场景下性能会存在一定的差距，所以如果你对性能有较高的要求，本项目可能不是一个好的参考方向。


# 🚀 项目运行
```
npm install

npm run serve
```


# 📚 功能列表
### 基础功能
- 历史记录（撤销、重做）
- 快捷键
- 右键菜单
- 导出本地文件（PPTX、JSON、图片、PDF）
- 打印
### 幻灯片页面编辑
- 页面添加、删除
- 页面顺序调整
- 页面复制粘贴
- 背景设置（纯色、渐变、图片）
- 设置画布尺寸
- 网格线
- 标尺
- 画布缩放、移动
- 主题设置
- 幻灯片备注
- 幻灯片模板
- 翻页动画
- 元素动画（入场、退场、强调）
### 幻灯片元素编辑
- 元素添加、删除
- 元素复制粘贴
- 元素拖拽移动
- 元素旋转
- 元素缩放
- 元素多选（框选、点选）
- 多元素组合
- 多元素批量编辑
- 元素锁定
- 元素吸附对齐（移动和缩放）
- 元素层级调整
- 元素对齐到画布
- 元素对齐到其他元素
- 多元素均匀分布
- 拖拽添加图文
- 粘贴外部图片
- 元素坐标、尺寸和旋转角度设置
- 元素超链接（链接到网页、链接到其他幻灯片页面）
#### 文字
- 富文本编辑（颜色、高亮、字体、字号、加粗、斜体、下划线、删除线、角标、行内代码、引用、超链接、对齐方式、项目符号、清除格式）
- 行高
- 字间距
- 填充色
- 边框
- 阴影
- 透明度
#### 图片
- 裁剪（自定义、按形状、按纵横比）
- 滤镜
- 翻转
- 边框
- 阴影
- 替换图片
- 重置图片
- 设置为背景图
#### 形状
- 填充色
- 边框
- 阴影
- 透明度
- 翻转
- 编辑文字
#### 线条
- 颜色
- 宽度
- 样式
- 端点样式
#### 图表（柱状图、条形图、折线图、面积图、散点图、饼图、环形图）
- 数据编辑
- 背景填充
- 主题色
- 坐标系与坐标文字颜色
- 其他图表设置
- 边框
- 图例
#### 表格
- 行、列添加删除
- 主题设置（主题色、表头、汇总行、第一列、最后一列）
- 合并单元格
- 单元格样式（填充色、文字颜色、加粗、斜体、下划线、删除线、对齐方式）
- 边框
#### 视频
- 预览封面设置
#### 音频
- 图标颜色
- 自动播放
- 循环播放
#### 公式
- LaTeX编辑
- 颜色设置
- 公式线条粗细设置
### 幻灯片放映
- 全部幻灯片预览
- 画笔、黑板工具
- 激光笔
- 自动放映
- 演讲者视图


# 💡 常见问题
**Q. 为什么xxx快捷键没有作用？**

A. 部分快捷键需要聚焦到指定区域才会生效，例如焦点在左边缩略图列表才能使用操作页面的快捷键，焦点在画布区域才能使用操作元素的快捷键。

**Q. 为什么粘贴没有作用？**

A. 请注意允许浏览器访问系统剪贴板。

**Q. 为什么浏览器刷新或重新打开后，之前做的PPT没有了？**

A. 该演示项目是纯前端部署的，不会保存数据。

**Q. 如何调整幻灯片页面的顺序？**

A. 按住左侧缩略图可进行拖拽调整顺序。

**Q. 为什么插入图片后会出现操作卡顿的情况？**

A. 由于本演示项目不依赖后端，插入本地图片实际引用的是Base64，导致数据体积非常大，在真正的生产环境中应该上传图片后引用图片地址，就不会出现这样的情况了。

**Q. 为什么应用预置主题后没有效果？**

A. 设置预置主题的作用是使新添加的元素和页面应用主题样式，不会对已有的元素和页面生效，您可以使用“应用主题到全部”功能，将当前主题应用到全部页面中。

**Q. 设置在线字体不生效？**

A. 设置在线字体时会下载对应的字体文件，该文件较大，需要等待下载完成后才会应用新的字体。

**Q. 关于导入导出PPTX文件**

A. 作为一个在线幻灯片应用，导出、导入 PPTX 文件是非常重要的功能，但是经过调研发现，该功能实现起来的复杂度远超过了预期。由于个人能力和时间有限，这部分功能只能借助第三方的轮子来完成。

目前导出功能主要基于 [PptxGenJS](https://github.com/gitbrent/PptxGenJS/) 完成，能够实现大多数基本元素的导出，但还有非常多的缺陷需要一点点完善。同时需要知晓的是：1、该功能依赖 PptxGenJS，对于该库本身无法实现的部分（如动画），本项目也无能为力；2、导出功能的目标只是【导出样式尽可能一致的元素】，而不是一比一将网页还原到PPT，一些样式差异是必然存在的。

导入功能目前暂时没有合适的解决方案，还在调研和观望中。如果有感兴趣或做过相关内容的朋友，欢迎来 issues 中讨论。

> PS. 我做了一个 [pptx转json](https://github.com/pipipi-pikachu/pptx2json) 的实验，可做参考。

同时补充一点，本项目不是 office PPT 的专属在线编辑器，本质上与 office PPT 没有任何关系。【导入/导出 ppt 文件】只是项目的一个功能而非目的。

**Q. 视频元素支持哪些格式？**

A. 本项目只提供最基础的视频能力，正常状态下可以播放video标签本身支持的格式。

此外，可以额外引入 [hls.js](https://github.com/video-dev/hls.js) 或 [flv.js](https://github.com/Bilibili/flv.js) 来支持对应的格式（.m3u8 .flv），你只需要在项目中引入对应的文件（如cdn）即可，无需其他配置。

**Q. 关于导入JSON文件**

A. 首先，出于安全等原因，个人并不建议将这种功能在前端直接暴露给用户，或者说用户根本就不应该接触到JSON这种格式（甚至导出JSON功能的初衷也只是为了方便开发）。如果真的有相关的需求，请自行在服务端实现，核心在于做好进行数据的校验，前端实现也是一样。


# 📅 后续规划
## 重要功能规划
- 组合元素重构：能够支持组合元素进行旋转、缩放、整体执行动画等；
- 添加强化版基础形状：支持调整圆角矩形弧度、调整三角形顶点位置等操作；
- 移动端简单编辑支持；
- 导入本地PPTX文件；

## 项目规划
- 跟进 Vue3 script setup 语法；
- 将 Vue CLI 更换到 Vite 生态；
- 开发文档；


# 📁 项目目录结构
```
├── assets                        // 静态资源
│   ├── fonts                     // 在线字体文件
│   └── styles                    // 样式
│       ├── antd.scss             // antd默认样式覆盖
│       ├── font.scss             // 在线字体定义
│       ├── global.scss           // 通用全局样式
│       ├── mixin.scss            // scss全局混入
│       ├── variable.scss         // scss全局变量
│       └── prosemirror.scss      // ProseMirror 富文本默认样式
├── components                    // 与业务逻辑无关的通用组件
├── configs                       // 配置文件，如：画布尺寸、字体、动画配置、快捷键配置、预置形状、预置线条等数据。
├── hooks                         // 供多个组件（模块）使用的 hooks 方法
├── mocks                         // mocks 数据
├── plugins                       // 自定义的 Vue 插件
├── types                         // 类型定义文件
├── store                         // Vuex store，参考：https://vuex.vuejs.org/zh/guide/
├── utils                         // 通用的工具方法
└── views                         // 业务组件目录，分为 `编辑器` 和 `播放器` 两个部分。
    ├── components                // 公用的业务组件
    ├── Editor                    // 编辑器模块
    └── Screen                    // 播放器模块
```


# 💿 数据
幻灯片的数据主要由 `slides` 和 `theme` 两部分组成。
> 换句话说，在实际的生产环境中，一般只需要存储这两项数据即可。

- `slides` 表示幻灯片页面数据，包括每一页的ID、元素内容、备注、背景、动画、切页方式等信息
- `theme` 表示幻灯片主题数据，包括背景色、主题色、字体颜色、字体等信息

具体类型的定义可见：[https://github.com/pipipi-pikachu/PPTist/blob/master/src/types/slides.ts](https://github.com/pipipi-pikachu/PPTist/blob/master/src/types/slides.ts)


# 💻 贡献代码
首先感谢每一位关注本项目的朋友，非常欢迎每一位对本项目感兴趣的朋友贡献代码。
### 具体参考如下：
- fork 源码，下载到本地并运行项目
- 添加/修改代码
- <b>对相关改动进行全面的自我测试（这非常重要）</b>
- 确认无误后提交修改到 Github
- 提交 Pull Request

### 另外需要注意的是：
- 每一次 Pull Request 都不应该提交过多的代码，且务必说明本次改动的具体目的，例如：修复了某个 bug、优化了某个方法 等，方便进行 Code Review；
- 对于 bug 的修复，应该将本次 Pull Request 和相对应 bug 的 issue 关联起来，让别人知道该问题已经被修复；
- 对于较大的新功能，你需要先提交 Issues，例如 “添加 XXX 功能”，确认该功能有被添加的必要后，再开始工作；
- 对于一些主观的样式、交互逻辑调整：如颜色、图标的使用，某些预设配置的增减修改等，一般不予通过。但可以在 Issues 中进行讨论；
- 其他如简单的代码优化、文档修正等，只要修改合理都会被接受。

在此感谢每一位贡献者。


# 📄 开源协议
[Apache-2.0 License](https://github.com/pipipi-pikachu/PPTist/blob/master/LICENSE)
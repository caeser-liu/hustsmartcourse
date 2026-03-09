# HUST SmartCourse Automation Pipeline
## ⚠️ 严正声明 (Disclaimer)
本项目仅供前端 DOM 操作、跨域框架通信（Iframe Routing）以及流媒体平台时序风控机制的学术研究与技术探讨。
**使用者需自行承担因违反所属机构教务平台《用户协议》或触发后端学术诚信风控审计（如进度回滚、成绩清零、违纪通报）而产生的一切后果。** 开发者不对任何滥用行为负责。

## ⚙️ 核心技术特性 (Core Features)

1. **环境上下文劫持 (Context Hijacking):** 通过 `Object.defineProperty` 强行覆写原生 `document.hidden` 与 `visibilityState` 属性，并在捕获阶段阻断 `visibilitychange` 与 `blur` 事件，实现系统级防失焦暂停（支持后台静默挂机）。
2. **安全时序注入 (Safe Time-Series Progression):** 强制剥离浏览器的自动播放策略（Auto-play Policy）拦截，并将底层 `<video>` 组件的 `playbackRate` 锁定在安全的 1.5 倍速阈值内，规避服务端物理时间差异常审计。
3. **跨框架精确寻址 (Cross-Frame DOM Routing):** 突破前端微服务嵌套架构的 Iframe 沙盒隔离。在子文档视频流触发 `ended` 事件后，利用 `window.top.document` 强行获取父级文档控制权，遍历并过滤无效标题节点，精准触发下一个任务点的业务跳转逻辑。

## 🛠️ 环境依赖 (Prerequisites)

* **内核要求:** 仅支持基于 Chromium 内核的现代浏览器（Google Chrome, Microsoft Edge 等）。
* 从这里开始看就行！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！
* **扩展容器:** 必须安装 [Tampermonkey (篡改猴)](https://www.tampermonkey.net/) 脚本管理器（严禁使用过时或无权限支持的第三方平替扩展），直接在插件中搜索即可。
* **系统权限:** 浏览器必须开启**“开发者模式” (Developer Mode)** 以允许本地脚本的 DOM 注入，跟随篡改猴的提示开启。

## 🚀 部署标准作业程序 (Deployment SOP)

1. 点击浏览器扩展栏的 Tampermonkey 图标，选择 **“添加新脚本” (Create a new script...)**。
2. **彻底清空**编辑器内自带的所有默认模板代码。
3. 复制本项目目录下的代码，按下 Ctrl + S 保存并退出。确保 Tampermonkey 仪表板中该脚本处于启用（绿色）状态。

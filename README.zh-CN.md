# Chat Plus

<p align="center">
  <a href="./README.md">English</a> | 简体中文
</p>

<p align="center">
  <img src="icons/icon128.png" alt="Chat Plus 标志" width="96">
</p>

<p align="center">
  <strong>把普通网页 AI，变成能连接工具、帮你干活的超级助手。</strong>
</p>

Chat Plus 是一个浏览器插件。它不是新的 AI，也不是新的聊天软件。它做的事情很简单：**增强你正在使用的网页 AI 聊天网站，让它不只是回答问题，还能连接工具去做事。**

普通网页 AI 最大的问题是：它很会聊，但很多时候做不了实际操作。它不能直接碰你的本地工具，不能直接操作浏览器，不能直接读写文件，也不能直接调用你电脑里的自动化能力。

Chat Plus 就是给这些网页 AI 加一层“工具连接能力”。

配合 [MCP-Gateway](https://github.com/aiguicai/MCP-Gateway) 使用后，你可以把各种工具先统一放到一个地方，再让 Chat Plus 把这些工具接进网页 AI 聊天里。这样你还是在熟悉的网页 AI 里聊天，但它背后已经能连接工具、执行任务、拿回结果，然后继续回答你。

## 一句话说明

以前：

```text
网页 AI = 只能聊天
```

现在：

```text
网页 AI + Chat Plus + MCP-Gateway = 能聊天，也能连接工具帮你做事
```

## 它能带来什么

装上 Chat Plus，并配合 MCP-Gateway 之后，网页 AI 可以从“只会说”变成“能做事”。

比如你可以让 AI：

- 调用你配置好的工具
- 操作浏览器
- 使用本地脚本或自动化流程
- 读写文件或数据
- 调用本地服务
- 查询外部接口
- 执行一串任务
- 把工具执行结果带回聊天里继续分析

你不用换掉原来的 AI 网站，也不用重新学习一个复杂平台。你还是打开原来的聊天网页，只是它被增强了。

## MCP-Gateway 是什么

你可以先不用管“MCP”这些专业词。

简单理解：[MCP-Gateway](https://github.com/aiguicai/MCP-Gateway) 就像一个“工具中转站”。

它负责把各种工具集中起来，例如：

- 本地工具
- 自动化脚本
- 浏览器控制能力
- 文件读写能力
- 电脑操作能力
- 各种接口和服务
- 其他可以被 AI 调用的能力

然后 Chat Plus 负责把这个“工具中转站”接到网页 AI 聊天里。

所以你可以这样理解：

```text
MCP-Gateway：负责管理工具
Chat Plus：负责把工具接进网页 AI
网页 AI：负责理解你的需求并决定怎么使用工具
```

## 为什么需要 Chat Plus

因为很多人已经习惯了直接用网页 AI，比如 ChatGPT、Gemini、DeepSeek、豆包、通义千问等。

这些网站的聊天体验很好，但它们通常只能在网页里回答你。你想让它们使用本地工具、操作浏览器、调用自己的服务，就会很麻烦。

Chat Plus 的目的就是让这些网页 AI 继续保持原来的使用方式，同时获得更强的工具能力。

你不需要先理解底层协议，也不需要知道每个工具背后怎么连接。你只需要知道：

1. MCP-Gateway 把工具准备好。
2. Chat Plus 把工具接进网页 AI。
3. 你在网页 AI 里正常聊天。
4. 需要工具时，AI 就可以调用工具并把结果带回来。

## 适配不同聊天网站

Chat Plus 不只想支持一个网站。

不同 AI 网站的页面结构不一样，所以 Chat Plus 使用“适配器”。你可以把适配器理解成“让 Chat Plus 认识这个网站的小插件”。

有了适配器，Chat Plus 就知道：

- 怎么把工具信息交给这个网页 AI
- 怎么读取 AI 的回复
- 怎么显示工具执行结果
- 怎么把结果继续送回当前聊天

仓库里已经有一些示例适配器，例如：

- ChatGPT
- Gemini
- Google AI Studio
- DeepSeek
- 豆包
- 通义千问 Chat
- Arena
- 小米 Mimo
- Z.ai
- Chatbox

重点不是这个列表有多长，而是：只要写好适配器，更多网页 AI 聊天网站也可以接入。

## 整体流程

```text
你的工具 / 脚本 / 浏览器操作 / 文件读写 / 本地服务
        |
        v
MCP-Gateway 把它们集中起来
        |
        v
Chat Plus 在浏览器里连接这些能力
        |
        v
网页 AI 聊天网站获得工具能力
        |
        v
AI 调用工具，拿到结果，继续和你对话
```

## 基本使用

1. 运行 [MCP-Gateway](https://github.com/aiguicai/MCP-Gateway)。
2. 在 MCP-Gateway 里添加你想让 AI 使用的工具或能力。
3. 安装或加载 Chat Plus 浏览器插件。
4. 打开一个已经支持的网页 AI 聊天网站。
5. 在 Chat Plus 里添加 MCP-Gateway 提供的地址。
6. 给当前网页启用需要的工具。
7. 正常聊天，需要工具时让 AI 调用即可。

## 从源码安装

```bash
npm install
npm run build
```

构建输出：

- `dist/chrome`
- `dist/firefox`

加载方式：

- Chrome / Edge：打开 `chrome://extensions`，启用开发者模式，选择“加载已解压的扩展程序”，然后选择 `dist/chrome`。
- Firefox：打开 `about:debugging`，选择 `This Firefox`，然后加载 `dist/firefox/manifest.json`。

## 它不是什么

Chat Plus 不是新的 AI 模型，也不是 MCP-Gateway 的替代品。

它更像是一座桥：

- MCP-Gateway 把工具集中起来。
- Chat Plus 把工具接进网页 AI。
- 适配器让不同网页 AI 都有机会接入。

## 许可证

Chat Plus 采用 **GPL v3 或更高版本** 开源，详见 [LICENSE](LICENSE)。

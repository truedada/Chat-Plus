# Chat Plus

<p align="center">
  English | <a href="./README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <img src="icons/icon128.png" alt="Chat Plus logo" width="96">
</p>

<p align="center">
  <strong>Turn ordinary web AI chat into an assistant that can use tools and get work done.</strong>
</p>

Chat Plus is a browser extension. It is not a new AI model and not another chat app. It does one simple thing: **it upgrades the web AI chat sites you already use, so they can connect to tools instead of only replying with text.**

A normal web AI page is convenient, but it is usually stuck inside the chat box. It can write, analyze, and answer, but it usually cannot directly use your local tools, control your browser, read and write files, or run automation on your computer.

Chat Plus adds that missing tool connection layer.

Together with [MCP-Gateway](https://github.com/aiguicai/MCP-Gateway), you can put your tools in one place first, then let Chat Plus bring those tools into the web AI chat page. You still chat in the familiar AI website, but now it can use tools, run tasks, get results, and continue the conversation.

## In One Sentence

Before:

```text
web AI = chat only
```

After:

```text
web AI + Chat Plus + MCP-Gateway = chat plus real tool use
```

## What It Unlocks

With Chat Plus and MCP-Gateway, a web AI page can move from "only talking" to "actually doing things".

For example, you can let the AI:

- call tools you have configured
- operate the browser
- use local scripts or automation workflows
- read and write files or data
- call local services
- query external APIs
- run a chain of tasks
- bring tool results back into the chat for continued reasoning

You do not need to replace the AI website you already like, and you do not need to learn a heavy new platform. You open the same web AI page, but it is now enhanced.

## What MCP-Gateway Does

You do not need to understand the technical meaning of "MCP" first.

In simple terms, [MCP-Gateway](https://github.com/aiguicai/MCP-Gateway) is a tool hub.

It gathers things like:

- local tools
- automation scripts
- browser control
- file access
- computer-control workflows
- APIs and services
- other capabilities that an AI can use

Then Chat Plus connects that tool hub to the web AI chat page.

Think of it this way:

```text
MCP-Gateway: manages the tools
Chat Plus: brings the tools into web AI
web AI: understands your request and decides how to use them
```

## Why Chat Plus Exists

Many people already use web AI products such as ChatGPT, Gemini, DeepSeek, Doubao, Qwen Chat, and others.

Those chat experiences are good, but they usually only answer inside the page. If you want them to use local tools, control a browser, or call your own services, things become difficult.

Chat Plus keeps the web AI experience you already know, while adding stronger tool abilities behind it.

You do not need to understand the low-level protocol first. You only need to know:

1. MCP-Gateway prepares the tools.
2. Chat Plus connects those tools to web AI.
3. You chat normally in the web AI page.
4. When a task needs tools, the AI can call them and bring the result back.

## Works With Different Chat Sites

Chat Plus is not meant for only one website.

Different AI websites have different page layouts and message formats, so Chat Plus uses adapters. You can think of an adapter as a small piece that teaches Chat Plus how to work with one website.

With an adapter, Chat Plus knows:

- how to give tool information to that web AI
- how to read the AI response
- how to show tool results
- how to send results back into the same chat

This repository includes example adapters for:

- ChatGPT
- Gemini
- Google AI Studio
- DeepSeek
- Doubao
- Qwen Chat
- Arena
- Xiaomi Mimo
- Z.ai
- Chatbox

The list is not the limit. The point is that more web AI chat sites can be connected by adding adapters.

## How It Fits Together

```text
your tools / scripts / browser actions / file access / local services
        |
        v
MCP-Gateway gathers them
        |
        v
Chat Plus connects them inside the browser
        |
        v
web AI chat sites gain tool abilities
        |
        v
AI calls tools, gets results, and continues chatting with you
```

## Basic Usage

1. Run [MCP-Gateway](https://github.com/aiguicai/MCP-Gateway).
2. Add the tools or capabilities you want the AI to use.
3. Install or load the Chat Plus browser extension.
4. Open a supported web AI chat site.
5. Add the MCP-Gateway address in Chat Plus.
6. Enable the tools for the current page.
7. Chat normally and let the AI call tools when needed.

## Install From Source

```bash
npm install
npm run build
```

Build output:

- `dist/chrome`
- `dist/firefox`

Load the extension:

- Chrome / Edge: open `chrome://extensions`, enable Developer mode, then choose `Load unpacked` and select `dist/chrome`.
- Firefox: open `about:debugging`, choose `This Firefox`, then load `dist/firefox/manifest.json`.

## What Chat Plus Is Not

Chat Plus is not a new AI model. It is not a replacement for MCP-Gateway.

It is a bridge:

- MCP-Gateway gathers the tools.
- Chat Plus brings the tools into web AI.
- Adapters make different web AI sites connectable.

## License

Chat Plus is open source under **GPL v3 or later**. See [LICENSE](LICENSE).

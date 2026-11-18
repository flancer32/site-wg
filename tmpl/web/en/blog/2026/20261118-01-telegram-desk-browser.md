---
title: "PDE v3: Telegram Desk runs in the browser"
description: "I tested the PDE v3 Telegram Desk with my own account. ChatGPT successfully read conversations and sent messages. The browser-based Desk now offers 11 text-based operations."
summary: "I tested the PDE v3 Telegram Desk with my own account. ChatGPT successfully read conversations and sent messages. The browser-based Desk now offers 11 text-based operations."
image: "/img/brand/pde-icon.png"
date: 2026-11-18
display_date: "November 18, 2026"
relations:
  - pde
---

# PDE v3: Telegram Desk runs in the browser

At the end of October, I wrote about getting PDE v3 ready for its first tests. On November 18, I finally had something concrete to report: I used ChatGPT to work with my own Telegram account through PDE v3.

I found a contact, read the latest 50 messages in our conversation, and sent a private message. I also published posts to my Telegram channels through the same connection. [This post](https://t.me/alexgusev_lab_en/103), for example, was sent directly from ChatGPT.

## Telegram without running your own server

Telegram Desk is a standalone browser application. It connects directly to Telegram, keeps the account credentials and session in the user's browser, and carries out permitted operations.

A separate browser application, Browser Office, connects the Desk to the PDE infrastructure. ChatGPT accesses it through MCP.

There's no need to set up your own server or VPS. You only need a browser on your computer. Telegram credentials stay in the browser rather than being sent to the PDE Gate. Requests and results still pass through the Gate.

## What works so far

Telegram Desk currently provides **11 text-based operations**:

- **7 read operations:** account and contact information, conversation lists, message history, individual messages, and message search.
- **4 state-changing operations:** sending, editing, and forwarding text messages, plus marking conversations as read.

I've tested all seven read operations against my own account. Of the four state-changing operations, I've verified message sending, including publishing to channels. Editing, forwarding, and marking messages as read are implemented but haven't yet been tested against my live account.

The Telegram account owner decides which operations each AI client may use through the Desk's access policies.

For now, the Desk handles text only. It doesn't return photos, videos, voice messages, or files. It can tell when a message contains non-text content, but that content isn't available through the current operations.

I'm not yet sure when an LLM really needs the original binary file and when extracted text, an image description, or some other processed result would do the job. I'd rather explore the practical value of the text operations before adding more complexity.

## Looking for testers

Telegram Desk is working in my test environment, but PDE v3 is still under development. I'd now like to see how it behaves with other users, browsers, and AI clients.

If you'd like to try giving ChatGPT or another MCP client access to your Telegram account, follow [my Telegram channel](https://t.me/alexgusev_lab_en) and [send me a message](https://t.me/wiredgeese).

Tell me which AI assistant you use and what you'd like to try. Access to the test Gate is by invitation for now, and I'll help the first testers get set up.

There will probably be bugs and unexpected limitations. That's part of what I want to find out.

More about the project: [pde.network](https://pde.network/).

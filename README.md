# 📰 Solana News Launchpad

https://github.com/user-attachments/assets/1f8fb417-d71a-4d3e-b9df-c25f8c9818fb

## Overview

Solana News Launchpad is a project designed to give Solana token creators a decisive edge. In the fast-paced world of decentralized finance, speed, information, and efficiency are paramount.

The platform empowers creators to launch tokens rapidly in response to real-time Twitter intelligence, transforming news into crypto market opportunities. An integrated suite of tools brings together token creation, trading execution, and wallet management, enabling full lifecycle control from a single, intuitive dashboard.

## Key Features

* **Real-time News Feed:** A real-time news feed sourced from a selection of high-signal accounts, ensuring that critical information, breaking news, and market trends are delivered instantly.

* **Advanced Token Launcher:** A streamlined token launch system supporting Solana launchpads such as Pump.fun and Bonk.fun. Token name and symbol are AI-generated from tweet content, enabling token deployment within seconds, with optional post-launch sniping via a dedicated wallet pool.

* **Telegram Interface:** A fully synchronized Telegram environment that mirrors the web application, providing access to the same real-time feed, tools, and configuration options. This mobile-first experience enables users to manage the entire platform on the go using a single unified account.

* **Wallet Management:** A structured wallet management system allowing the creation, import, and organization of multiple Solana wallets by category. This enables coordinated token creation, trading activity, and capital management, enabling coordinated wallet management and fund routing.

* **Multi-Wallet Trading:** Integrated trading capabilities supporting execution across multiple wallets simultaneously or managed individually, providing flexibility in execution and strategy management.

* **Account Settings:** Configurable transaction parameters covering buying, selling, and sniping workflows, allowing precise control over transaction behavior and execution preferences.

* **Affiliate Program:** A built-in referral system that allows users to invite others to the platform via unique links and earn a share of the fees generated through referred activity.

## Architecture

* **Web Application (NextJS/TypeScript):** A unified dashboard for all platform operations. Using the Backend-for-Frontend pattern, it provides secure, streamlined access to the backend services powering token creation, trading, and wallet management.

* **Telegram Bot (Rust):** A mobile-native, headless client providing streamlined access to backend services. It mirrors the platform’s core functionalities (news feed, token creation, and wallet management) enabling full control directly from Telegram.

* **News Feed Service (Rust):** Ingests and processes data from specialized Twitter streams, broadcasting Tweets to all connected clients via WebSockets and the news feed Telegram channel.

* **Token Launcher Service (NodeJS/TypeScript):** Handles token creation by uploading metadata and token icon to IPFS and deploying the tokens directly on supported Solana launchpads, such as Pump.fun and Bonk.fun.

* **Funds Management Service (Rust):** Manages funds operations by orchestrating complex, multi-step transaction flows. It handles fund splitting to multiple trading wallet and consolidating profits back to a central wallet.

* **PostgreSQL Database:** Reliably stores all core data, including user accounts, encrypted wallet details, referral program information, and user settings for trading and sniping.

* **Redis Cache:** Provides a high-speed cache for incoming tweet data. It stores AI-generated token names and symbols to minimize repeated API calls for the same tweet, reducing cost and latency. This shared cache ensures pre-computed metadata is served instantly to all users acting on the same news, optimizing performance across the platform.

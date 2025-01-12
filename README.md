# 🚀 Mudi - Open Supply Chain 🌾

## 🌟 Overview

The Grocery Supply Chain Transparency Platform is designed to create transparency and fairness in Bangladesh's grocery market through a comprehensive digital ecosystem. This system connects farmers, retailers, consumers, and administrators, providing real-time trading data and market insights.

![Mudi Mukto System Architecture](https://github.com/user-attachments/assets/c3dea477-cd26-494d-bb06-671ab2ada233)

## 📝 Description

A user-friendly platform promoting transparency in the grocery supply chain. The web app tracks and displays real-time transaction data between farmers, retailers, and consumers, ensuring fair pricing.
Consumers can check product prices to avoid overcharging, while farmers and retailers benefit from a transparent system. By exposing price syndication and fostering accountability, the app aims to stabilize grocery markets in Bangladesh and protect consumers from exploitation.

## ⚙️ System Components

1. **Frontend Layer**
2. **API Layer**
3. **Core Services**
4. **Data Layer**
5. **External Integrations**

## 🏗️ System Architecture

At its core, the platform operates through specialized user interfaces tailored to each stakeholder's needs:

- **🧑‍🌾 Farmer Portal:** Manage inventory, list products, set prices, and track sales transactions.
- **🛒 Retailer Portal:** Focuses on purchasing, inventory management, and transaction tracking.
- **📱 Consumer Mobile App:** Check and compare prices, ensuring fair market rates.
- **🛡️ Admin Portal:** Provides complete visibility into all market activities and transactions.

The real-time trading functionality is powered by a sophisticated backend infrastructure. When a farmer lists a product or a retailer makes a purchase, the information flows through a WebSocket server for immediate data transmission. These trades are processed by specialized services:

- **📒 Order Book Service:** Manages all active buy and sell orders.
- **⚡ Trade Matching Engine (built-in Rust):** Pairs compatible trades for optimal speed.
- **💰 Price Discovery Engine:** Continuously calculates and validates fair market prices.

Data management employs a multi-layered approach:

- **💾 Main Database (MongoDB):** Stores core information about users, transactions, and products.
- **🚄 Redis Cache:** Provides high-speed access to frequently needed data like current prices.
- **📈 InfluxDB (Time-series database):** Stores historical price trends and market analytics.
- **✉️ RabbitMQ (Message Queue):** Ensures smooth communication between services.

The platform integrates several support services:

- **📊 Analytics Engine:** Processes market data to identify trends and anomalies.
- **🔔 Notification Service:** Keeps users informed about market activities and price changes via SMS and in-app notifications.
- **🧾 Reporting Service:** Generates customized reports for different stakeholders.

Security is implemented at every level, with encrypted communications and a robust authentication service. The API Gateway acts as the single entry point for all client requests, implementing rate limiting and security measures.

To handle Bangladesh's unique market conditions, the system is resilient and accessible, working efficiently even with limited internet connectivity using SMS notifications as a backup. The architecture scales horizontally to handle growing user bases and transaction volumes.

External integrations include:

- **💳 Payment Gateway:** For Subscription Tiers.
- **💹 Market Price APIs:** Helps validate pricing information.
- **💬 SMS Gateway:** Ensures critical information reaches users without internet access.

All components work together to create a transparent, efficient, and fair system, helping to stabilize grocery markets across Bangladesh.

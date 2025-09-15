# 🍲 LocalBites

[![Flutter](https://img.shields.io/badge/Mobile-Flutter-02569B?logo=flutter)](https://flutter.dev)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js)](https://nodejs.org)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?logo=postgresql)](https://www.postgresql.org)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**LocalBites** is a **community-driven food marketplace** that connects local chefs with hungry customers.  
It enables chefs to create profiles, showcase menus, and accept orders directly — while customers enjoy authentic, home-made meals through a polished mobile experience.

---
## 🔎 Overview

**LocalBites** makes food discovery personal and local:  
- Customers browse **chefs, kitchens, and menus** nearby.  
- Place **real-time orders** with add-ons & customizations.  
- Chefs manage **menus, pricing, and availability**.  
- Deliveries are tracked seamlessly.  
- Built with **Flutter (mobile)**, **Node.js backend**, and **PostgreSQL database**.

---

## 🚀 Features

- 👨‍🍳 **Chef Profiles** – Personalized chef pages with ratings & photos.  
- 📖 **Menu Management** – Add meals, prices, and daily specials.  
- 🛒 **Ordering System** – Cart, add-ons, and multi-step checkout.  
- 🚚 **Delivery Tracking** – Integrated delivery role for status updates.  
- 📲 **Beautiful Mobile UI** – Animated splash, onboarding, and responsive pages.  
- 🔐 **Authentication & Roles** – Clients, Chefs, Delivery drivers.  
- 💬 **Notifications** – Order updates, promotions, and system alerts.  
- 🌙 **Dark Mode Support** – Full light/dark theme switching.  

---

## 🏗️ Architecture
        ┌──────────────┐
        │   Flutter    │  ← Mobile app (ordering flow, onboarding, chef profiles)
        └──────┬───────┘
               │
        ┌──────▼──────┐
        │   Node.js   │  ← REST APIs: orders, chefs, menus, auth
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │ PostgreSQL  │  ← users, chefs, menus, orders, deliveries
        └─────────────┘


---


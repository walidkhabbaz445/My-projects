# 🌍 Adventura

Adventura is an **AI-powered activity booking and trip planner** built with **Flutter (mobile frontend)**, **FastAPI + Node.js (backend)**, and **PostgreSQL (database)**.  
It helps users discover, book, and manage unique activities & events — with smart availability, AI chat suggestions, and trip planning.

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Features](#-features)
- [Architecture](#-architecture)
- [Database Schema](#-database-schema)
- [Setup Guide](#-setup-guide)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [License](#-license)

---

## 🔎 Overview

**Adventura** makes adventure planning simple:  
- Browse activities & one-time events.  
- Check **real-time availability & slots**.  
- Book directly inside the app.  
- Get **AI-powered suggestions** via chatbot.  
- Generate **multi-day trip itineraries** tailored to preferences.  

---

## 🚀 Features

- 📅 **Smart Booking Flow** – Availability calendar + slot picker.  
- 🤖 **AI Chatbot** – Suggests activities, answers FAQs, plans trips.  
- 🗺️ **Trip Generator** – Build a multi-day itinerary with activities.  
- 🎟️ **Bookings Management** – View upcoming & past bookings.  
- 📲 **Polished Flutter UI** – Clean, modern, and responsive.  
- 🔐 **Authentication & Roles** – Clients, Providers, Deliveries.  
- 📸 **Reels Uploads** – Providers share videos with likes/comments.  

---

## 🏗️ Architecture


- **Frontend (Flutter)**: Booking flow, chat UI, trip planner UI, reels.  
- **Backend (FastAPI)**: AI chatbot, trip generator (Groq LLaMA models).  
- **Backend (Node.js)**: Booking & availability APIs.  
- **Database (PostgreSQL)**: Activities, bookings, availability, clients.  
- **Storage (Hive, Firebase)**: Local user data & reels videos.  

---

## 🗄️ Database Schema

Key tables:  
- **activities**: Stores activities/events (with category, trending flag).  
- **availability**: Date + time slot availability per activity.  
- **bookings**: User bookings (with soft delete & status).  
- **client** & **user**: Split for authentication & profile.  
- **trip_plans** & **activity_features**: Store generated trip itineraries.  

---
## 🛠️ Roadmap

- [x] Booking flow with availability & slots
- [x] AI chatbot with activity suggestions
- [x] Multi-day trip generator
- [ ] Payment integrations (credit card, wallets)
- [x] Agent-based AI planning
- [x] Web dashboard for Admins

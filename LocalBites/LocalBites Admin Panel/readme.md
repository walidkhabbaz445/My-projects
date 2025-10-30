# 🍽️ LocalBites – Admin Dashboard & Backend

A professional, full-stack **LocalBites Admin Platform** built with:
-  **React (Admin Dashboard Frontend)**
-  **Node.js + Express + Sequelize (Backend API)**
-  **PostgreSQL (Database)**

Designed for internal use by LocalBites admins to manage chefs, dishes, clients, orders, analytics, and system notifications — all in one secure control center.

---

## 🧩 Overview

The **LocalBites Admin Dashboard** provides a central hub to manage the entire LocalBites food-tech ecosystem.

### 🌟 Key Features

#### 👨‍🍳 Chef Management
- View and approve or reject **chef verification submissions**
- Review uploaded verification documents, selfies, and kitchen photos
- Track each chef’s **profile status**: `not_applied`, `pending`, `approved`, `rejected`
- Update chef profiles, bios, and availability status
- See all dishes linked to each chef and their performance metrics

#### 🍛 Dish & Menu Control
- Full CRUD for dishes: create, edit, archive, or delete
- Manage dish visibility and status (`draft`, `active`, `archived`)
- Upload and preview dish images via AWS S3
- View reviews, ratings, and analytics for each dish
- Tagging, allergens, cuisine, and serving options support

#### 📦 Orders & Reservations
- View all customer reservations in real time
- Filter by status (`pending`, `confirmed`, `fulfilled`, `cancelled`, etc.)
- Monitor chef fulfillment performance
- See linked client details, slot times, and total transaction values
- Admins can override or update order states if needed

#### 👥 Client Management
- View all registered clients with full profile details:
  - Name, Email, Role, Status, Date of Birth, Created At
- Track order history per client
- View default addresses, notifications, and device tokens
- Access review activity and ratings history

#### 📊 Analytics & Insights
- Dashboard widgets for:
  - Total Active Chefs, Clients, and Dishes
  - Orders per day/week/month
  - Top rated dishes and chefs
  - Revenue summary (total and per chef)
  - Review ratings distribution
- Interactive charts built with React + Chart.js (or Recharts)
- Data fetched dynamically from `/admin/analytics` API endpoints

#### 🔔 Notifications Center
- Send broadcast or targeted push notifications to users
- Manage all system alerts and announcements
- Integration with Firebase Cloud Messaging (FCM)

#### 🖼️ Media Management
- Secure S3 uploads for chef verification documents, dish photos, and intro videos
- Multipart upload for large videos
- Presigned URLs for controlled access

#### 🧾 Audit & Security Logs
- Every admin action (like chef approval or review moderation) is logged
- Audit logs accessible under `/admin/audit`
- Includes request IDs, timestamps, and affected entities

---

## ⚛️ Frontend (Admin Dashboard)

### Tech Stack
| Layer | Technology |
|-------|-------------|
| Framework | React (CRA or Vite) |
| UI Library | Material UI (MUI 5) |
| State Management | Redux Toolkit / React Query |
| Charts | Chart.js / Recharts |
| Routing | React Router v6 |
| Auth | JWT-based, integrated with backend |
| API Client | Axios with interceptors |
| Notifications | Toastify / Snackbar alerts |

### Major Pages
- **Dashboard** – Overview charts and KPIs
- **Chefs** – List, search, view details, approve/reject verification
- **Dishes** – Manage all dishes and their details
- **Orders** – Track all reservations and statuses
- **Clients** – View and manage registered clients
- **Analytics** – Revenue and growth insights
- **Notifications** – Broadcast center for announcements
- **Settings** – Admin preferences and logout

---

## 🟩 Backend (Express + PostgreSQL)

### Tech Stack
| Layer | Technology |
|-------|-------------|
| Framework | Express.js |
| ORM | Sequelize |
| Database | PostgreSQL |
| Validation | Zod |
| File Storage | AWS S3 |
| Push Notifications | Firebase Cloud Messaging |
| Authentication | JWT, OTP, Google OAuth2 |
| Security | Helmet, HPP, Rate Limits, CORS |

### Core APIs
- `/auth` – Login, Signup (OTP), Refresh, Logout, Google Auth
- `/chef` – Manage and verify chefs
- `/dishes` – CRUD for dishes and images
- `/availability` – Manage chef slots and availability
- `/reservations` – Booking and order flow
- `/reviews` – User reviews and moderation
- `/notifications` – User inbox and admin broadcast
- `/addresses` – Manage client delivery addresses
- `/devices` – Register user device tokens (for FCM)
- `/media` – Secure S3 upload/download URLs
- `/admin` – Audit, analytics, and chef verification APIs

---

## 🧠 Security Highlights

- 🔒 JWT authentication & role enforcement middleware  
- 🧩 Zod schema validation on every route  
- 🧱 Helmet & HPP for HTTP hardening  
- 🚦 Rate limits per route (Auth, OTP, General)  
- 🧾 UUIDv4 IDs and Sequelize transactions for atomic actions  
- 🕵️ Centralized audit logs for every admin operation  

---

## 🧰 Project Structure


# 🚚 GoCarry

**GoCarry** is a modern parcel delivery and logistics platform that connects **customers, riders, and administrators** through a complete web-based delivery management system.

The project consists of a **React/Vite client** and a **Node.js/Express backend**, with Firebase Authentication, MongoDB, Stripe payments, parcel tracking, rider management, and role-based access control.

---

## 🌐 Live Project

- **Client:** https://gocarry-acfd5.web.app/
- **Server:** https://go-carry-server-side.vercel.app/

---

## ✨ Main Features

### 👤 Authentication

- Firebase Email/Password authentication
- Google authentication
- Protected routes
- Firebase token-based API authentication
- Role-based access: **User, Rider, Admin**
- Profile management

### 📦 Parcel Management

- Create, view, edit, and delete parcels
- Document and non-document parcels
- Sender and receiver information
- District and service-center selection
- Delivery cost calculation
- Parcel status management
- User-specific parcel history

### 💳 Stripe Payments

- Stripe PaymentIntent integration
- Secure online payment
- Payment status tracking
- Payment history
- Parcel and payment relationship

### 🚴 Rider Management

- Rider application
- Admin approval/rejection
- Rider status management
- Parcel assignment
- Delivery status updates
- Rider notifications

### 📍 Tracking

- Parcel tracking
- Tracking history
- Delivery status updates
- District/location information

### 👨‍💼 Admin Dashboard

- User management
- Rider management
- Parcel management
- Rider assignment
- Warehouse management
- Notifications
- Dashboard statistics

### 🗺️ Delivery Coverage

- Bangladesh district coverage
- Interactive Leaflet map
- District search
- Dynamic service-center selection

---

## 🛠️ Technology Stack

### Client

- React
- Vite
- JavaScript
- React Router
- Tailwind CSS
- shadcn/ui
- React Hook Form
- TanStack Query
- Axios
- Firebase Authentication
- Stripe
- Leaflet / React Leaflet
- SweetAlert2
- Lucide React

### Server

- Node.js
- Express.js
- MongoDB Native Driver
- Firebase Admin SDK
- Stripe
- CORS
- dotenv

### Deployment

- Firebase Hosting
- Vercel

---

## 🏗️ Project Architecture

```text
GoCarry
│
├── client/
│   ├── React + Vite
│   ├── Firebase Authentication
│   ├── TanStack Query
│   ├── Stripe
│   └── Leaflet
│
├── server/
│   ├── Node.js
│   ├── Express.js
│   ├── MongoDB
│   ├── Firebase Admin
│   └── Stripe API
│
└── README.md
```

---

## 🔐 Authentication Flow

```text
Firebase Authentication
        ↓
Firebase Token
        ↓
Secure Axios
        ↓
Authorization: Bearer Token
        ↓
Express Server
        ↓
Firebase Admin Verification
        ↓
Protected API
```

---

## 📦 Parcel Delivery Flow

```text
Customer
   ↓
Create Parcel
   ↓
Calculate Delivery Cost
   ↓
Payment
   ↓
Parcel Created
   ↓
Admin Assigns Rider
   ↓
Rider Pickup
   ↓
In Transit
   ↓
Out for Delivery
   ↓
Delivered
```

---

## 💰 Delivery Pricing

| Parcel             | Same District | Different District |
| ------------------ | ------------: | -----------------: |
| Document           |           ৳60 |                ৳80 |
| Non-document ≤ 3kg |          ৳110 |               ৳150 |

For non-document parcels above 3kg, additional charges are applied according to the project's pricing rules.

---

## 🗄️ Database Collections

```text
users
parcels
payments
riders
tracking
notifications
warehouses
```

MongoDB is used with the **native MongoDB driver**.

---

## 🔌 Main API Routes

```text
/users
/parcels
/payments
/riders
/tracking
/admin
/dashboard
/notifications
```

The API uses Firebase Bearer tokens for protected requests and role-based middleware for admin and rider operations.

---

## ⚙️ Client Setup

```bash
git clone <client-repository-url>
cd GoCarry-client-side
npm install
npm run dev
```

Create `.env.local`:

```env
VITE_API_URL=your_backend_url

VITE_FIREBASE_API_KEY=your_key
VITE_FIREBASE_AUTH_DOMAIN=your_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id

VITE_STRIPE_PUBLIC_KEY=your_stripe_publishable_key
VITE_IMGBB_API_KEY=your_imgbb_api_key
```

---

## ⚙️ Server Setup

```bash
git clone <server-repository-url>
cd GoCarry-server-side
npm install
npm run dev
```

Create `.env`:

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string
DB_NAME=gocarry

STRIPE_SECRET_KEY=your_stripe_secret_key

FB_SERVICE_KEY=your_firebase_service_configuration

CLIENT_URL=your_client_url
```

Never commit `.env`, Firebase private keys, Stripe secret keys, or database credentials.

---

## 🔒 Security

GoCarry uses:

- Firebase token verification
- Admin authorization
- Rider authorization
- Protected API routes
- Environment variables
- CORS configuration
- Server-side authentication
- Secure Stripe integration

---

## 👥 User Roles

| Role      | Main Responsibilities                                      |
| --------- | ---------------------------------------------------------- |
| **User**  | Create parcels, payments, tracking                         |
| **Rider** | Handle assigned deliveries and update status               |
| **Admin** | Manage users, riders, parcels, warehouses, and assignments |

---

## 📱 Responsive Design

The client is designed for:

- 📱 Mobile
- 💻 Desktop
- 🖥️ Large screens

The UI uses responsive Tailwind CSS layouts with reusable components and modern dashboard interfaces.

---

## 🚀 Development Commands

### Client

```bash
npm install
npm run dev
npm run build
npm run preview
```

### Server

```bash
npm install
npm run dev
npm start
```

---

## 👨‍💻 Developer

**Md. Tushar Hossain**

**MERN Stack Developer / Junior Software Developer**

---

## 📄 License

This project is developed for **educational and portfolio purposes**.

---

### ⭐ GoCarry

**A modern parcel delivery platform built with React, Node.js, Express, MongoDB, Firebase, and Stripe.**

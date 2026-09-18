# 🛒 Grocery Delivery App

A full-stack grocery delivery web app inspired by Instacart, built with React, TypeScript, Node.js, Prisma, and PostgreSQL.

## Features

- Product browsing by category with search and filters
- Cart management and multi-step checkout
- Order tracking with live map and OTP delivery confirmation
- Admin dashboard — manage products, orders, and delivery partners
- Delivery partner portal — accept/complete orders
- Background job processing with Inngest
- Image uploads via Cloudinary
- Email notifications via Nodemailer
- Authentication with JWT

## Tech Stack

**Client:** React, TypeScript, Vite, Tailwind CSS  
**Server:** Node.js, Express, TypeScript  
**Database:** PostgreSQL, Prisma ORM  
**Other:** Inngest, Cloudinary, Nodemailer, Vercel

## Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL database
- Cloudinary account
- Inngest account

### Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/Mohit20251/grocery-delivery-fullstack.git
   cd grocery-delivery-fullstack
   ```

2. **Server**
   ```bash
   cd server
   npm install
   # Create .env file (see Environment Variables below)
   npx prisma migrate dev
   npx tsx seed.ts       # optional: seed sample data
   npm run dev
   ```

3. **Client**
   ```bash
   cd client
   npm install
   # Create .env file (see Environment Variables below)
   npm run dev
   ```

## Environment Variables

### `server/.env`
```
DATABASE_URL=
JWT_SECRET=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
EMAIL_USER=
EMAIL_PASS=
INNGEST_EVENT_KEY=
INNGEST_SIGNING_KEY=
```

### `client/.env`
```
VITE_API_URL=http://localhost:5000
```

## Deployment

Both client and server include `vercel.json` for deployment on [Vercel](https://vercel.com).

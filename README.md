# Flight Reservation System

This project is a **web-based flight booking system** built with **Next.js**, **TypeScript**, **TailwindCSS**, and **Neon PostgreSQL**. It allows users to search for flights, make reservations, and receive email confirmations. Admins can manage flights and view trends.

## Features

- User Authentication (Login/Signup)
- Search & Reserve Flights
- Admin Dashboard
- Send Email on Reservation (via Resend API)
- Trending Airlines Statistics
- Fully responsive UI

## Tech Stack

| Component       | Technology           |
|----------------|----------------------|
| Frontend       | Next.js, React, Tailwind CSS |
| Backend        | Next.js API Routes (App Router) |
| Database       | Neon PostgreSQL (hosted) |
| Auth & State   | Cookies, Server Actions |
| Email Service  | Resend API |
| ORM/SQL Client | PostgreSQL tagged queries via `@neondatabase/serverless` |

## Requirements

- Node.js 18+
- pnpm or npm
- Neon database account (or replace with local PostgreSQL)
- Resend API Key (for email notifications)
- Git

## Project Structure
├── app/                  # Next.js App Router
│   ├── page.tsx          # Home page
│   └── dashboard/        # Admin dashboard routes
├── components/           # Reusable UI components
├── lib/                  # Database and utilities
│   └── neon.ts           # SQL tagged queries
├── actions/              # Server actions (booking, get data)
├── public/               # Static files
├── styles/               # Tailwind CSS configuration
├── types/                # TypeScript type definitions
├── .env                  # Environment variables
├── tailwind.config.ts    # Tailwind config
├── tsconfig.json         # TypeScript config

  

  ## Dependencies
  -Package	Purpose
  -next	React-based SSR framework
  -tailwindcss	Utility-first CSS framework
  -@neondatabase/serverless	PostgreSQL access (Neon)
  -resend	Email sending API
  -cookies	Cookie-based auth/session
  -Usage Flow
  -User signs up and logs in
  -User selects destination and date
  -User selects a flight and reserves it
  -Reservation is stored in DB and email confirmation is sent
  -Admin can view flight stats in dashboard


## Installation

### Install Dependencies

```bash
npm install

Set Environment Variables
Create a .env file in the root directory and add the following:
DATABASE_URL=your_neon_postgres_database_url
RESEND_API_KEY=your_resend_api_key

Run the Development Server
npm run dev
Visit http://localhost:3000 in your browser.


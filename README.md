# FloatMaster Uganda

A modern Progressive Web App (PWA) for mobile money float management, bill payments, bank transactions, and multi-branch business operations in Uganda.

## Features

- **Dashboard** — Real-time overview of float balance, sales, expenses, net profit, active agents, and pending bills with interactive charts
- **Transactions** — Record, edit, delete, filter, search, and export deposits/withdrawals with agent assignment
- **Agents** — Manage mobile money agents with commission rates, contact info, and status toggles
- **Bill Payments** — Process electricity, water, internet, TV, airtime/data, and other utility payments with status tracking
- **Bank Management** — Track multiple bank accounts, record bank transactions, monitor balances
- **Reports** — Generate summary, transaction, agent, and bill reports with date range filtering and data visualization
- **Settings** — Business info, multi-branch management, dark/light theme, notification preferences
- **PWA** — Installable on mobile/desktop, works offline with service worker caching
- **Real-time** — Live data sync via Supabase Realtime across all devices
- **Dark Mode** — Full dark theme support

## Tech Stack

- **React 18** + **TypeScript**
- **Vite** — Build tool
- **Tailwind CSS** — Styling
- **Framer Motion** — Animations
- **Recharts** — Data visualization
- **Supabase** — Backend, Auth, Realtime, Database
- **Lucide React** — Icons

## Quick Start

### 1. Clone & Install

```bash
git clone https://github.com/YOUR_USERNAME/floatmaster-uganda.git
cd floatmaster-uganda
npm install
```

### 2. Supabase Setup

1. Create a project at [supabase.com](https://supabase.com)
2. Run the SQL from `supabase/setup.sql` in the SQL Editor
3. Go to Project Settings > API and copy your URL and anon key
4. Create a `.env` file:

```env
VITE_SUPABASE_URL=https://your-project.supabase.co
VITE_SUPABASE_ANON_KEY=your-anon-key
```

### 3. Run Locally

```bash
npm run dev
```

### 4. Build for Production

```bash
npm run build
```

## Deploy to Vercel

1. Push code to GitHub
2. Go to [vercel.com](https://vercel.com) → Import Project
3. Select your GitHub repo
4. Add Environment Variables:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
5. Deploy!

## Database Schema

The app uses these Supabase tables:
- `businesses` — Business profiles
- `branches` — Multi-branch support
- `users` — App users with roles
- `agents` — Mobile money agents
- `transactions` — Financial transactions
- `bill_payments` — Utility bill payments
- `bank_accounts` — Bank account records
- `bank_transactions` — Bank transactions
- `float_balances` — Float balance tracking
- `notifications` — In-app notifications

See `supabase/setup.sql` for full schema with RLS policies.

## License

MIT

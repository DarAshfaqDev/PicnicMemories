# The Friendship Vault

> A digital museum celebrating 12+ years of annual picnics across Kashmir by three best friends — Ishfaq, Rouf & Shoib.

![Next.js](https://img.shields.io/badge/Next.js-16-black?logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-38bdf8?logo=tailwindcss)
![React](https://img.shields.io/badge/React-19-61dafb?logo=react)
![Prisma](https://img.shields.io/badge/Prisma-SQLite-2d3748?logo=prisma)

---

## Overview

**The Friendship Vault** is an emotionally rich, visually stunning single-page web application that preserves and showcases the memories of three childhood friends from Kashmir who have been organizing annual picnics every year since 2013. The site features glassmorphism design, nature-inspired color palettes, smooth Framer Motion animations, dark/light mode, and interactive data visualizations.

From the snow-covered meadows of Gulmarg to the untouched valleys of Lolab, every picnic location, funny moment, and shared meal is documented here — a living tribute to a friendship that has only grown stronger with time.

---

## Features

### Core Sections

| Section | Description |
|---------|-------------|
| **Cinematic Hero** | Fullscreen slideshow with floating particles, SVG mountain silhouettes, and gradient text |
| **12-Year Timeline** | Alternating left/right timeline with weather icons, season badges, star ratings, and expandable detail dialogs |
| **Photo Gallery** | Masonry grid with category filters, search, favorites, and a lightbox with keyboard navigation |
| **Friend Profiles** | Detailed cards for Ishfaq, Rouf & Shoib with bios, awards, fun facts, and funny habits |
| **Statistics Dashboard** | Animated counters, budget/distance/season charts (Recharts), and fun facts |
| **Memory Journal** | Picnic journal entries and story cards with expand/collapse |
| **Friendship Wall** | Masonry quote wall with inside jokes (locked), like toggles |
| **Guestbook** | Visitor messages with emoji picker and reaction system |
| **Then vs Now** | Image comparison slider showing how the trio and locations have changed |
| **Random Memory** | Floating button that serves a random photo, story, or picnic memory |
| **Search** | Live search across picnics, photos, stories, and friends with typed result badges |
| **Travel Map** | Visual representation of all picnic locations across Kashmir |
| **Countdown** | Live countdown timer to the next picnic |
| **On This Day** | Shows what the trio was doing on this date in past years |

### Design & UX

- **Dark / Light Mode** — Toggle with smooth transitions via `next-themes`
- **Glassmorphism Cards** — Frosted glass effects on cards and overlays
- **Nature-Inspired Palette** — Forest green, sky blue, sunset orange, warm beige (no default blue/purple)
- **Framer Motion Animations** — Scroll reveals, parallax effects, floating particles, page transitions
- **Responsive Design** — Mobile-first with full mobile navigation (Sheet menu)
- **Scroll Progress Bar** — Animated progress indicator in the navigation
- **Active Section Tracking** — Navigation highlights current section on scroll
- **Keyboard Shortcuts** — Escape to close, arrow keys for gallery navigation
- **Custom Scrollbar** — Styled scrollbars for a polished look

---

## Tech Stack

| Technology | Purpose |
|-----------|---------|
| [Next.js 16](https://nextjs.org/) | React framework (App Router) |
| [TypeScript 5](https://www.typescriptlang.org/) | Type safety |
| [React 19](https://react.dev/) | UI library |
| [Tailwind CSS 4](https://tailwindcss.com/) | Utility-first styling |
| [shadcn/ui](https://ui.shadcn.com/) | Component library (New York style) |
| [Framer Motion 12](https://www.framer.com/motion/) | Animations & transitions |
| [Recharts 2](https://recharts.org/) | Data visualization charts |
| [Prisma 6](https://www.prisma.io/) | ORM for database |
| [SQLite](https://sqlite.org/) | Embedded database |
| [next-themes](https://github.com/pacocoursey/next-themes) | Dark/light mode |
| [Lucide React](https://lucide.dev/) | Icon library |
| [Sonner](https://sonner.emilkowal.dev/) | Toast notifications |
| [date-fns](https://date-fns.org/) | Date formatting & utilities |

---

## Project Structure

```
friendship-vault/
├── public/
│   └── images/
│       ├── hero/          # Hero slideshow backgrounds (3 images)
│       ├── friends/       # Friend avatars (3 images)
│       ├── picnics/       # Picnic hero images (12 images, 2013-2024)
│       └── gallery/       # Gallery photos (7 images)
├── prisma/
│   └── schema.prisma  # Database schema (12 models)
├── src/
│   ├── app/
│   │   ├── globals.css   # Custom theme, glassmorphism, animations
│   │   ├── layout.tsx    # Root layout with ThemeProvider, fonts, SEO
│   │   └── page.tsx      # Main page composing all sections
│   ├── components/
│   │   ├── ui/            # 40+ shadcn/ui base components
│   │   ├── navigation.tsx       # Sticky nav with scroll tracking
│   │   ├── hero-section.tsx     # Cinematic hero with particles
│   │   ├── timeline-section.tsx  # 12-year picnic timeline
│   │   ├── gallery-section.tsx   # Masonry photo gallery + lightbox
│   │   ├── friends-section.tsx   # Friend profile cards
│   │   ├── statistics-section.tsx # Charts + animated counters
│   │   ├── journal-section.tsx   # Memory journal + stories
│   │   ├── friendship-wall.tsx   # Quote wall with inside jokes
│   │   ├── guestbook-section.tsx # Visitor guestbook
│   │   ├── then-vs-now.tsx      # Image comparison slider
│   │   ├── random-memory.tsx     # Random memory floating button
│   │   ├── search-section.tsx    # Live search across all content
│   │   ├── footer.tsx           # Site footer
│   │   └── theme-provider.tsx   # Dark/light mode provider
│   ├── lib/
│   │   ├── db.ts          # Prisma database client
│   │   ├── seed-data.ts   # All picnic, friend, photo, story data
│   │   └── utils.ts      # Utility functions (cn helper)
│   └── hooks/
│       ├── use-mobile.ts  # Mobile detection hook
│       └── use-toast.ts  # Toast notification hook
├── .env                  # Environment variables (DB path)
├── package.json
├── tsconfig.json
└── README.md
```

---

## Prerequisites

- **Node.js** 18.17 or later (v20+ recommended)
  - Download: [https://nodejs.org](https://nodejs.org/)
  - Verify: `node --version`
- **npm** (comes bundled with Node.js)
  - Verify: `npm --version`
- **Git** (for cloning, if applicable)

> **Note:** You do NOT need Bun. The project works entirely with Node.js and npm.

---

## Installation

### Step 1: Open the Project

Extract or copy the project folder to your preferred location, then open it in **VS Code**:

```
File > Open Folder > select the project folder
```

Open the VS Code terminal: `Ctrl + `` ` ` (backtick) or `Terminal > New Terminal` from the menu.

### Step 2: Install Dependencies

```powershell
npm install
```

This downloads all required packages. It takes 2-5 minutes depending on your internet speed. You will see some deprecation warnings — **these are safe to ignore**.

### Step 3: Fix the `.env` File

Open the `.env` file in the project root and make sure it contains:

```
DATABASE_URL=file:./db/custom.db
```

> **Important:** If it contains a path like `/home/z/my-project/db/custom.db`, change it to `file:./db/custom.db` (the relative version). The absolute path won't work on Windows.

### Step 4: Generate Prisma Client

```powershell
npx prisma generate
```

### Step 5: Create the Database

```powershell
npx prisma db push
```

This creates a `db/custom.db` SQLite file in the project folder.

### Step 6: Start the Development Server

```powershell
npm run dev
```

You will see:

```
  ▲ Next.js 16.x
  - Local:        http://localhost:3000
  - Environments: .env

 Ready in 2-3s
```

### Step 7: Open in Browser

Go to **http://localhost:3000** in your browser.

---

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm install` | Install all dependencies |
| `npm run dev` | Start development server on port 3000 |
| `npm run build` | Create production build |
| `npm run start` | Start production server |
| `npm run lint` | Run ESLint code quality checks |
| `npx prisma generate` | Generate Prisma database client |
| `npx prisma db push` | Push schema to SQLite database |
| `npm run setup` | One-command setup: install + generate + push |

---

## Troubleshooting

### `tee` is not recognized

**Cause:** Older versions of this project had Unix-only commands in the dev script.

**Fix:** Make sure your `package.json` scripts section contains:

```json
"scripts": {
  "dev": "next dev -p 3000",
  "build": "next build",
  "start": "next start"
}
```

If it still has `| tee dev.log` or `cp -r`, remove those parts.

### `bun` is not recognized

**You don't need Bun.** Use `npm` for everything:

| Instead of | Use |
|-----------|-----|
| `bun install` | `npm install` |
| `bun run dev` | `npm run dev` |
| `bun run build` | `npm run build` |

### Database path error

If you see errors about `/home/z/my-project/db/custom.db`, edit `.env` and change it to:

```
DATABASE_URL=file:./db/custom.db
```

Then run:

```powershell
npx prisma generate
npx prisma db push
```

### Port 3000 already in use

Something else is running on port 3000. Either:
- Close the other program using port 3000
- Or change the port: `npx next dev -p 3001`

### Images not loading

The site uses AI-generated images in the `public/images/` folder. Make sure:
1. The `public/images/` folder exists with all subfolders (`hero/`, `friends/`, `picnics/`, `gallery/`)
2. Image files are `.png` format

### White screen / blank page

1. Open browser Developer Tools (`F12`) and check the **Console** tab for errors
2. Make sure `npm install` completed without errors
3. Make sure `npx prisma generate` was run
4. Try deleting the `.next` folder and restarting: `npm run dev`

### Deprecation warnings during install

Warnings like `deprecated uuid@8.3.2` or `deprecated recharts@2.15.4` are **normal and safe to ignore**. They don't affect functionality.

---

## Database Schema

The SQLite database contains 12 models:

- **Friend** — Profile data for each trio member
- **Picnic** — Details for each annual picnic (2013-2024)
- **PicnicFriend** — Many-to-many join table
- **Photo** — Gallery photos with metadata
- **Story** — Memory stories and journal entries
- **Expense** — Picnic expense tracking
- **GuestbookEntry** — Visitor guestbook messages
- **GuestbookReaction** — Emoji reactions on guestbook entries
- **Quote** — Friendship quotes and inside jokes
- **Album** — Photo album organization
- **SiteSettings** — Key-value site configuration

---

## Picnic Locations (2013 - 2024)

| Year | Location | Season |
|------|----------|--------|
| 2013 | Pahalgam | Summer |
| 2014 | Gulmarg | Autumn |
| 2015 | Sonmarg | Spring |
| 2016 | Doodhpathri | Summer |
| 2017 | Yusmarg | Autumn |
| 2018 | Gurez Valley | Summer |
| 2019 | Bangus Valley | Spring |
| 2020 | Srinagar Dal Lake | Summer |
| 2021 | Sinthan Top | Autumn |
| 2022 | Aharbal Waterfall | Summer |
| 2023 | Lolab Valley | Spring |
| 2024 | Keran Valley | Summer |

---

## Built With

- Designed and developed for **Ishfaq, Rouf & Shoib**
- Powered by the beauty of **Kashmir**
- 12 years of friendship, 12 picnics, countless memories

---

## License

This project is a personal digital museum. All rights reserved.

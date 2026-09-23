# Donezy Design Team Setup

Welcome! This repo is for the Donezy UX/UI redesign project. Here's everything you need to get started.

## Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/cherinegrove/donezy-design.git
cd donezy-design
```

### 2. Switch to the design branch
```bash
git checkout design/main
```

### 3. Install dependencies
```bash
npm install
```

### 4. Start the dev server
```bash
npm run dev
```

The app will run at `http://localhost:5173` (or another port if 5173 is in use).

---

## Project Structure

```
src/
├── components/      # React components (organize by feature)
├── pages/          # Page components
├── contexts/       # React context (app state)
├── types/          # TypeScript types
├── utils/          # Utility functions
├── integrations/   # API clients (Supabase, HubSpot, etc.)
├── styles/         # Global styles
└── App.tsx         # Main app component

supabase/
├── migrations/     # Database migrations
└── functions/      # Supabase edge functions
```

---

## Key Areas to Redesign

### 1. **Dashboard** (`src/pages/Dashboard.tsx`)
- Task overview cards
- Quick stats/metrics
- Project summaries
- Team performance

### 2. **Kanban Board** (`src/components/kanban/KanbanBoard.tsx`)
- Task cards
- Column headers
- Drag-and-drop UX
- Status indicators

### 3. **Task Detail** (`src/pages/TaskDetail.tsx`)
- Task form/editing
- Time tracking UI
- Subtasks
- Comments/activity feed
- File attachments

### 4. **Capacity Tracker** (`src/pages/CapacityTracker.tsx`)
- Team workload visualization
- Gantt chart
- Filters & date ranges
- Utilization metrics

### 5. **Time Tracking** (`src/components/time/TimerBox.tsx`)
- Timer start/pause/stop
- Time entry history
- Duration editing
- Task association

### 6. **Navigation & Layout**
- Sidebar navigation
- Header/top bar
- Mobile responsiveness
- Dark/light mode

### 7. **Admin Panel** (`src/pages/AdminPanel.tsx`)
- User management
- Project setup
- Custom statuses
- Settings

---

## Design Workflow

### Before you start coding:
1. Create mockups/wireframes (Figma, etc.)
2. Get approval from Cherine
3. Document the changes

### While redesigning:
1. Work on the `design/main` branch
2. Create small, focused commits
3. Test every feature in the **UX Testing Checklist** below
4. Keep responsive design in mind (mobile, tablet, desktop)

### When done:
1. Push your changes
2. Create a PR: `design/main` → `main`
3. Include before/after screenshots
4. Cherine reviews & merges

---

## Available Commands

```bash
npm run dev          # Start dev server
npm run build        # Build for production
npm run preview      # Preview production build locally
npm run type-check   # Run TypeScript type checking
npm run lint         # Run ESLint
```

---

## Important Files

- **`.env.local`** — Environment variables (you may need to set up Supabase keys)
- **`src/contexts/AppContext.tsx`** — Global app state
- **`src/types/index.ts`** — TypeScript type definitions
- **`tailwind.config.js`** — Tailwind CSS configuration (for styling)

---

## Testing the Design

After every change, test the corresponding UX flow. Use the **UX_TESTING_CHECKLIST.md** to ensure nothing breaks.

Key things to validate:
- ✅ Responsive on mobile, tablet, desktop
- ✅ Dark/light mode compatibility
- ✅ All buttons/links work
- ✅ Forms submit correctly
- ✅ Time tracking starts/stops/pauses
- ✅ Kanban cards drag & drop
- ✅ Filters/sorts work
- ✅ No console errors

---

## Getting Help

- Check `src/components/ui/` for existing UI components (buttons, inputs, cards, etc.)
- Look at existing pages for patterns
- Tailwind CSS docs: https://tailwindcss.com/
- Supabase context: `src/contexts/AppContext.tsx` shows how data flows

---

## Branch Strategy

- **`main`** — Production-ready code
- **`design/main`** — Active design work (your branch)
- Feature branches off `design/main` for big changes: `design/feature/kanban-redesign`, etc.

Push often, PR when ready for review!

---

**Let's make Donezy beautiful! 🎨**

# Donezy UX Testing Checklist

Use this checklist to validate **every** UX flow after design changes. Test on desktop, tablet, and mobile.

---

## 1. Authentication & Login

- [ ] Login page loads correctly
- [ ] Email/password input fields are accessible
- [ ] "Forgot password" link works
- [ ] Login button is visible and clickable
- [ ] Error messages display properly (invalid credentials, etc.)
- [ ] Loading state shows during login
- [ ] Redirect to dashboard on successful login
- [ ] Sign-up flow works (if applicable)

---

## 2. Dashboard

- [ ] Dashboard loads with no errors
- [ ] Task summary cards display correctly
  - [ ] Total tasks count
  - [ ] Tasks in progress count
  - [ ] Overdue tasks count
  - [ ] Due today count
- [ ] Project cards show project names, progress, status
- [ ] Quick action buttons are visible (+ New Task, etc.)
- [ ] Recent activity feed displays
- [ ] Charts/analytics render without distortion
- [ ] Responsive: stack cards on mobile
- [ ] Dark mode: text readable, colors contrasting

---

## 3. Navigation & Layout

- [ ] Sidebar displays all menu items
  - [ ] Dashboard
  - [ ] Kanban
  - [ ] List View
  - [ ] Capacity Tracker
  - [ ] Time Tracking
  - [ ] Projects
  - [ ] Admin (if user is admin)
- [ ] Active menu item is highlighted
- [ ] Sidebar collapse/expand works (if applicable)
- [ ] Header shows user avatar, notifications, settings
- [ ] Mobile: hamburger menu toggles sidebar
- [ ] Breadcrumbs show current location (if used)

---

## 4. Kanban Board

- [ ] Board loads with all columns visible
- [ ] Column headers display status names (New, In Progress, etc.)
- [ ] Task cards appear in correct columns
- [ ] Card titles are readable (not truncated)
- [ ] Card details visible:
  - [ ] Assignee avatar/name
  - [ ] Priority indicator
  - [ ] Due date
  - [ ] Estimated hours
- [ ] Drag-and-drop works:
  - [ ] Drag card between columns
  - [ ] Drag card within same column
  - [ ] Status updates on drop
  - [ ] No lag/jank during drag
- [ ] Click card opens detail modal/page
- [ ] + Add Task button in column header works
- [ ] Empty state displays when no tasks
- [ ] Filter works:
  - [ ] By assignee
  - [ ] By project
  - [ ] By status
- [ ] Sort works (by due date, priority, etc.)
- [ ] Mobile: columns scroll horizontally
- [ ] Mobile: tap card to expand details

---

## 5. Task List View

- [ ] Table/list loads without errors
- [ ] Columns display:
  - [ ] Task name
  - [ ] Status
  - [ ] Assignee
  - [ ] Due date
  - [ ] Priority
  - [ ] Project
  - [ ] Estimated hours
- [ ] Click row opens task detail
- [ ] Sort by clicking column headers
- [ ] Filter dropdown works
- [ ] Pagination or infinite scroll works (if applicable)
- [ ] Mobile: columns stack or horizontally scroll
- [ ] Empty state shows when no tasks

---

## 6. Task Detail / Task Form

### Creating a Task:
- [ ] + New Task button opens form/modal
- [ ] Title field required (validation shows if empty)
- [ ] Description field accepts text
- [ ] Project dropdown shows all projects
- [ ] Assignee dropdown shows all team members
- [ ] Status dropdown shows custom statuses (New, In Progress, etc.)
- [ ] Priority selector works (Low, Medium, High, Urgent)
- [ ] Due date picker works
- [ ] Estimated hours input accepts numbers
- [ ] Collaborators can be added
- [ ] File upload works (or placeholder shows "coming soon")
- [ ] Submit button creates task
- [ ] Success message displays
- [ ] Form closes after submit

### Editing a Task:
- [ ] Open existing task
- [ ] All fields are editable
- [ ] Changes save on submit
- [ ] Validation works for required fields
- [ ] Success message displays

### Task Detail View:
- [ ] Task title is prominent
- [ ] All task fields display (status, assignee, due date, etc.)
- [ ] Edit button opens edit form
- [ ] Delete button removes task (with confirmation)
- [ ] Status can be changed from detail view
- [ ] Tabs display:
  - [ ] Activity/timeline
  - [ ] Comments
  - [ ] Time entries
  - [ ] Subtasks (if applicable)
- [ ] Add comment field works
- [ ] Comment input validates and submits
- [ ] Previous comments display with timestamps

---

## 7. Time Tracking

### Timer:
- [ ] Start button begins timer
- [ ] Timer displays elapsed time (updates in real-time)
- [ ] Pause button pauses timer (without stopping)
- [ ] Resume button continues from pause
- [ ] Stop button ends timer session
- [ ] Stop shows duration before saving
- [ ] Save time entry creates entry in database
- [ ] Success message displays
- [ ] Timer resets after save
- [ ] Timer doesn't continue running in background if user navigates away
- [ ] Mobile: timer buttons are large/tappable

### Time Entry History:
- [ ] List shows all time entries for task
- [ ] Each entry shows:
  - [ ] Date/time
  - [ ] Duration
  - [ ] Task name
  - [ ] User who logged it
- [ ] Edit button allows changing duration
- [ ] Delete button removes entry (with confirmation)
- [ ] Total hours logged displays

---

## 8. Recurring Tasks

- [ ] Create Recurring Task dialog opens
- [ ] Title field required
- [ ] Project dropdown works
- [ ] Initial Status dropdown shows custom statuses
- [ ] Assignee dropdown works
- [ ] Pattern selector works:
  - [ ] Daily
  - [ ] Weekly (days of week selector)
  - [ ] Monthly (day of month selector)
- [ ] Repeat interval input works
- [ ] Start date picker works
- [ ] End date checkbox toggles
- [ ] Form submits and creates recurring task
- [ ] Success message displays
- [ ] Recurring task generates instances

---

## 9. Capacity Tracker

- [ ] Page loads without errors
- [ ] Filters display:
  - [ ] Owner/Assignee dropdown
  - [ ] Project dropdown
  - [ ] Client dropdown
  - [ ] Date range selector
- [ ] Reset Filters button clears all filters
- [ ] Summary cards display:
  - [ ] Total tasks count
  - [ ] In Progress count
  - [ ] To Do (New) count
  - [ ] Backlog count
- [ ] Gantt chart renders
- [ ] Gantt bars show task duration
- [ ] Gantt labels readable
- [ ] Gantt responsive (scroll horizontally on mobile)
- [ ] Scroll/zoom works on Gantt
- [ ] Task click in Gantt opens detail
- [ ] Date range at bottom updates based on filters

---

## 10. Projects

### Project List:
- [ ] All projects display
- [ ] Each card/row shows:
  - [ ] Project name
  - [ ] Status
  - [ ] Owner
  - [ ] Progress % (if shown)
  - [ ] Due date
- [ ] Click project opens detail
- [ ] + New Project button works
- [ ] Filter/search works

### Project Detail:
- [ ] Project name displayed
- [ ] Team members list shows
- [ ] Tasks associated with project display
- [ ] Project settings accessible (if user is owner)
- [ ] Edit button opens form
- [ ] Start date, due date, status display

---

## 11. Admin Panel

### User Management:
- [ ] User list displays all users
- [ ] Each user shows:
  - [ ] Name
  - [ ] Email
  - [ ] Role
- [ ] Add user button works
- [ ] Edit user works (change role, etc.)
- [ ] Delete user works (with confirmation)

### Settings:
- [ ] Custom task statuses display
- [ ] Add status works
- [ ] Edit status works
- [ ] Delete status works (if no tasks use it)
- [ ] Project templates display (if applicable)
- [ ] General settings accessible

---

## 12. Notifications & Alerts

- [ ] Toast notifications appear for:
  - [ ] Task created/updated/deleted
  - [ ] Time entry saved
  - [ ] Error messages
- [ ] Notifications are readable
- [ ] Notifications auto-dismiss
- [ ] Error notifications stay longer
- [ ] Notification icons/colors match intent (success green, error red, etc.)

---

## 13. Responsive Design

### Mobile (375px width):
- [ ] Layout doesn't break
- [ ] Text is readable (no tiny fonts)
- [ ] Buttons are tappable (48px minimum height)
- [ ] Forms stack vertically
- [ ] Navigation works (sidebar or hamburger)
- [ ] Tables scroll horizontally (not break)
- [ ] Modals are full-width and scrollable

### Tablet (768px width):
- [ ] Grid layouts adjust properly
- [ ] All content accessible
- [ ] Buttons/inputs appropriately sized

### Desktop (1200px+ width):
- [ ] Full layout displays
- [ ] Sidebar visible
- [ ] Multi-column layouts work
- [ ] No horizontal scroll

---

## 14. Dark Mode

- [ ] Toggle works (settings or theme switcher)
- [ ] Background colors invert
- [ ] Text remains readable
- [ ] Borders/dividers visible
- [ ] Cards have proper shadow/depth
- [ ] Colors accessible (WCAG AA contrast)
- [ ] Charts readable in dark mode
- [ ] Form inputs visible
- [ ] Buttons visible

---

## 15. Performance & General

- [ ] Page loads without console errors
- [ ] No broken images
- [ ] Links navigate correctly
- [ ] Loading states show for async operations
- [ ] Buttons disable while loading
- [ ] Form validation prevents invalid submissions
- [ ] Alerts/modals are accessible (keyboard navigation, focus)
- [ ] Search/filter is responsive (no lag)

---

## 16. Team Features

### Collaboration:
- [ ] Add collaborators to tasks works
- [ ] Collaborators list displays
- [ ] Comments from other users show
- [ ] Real-time updates (if applicable)

### Workload/Capacity:
- [ ] Team member workload displays
- [ ] Overbooked status shows
- [ ] Capacity percentage calculates
- [ ] Recommendations/alerts display

---

## Test Coverage Summary

After redesigning, test:
1. ✅ All flows above on **desktop**
2. ✅ All flows above on **mobile**
3. ✅ All flows above on **tablet**
4. ✅ **Dark mode** toggle & readability
5. ✅ **Responsive** images & layouts
6. ✅ **Accessibility** (keyboard nav, contrast, labels)
7. ✅ **Error states** (invalid inputs, API failures)
8. ✅ **Loading states** (spinners, disabled buttons)

---

## Reporting Issues

If you find a bug or UX problem:
1. Screenshot it
2. Note device/browser (desktop/mobile, Chrome/Safari, etc.)
3. Create a GitHub issue or leave a comment on the PR

**Document the issue clearly so it can be fixed!**

---

**Happy testing! 🧪**

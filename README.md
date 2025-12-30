# Student Management Dashboard

This project is a customization of the Mazer Admin Dashboard template, transformed into a Student Management System.

## Customizations Made

### UI/UX
- **Branding**: Updated sidebar logo to "Student Management" text.
- **Theme**: Changed primary theme color to a shade of blue (`#5A8DEE`) via SCSS variables.
- **Navigation**: Added a "Students" link to the sidebar.
- **Dashboard**: Redesigned the home page to show student statistics (Total, Active, Avg Marks, Inactive) and chart analytics. Replaced static table with "Top Performing Students".

### Pages
- **Students Page** (`src/pages/students.html`): A new page dedicated to student management.
    - Displays a table of students.
    - Includes Search, Status Filter, and Sorting by marks.
    - Shows a marks distribution chart.

### Data & Logic
- **Data Source**: `src/data/students.json` contains the mock student records.
- **Logic**:
    - `src/js/dashboard-custom.js`: Handles data fetching and rendering for the main dashboard (stats, charts, top students).
    - `src/js/students.js`: Handles the full logic for the Students page (CRUD-like read operations, sorting, filtering).
- **Configuration**: Updated `vite.config.js` to correctly resolve pages in `src/pages/` and inject `basePath` for correct asset loading in sub-directories.

## How to Run Locally

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Run Development Server**
   ```bash
   npm run dev
   ```
   Access the dashboard at `http://localhost:5173` (or the port shown in terminal).

3. **Build for Production**
   ```bash
   npm run build
   ```

## File Structure Highlights

- `src/data/students.json`: The data source.
- `src/js/`: Contains the logic scripts (`students.js`, `dashboard-custom.js`).
- `src/pages/`: Contains the new HTML pages (`students.html`).
- `src/layouts/`: Modified layouts (`sidebar.html`, `master.html`).

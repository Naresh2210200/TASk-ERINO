# TaskGlitch

A modern task management application built with React, TypeScript, and Material-UI. Track tasks with revenue, time tracking, priority management, and comprehensive analytics.
url : https://naresh-kumar-taskglitch.netlify.app/
## Features

- **Task Management**: Create, update, and delete tasks with title, revenue, time tracking, priority, and status
- **Analytics Dashboard**: View comprehensive metrics including:
  - Total revenue and time taken
  - Revenue per hour
  - Time efficiency percentage
  - Average ROI (Return on Investment)
  - Performance grading
- **Charts & Visualizations**: Interactive charts showing task distribution and trends
- **Activity Log**: Track all task-related activities (add, update, delete, undo)
- **Search & Filter**: Search tasks by title and filter by status and priority
- **CSV Export**: Export filtered tasks to CSV format
- **Undo Functionality**: Undo accidental task deletions
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Material-UI (MUI)** - Component library
- **MUI X Charts** - Data visualization
- **Day.js** - Date manipulation

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd task-glitch-main
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

### Building for Production

```bash
npm run build
```

The production build will be in the `dist` directory.

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
task-glitch-main/
├── public/
│   └── tasks.json          # Initial task data
├── src/
│   ├── components/         # React components
│   │   ├── ActivityLog.tsx
│   │   ├── AnalyticsDashboard.tsx
│   │   ├── ChartsDashboard.tsx
│   │   ├── MetricsBar.tsx
│   │   ├── TaskDetailsDialog.tsx
│   │   ├── TaskForm.tsx
│   │   ├── TaskTable.tsx
│   │   └── UndoSnackbar.tsx
│   ├── context/            # React context providers
│   │   ├── TasksContext.tsx
│   │   └── UserContext.tsx
│   ├── hooks/              # Custom React hooks
│   │   └── useTasks.ts
│   ├── utils/              # Utility functions
│   │   ├── csv.ts          # CSV export utilities
│   │   ├── logic.ts        # Business logic and calculations
│   │   └── seed.ts         # Data seeding utilities
│   ├── App.tsx             # Main application component
│   ├── main.tsx            # Application entry point
│   ├── types.ts            # TypeScript type definitions
│   ├── theme.ts            # MUI theme configuration
│   └── index.css           # Global styles
├── index.html
├── vite.config.ts          # Vite configuration
├── tsconfig.json           # TypeScript configuration
├── tsconfig.node.json      # TypeScript config for Node files
├── netlify.toml            # Netlify deployment configuration
└── package.json
```

## Deployment

This project is configured for deployment on Netlify. The `netlify.toml` file contains the deployment configuration.

### Netlify Deployment

1. Push your code to a Git repository
2. Connect the repository to Netlify
3. Netlify will automatically detect the build settings from `netlify.toml`
4. The site will be built and deployed automatically

## Bug Fixes

The following build issues have been resolved:

1. **Vite Config Module Resolution**: Fixed `node:path` and `node:url` imports to use standard `path` and `url` imports for better TypeScript compatibility
2. **TaskForm Missing Property**: Added `createdAt` property to task creation payload to satisfy TypeScript type requirements
3. **TypeScript Module Configuration**: Updated `tsconfig.node.json` to use `NodeNext` module resolution to match `nodenext` moduleResolution setting

## License

This project is private and proprietary.

## Contributing

This is a private project. Contributions are not accepted at this time.

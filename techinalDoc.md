\n## Frontend Folder Structure

The frontend application will strictly follow a feature-driven folder structure, utilizing **React with TypeScript**, **Redux Toolkit** for state management, and **Chakra UI** as the primary design system. This structure is designed for scalability, maintainability, and clear separation of concerns, supporting both public-facing and authenticated areas of the application. Test files will be co-located with the components/modules they test.

```
src/
├── assets/                 # Static assets (images, icons, fonts)
│   ├── images/
│   ├── icons/
│   └── fonts/
├── components/             # Reusable UI components (agnostic to business logic)
│   ├── ui/                 # Custom generic UI elements or complex compositions of Chakra components (e.g., CustomModal, FormInputGroup)
│   └── layout/             # General layout components (e.g., Header, Footer, Sidebar, Grid)
├── config/                 # Application-wide configuration, environment variables, constants
├── features/               # Feature-specific modules (auth, resume, portfolio, AI assistant)
│   ├── auth/               # e.g., Login, Registration, Password Reset
│   │   ├── components/     # Auth-specific UI (e.g., LoginForm, RegisterForm, AuthCard.tsx)
│   │   ├── hooks/          # Auth-specific logic (e.g., useAuth.ts)
│   │   ├── services/       # Auth-related API calls (e.g., authService.ts)
│   │   └── store/          # Feature-specific Redux Toolkit slice (e.g., authSlice.ts)
│   │   └── AuthCard.test.tsx # Co-located tests
│   ├── resume-management/  # e.g., Create, Edit, View, Delete Resumes
│   │   ├── components/     # ResumeCard, ResumeEditor, TemplateSelector
│   │   ├── hooks/          # useResume, useResumeList
│   │   ├── services/       # Resume API calls
│   │   └── store/          # Redux Toolkit slices (e.g., resumeSlice.ts, templatesSlice.ts)
│   ├── portfolio-management/# e.g., Manage portfolios, projects, showcase
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── services/
│   │   └── store/
│   └── ai-assistant/       # e.g., AI generation, analysis, feedback tools
│       ├── components/
│       ├── hooks/
│       ├── services/
│       └── store/
├── hooks/                  # Global, reusable custom React hooks (e.g., useDebounce, useLocalStorage.ts)
├── layouts/                # Overall application layouts for different sections
│   ├── AuthLayout.tsx      # For login, registration, password reset pages
│   ├── DashboardLayout.tsx # For authenticated user pages (dashboard, resume management)
│   └── PublicLayout.tsx    # For public landing page, about, etc.
├── pages/                  # Top-level route components (compose components from features/components and global components)
│   ├── public/             # Pages accessible without authentication
│   │   └── LandingPage.tsx
│   │   └── AboutPage.tsx
│   ├── auth/               # Pages for authentication flows
│   │   └── LoginPage.tsx
│   │   └── RegisterPage.tsx
│   ├── app/                # Authenticated application pages
│   │   ├── DashboardPage.tsx
│   │   ├── ResumeOverviewPage.tsx
│   │   └── SettingsPage.tsx
│   └── NotFoundPage.tsx
├── services/               # General API client setup, base service calls (e.g., axios instance.ts)
├── store/                  # Global Redux Toolkit store setup and slices
│   ├── index.ts            # Root store configuration, combine reducers
│   ├── slices/             # Global Redux Toolkit slices (e.g., uiSlice.ts for notifications/modals, userSlice.ts for global user state)
│   └── middlewares/        # Custom Redux middlewares
├── styles/                 # Global styles, Chakra UI theme extensions, utility classes
│   ├── theme/              # Chakra UI theme configuration, extensions, custom components styles
│   ├── base/               # CSS resets, global typography
│   └── global.css          # Any general global CSS
├── types/                  # TypeScript type definitions (API, component props, global)
│   ├── api.d.ts
│   ├── component.d.ts
│   └── global.d.ts
├── utils/                  # General utility functions (formatters, validators, helper functions.ts)
├── App.tsx                 # Main application component, global providers (ChakraProvider, Redux Provider), router setup
└── main.tsx                # Entry point (ReactDOM.render)
```
\n
## Tech Stack

-   **Frontend:** React + TypeScript
-   **Backend:** Python (FastAPI)
-   **Database:** PostgreSQL
-   **AI/ML:** Google's Gemini API (for LLM capabilities), Python libraries for document parsing (e.g., `pypdf`, `python-docx`)
-   **Authentication:** Clerk
-   **Hosting:** AWS (e.g., EC2/ECS for backend, S3 for storage, RDS for DB)
-   **CI/CD:** GitHub Actions### 2.3 Shared Components

#### 2.3.1 Common/Generic UI Components

1.  **Button:** Standard interactive button with various states and sizes.
2.  **Input/TextField:** Generic text input field.
3.  **Dropdown/Select:** Controlled component for selection.
4.  **Modal/Dialog:** Versatile overlay for information or forms.
5.  **Spinner/Loader:** Visual indicator for loading states.
6.  **Alert/Toast:** Non-intrusive notifications.
7.  **Icon:** Component for rendering SVG or font-based icons.
8.  **Card:** Flexible container for grouped content.

#### 2.3.2 Feature-Specific Reusable Components

1.  **FileUploadArea:** UI for drag-and-drop resume uploads.
2.  **AudienceSelector:** Component to select multiple audience types.
3.  **ChatWindow:** Core component for the AI chat pop-up.
4.  **ChatMessage:** Sub-component to render individual chat messages.
5.  **SuggestedQuestions:** Displays dynamic, clickable AI-generated questions.
6.  **PortfolioSectionDisplay:** Reusable component to render resume data sections.
7.  **ResumePreviewCard:** Displays a summary of an uploaded resume on the dashboard.

#### 2.3.3 Layout Components

1.  **AppHeader:** Application branding, navigation, user controls.
2.  **AppFooter:** Standard application footer.
3.  **MainLayout:** Wrapper for overall page layout.## Tech Stack

- **Frontend (FE):** React + TypeScript
- **Backend (BE):** Python (FastAPI)
- **Database (DB):** PostgreSQL
- **Authentication (Auth):** Auth0
- **AI Services:** OpenAI API (for data extraction, embeddings, and chat completions)
- **Hosting:** AWS (e.g., ECS for containers, S3 for static assets, RDS for DB)
- **CI/CD:** GitHub Actions
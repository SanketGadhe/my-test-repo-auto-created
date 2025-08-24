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
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain
- **Database:** PostgreSQL (structured data) + Vector Database (e.g., Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (e.g., `python-docx`, `PyPDF2`) integrated into backend
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain
- **Authentication:** Auth0 or Firebase Authentication
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway)
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain on AWS Lambda
- **Database:** PostgreSQL (structured data) + Vector Database (Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (`python-docx`, `PyPDF2`) for initial parsing, with a plan for potential advanced multi-language solutions.
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain, with multi-language prompt engineering.
- **Authentication:** Firebase Authentication
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway)
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain on AWS Lambda (AWS India Region: ap-south-1)
- **Database:** PostgreSQL (structured data) + Vector Database (Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (`python-docx`, `PyPDF2`) for English PDF/DOCX parsing.
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain, with English-specific prompt engineering.
- **Authentication:** Firebase Authentication
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway) in an AWS India Region (ap-south-1)
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain on AWS Lambda
- **Database:** PostgreSQL (structured data) + Vector Database (Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (`python-docx`, `PyPDF2`) for initial parsing, focusing on **English resumes**. Multi-language support is a future enhancement.
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain.
- **Authentication:** Firebase Authentication
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway) in **Mumbai (ap-south-1) region**.
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain on AWS Lambda
- **Database:** PostgreSQL (structured data) + Vector Database (Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (`python-docx`, `PyPDF2`) for initial parsing, focusing strictly on **English resumes for the first 2 years**. Multi-language support is a future roadmap item.
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain.
- **Authentication:** Firebase Authentication
- **Payment Gateway:** Razorpay (for UPI, internet banking, card payments in India)
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway, DynamoDB) in **Mumbai (ap-south-1) region**.
- **CI/CD:** GitHub Actions## Tech Stack
- **Frontend:** React with TypeScript
- **Backend:** Python (FastAPI) with LangChain on AWS Lambda
- **Database:** PostgreSQL (structured data) + Vector Database (Pinecone/Weaviate for RAG)
- **Document Processing:** Python libraries (`python-docx`, `PyPDF2`) for initial parsing, focusing strictly on **English resumes for the first 2 years**. Multi-language support is a future roadmap item.
- **AI/ML:** OpenAI API (GPT-4) orchestrated by LangChain.
- **Authentication:** Firebase Authentication
- **Payment Gateway:** Razorpay (for **subscription management** including UPI, internet banking, card payments in India)
- **Hosting:** AWS Serverless (Lambda, S3, API Gateway, DynamoDB) in **Mumbai (ap-south-1) region**.
- **CI/CD:** GitHub Actions
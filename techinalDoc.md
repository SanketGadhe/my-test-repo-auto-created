## Tech Stack

**Frontend:** React + TypeScript
  - *Styling:* Tailwind CSS
  - *Rationale:* Robust for interactive UIs, strong component model, type safety, and efficient styling with Tailwind.
**Backend:** Node.js (NestJS)
  - *Rationale:* Structured, scalable framework, excellent for building APIs, strong community, and suitable for integrating with external AI services like Gemini.
**Database:** PostgreSQL
  - *Hosting:* AWS RDS Multi-AZ
  - *Data Redundancy:* Configured for Multi-AZ for high availability and automated daily backups for disaster recovery.
  - *Rationale:* Reliable, open-source relational database, suitable for structured resume data and user preferences, with built-in high availability and backup.
**Authentication:** Auth0
  - *Rationale:* Managed service, reduces security burden, supports various authentication flows.
**Hosting:** AWS
  - *Frontend:* S3 + CloudFront (static site hosting, CDN for global content delivery).
  - *Backend:* AWS Fargate (ECS) (containerized API application for scalability for NestJS).
  - *File Storage:* AWS S3 (for uploaded resumes).
  - *Database:* AWS RDS (for managed PostgreSQL Multi-AZ).
  - *AI Services:* Primarily external Gemini API (for chatbot and resume AI logic).
**CI/CD:** GitHub Actions
  - *Rationale:* Integrated with GitHub, automates build, test, and deployment pipelines.
**Repository Structure:** Monorepo (Frontend and Backend within the same repository).
  - *Rationale:* Simplifies development workflow for co-located teams and shared configurations.
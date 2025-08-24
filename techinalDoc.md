## Tech Stack

- **Frontend:** React + TypeScript
  - *Rationale:* Robust for interactive UIs, strong component model, type safety.
- **Backend:** Node.js (NestJS)
  - *Rationale:* Structured, scalable framework, excellent for building APIs, strong community, and suitable for integrating with external AI services like Gemini.
- **Database:** PostgreSQL
  - *Rationale:* Reliable, open-source relational database, suitable for structured resume data and user preferences.
- **Authentication:** Auth0
  - *Rationale:* Managed service, reduces security burden, supports various authentication flows.
- **Hosting:** AWS
  - *Frontend:* S3 + CloudFront (static site hosting, CDN).
  - *Backend:* AWS Fargate (ECS) (containerized API application for scalability for NestJS).
  - *File Storage:* AWS S3 (for uploaded resumes).
  - *Database:* AWS RDS (for managed PostgreSQL).
  - *AI Services:* External Gemini API (for chatbot and potentially other AI logic).
- **CI/CD:** GitHub Actions
  - *Rationale:* Integrated with GitHub, automates build, test, and deployment pipelines.
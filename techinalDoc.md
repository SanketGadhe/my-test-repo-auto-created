## Tech Stack

- **Frontend:** React + TypeScript
  - *Rationale:* Robust for interactive UIs, strong component model, type safety.
- **Backend:** Python (FastAPI)
  - *Rationale:* Excellent for AI/ML integration, high performance, asynchronous capabilities, auto-generates OpenAPI docs.
- **Database:** PostgreSQL
  - *Rationale:* Reliable, open-source relational database, suitable for structured resume data and user preferences.
- **Authentication:** Auth0
  - *Rationale:* Managed service, reduces security burden, supports various authentication flows.
- **Hosting:** AWS
  - *Frontend:* S3 + CloudFront (static site hosting, CDN).
  - *Backend:* AWS Fargate (ECS) (containerized API application for scalability).
  - *File Storage:* AWS S3 (for uploaded resumes).
  - *Database:* AWS RDS (for managed PostgreSQL).
  - *AI Services:* AWS Textract/Comprehend, or other specialized AI/ML services as needed.
- **CI/CD:** GitHub Actions
  - *Rationale:* Integrated with GitHub, automates build, test, and deployment pipelines.
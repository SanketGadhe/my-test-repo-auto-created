## Frontend Architecture - Folder Structure

**Decision:** Adopt a standard React + TypeScript project structure with dedicated directories for pages, components, assets, hooks, utilities, styles, and types. The project will leverage Tailwind CSS for styling.

**Key Directories:**
- `src/pages`: Top-level components representing distinct application views.
- `src/components`: Reusable UI components.
- `src/assets`: Static assets like images, fonts, icons.
- `src/hooks`: Custom React hooks for encapsulating logic.
- `src/utils`: Helper functions and non-component-specific logic.
- `src/styles`: Global stylesheets, Tailwind CSS configuration, and base styles.
- `src/types`: TypeScript type definitions and interfaces.

**Monorepo Consideration:** While the current focus is on the `frontend` structure, the team confirmed a preference for "no separate repo for FE and BE," implying a monorepo. This will be addressed in more detail for the overall repository structure. The frontend project will likely reside in a subdirectory such as `packages/frontend` or `frontend/` at the root of the monorepo.

**Styling:** Tailwind CSS will be used for styling, integrated via its configuration file and utility-first approach. Custom themes or global styles will be managed through the Tailwind configuration and a global CSS file.
### 1. Frontend Folder Structure

The initial frontend folder structure is designed for clarity, maintainability, and scalability, following common React Native conventions.

```
src/
├── App.tsx
├── assets/
│   ├── images/
│   └── fonts/
├── components/
│   ├── Button/
│   │   ├── Button.tsx
│   │   └── Button.styles.ts
│   ├── Display/
│   │   ├── Display.tsx
│   │   └── Display.styles.ts
│   └── Keypad/
│       ├── Keypad.tsx
│       └── Keypad.styles.ts
├── constants/
│   ├── index.ts
│   └── colors.ts
├── hooks/
│   └── useCalculator.ts
├── screens/
│   └── CalculatorScreen/
│       ├── CalculatorScreen.tsx
│       └── CalculatorScreen.styles.ts
├── styles/
│   ├── theme.ts
│   └── index.ts
├── types/
│   └── index.ts
└── utils/
    └── math.ts
```

**Rationale:**

*   **`src/App.tsx`**: The root component where the application starts.
*   **`assets/`**: Centralized location for static resources (images, fonts).
*   **`components/`**: Houses reusable UI elements (e.g., buttons, display areas). Each component has its own folder for co-located code and styles.
*   **`constants/`**: Stores immutable application-wide values like operation types, button labels, and color palettes.
*   **`hooks/`**: Contains custom React Hooks for encapsulating and reusing complex stateful logic, such as the core calculator operations (`useCalculator.ts`).
*   **`screens/`**: Contains top-level components representing distinct views. For this single-screen app, it will primarily contain `CalculatorScreen`.
*   **`styles/`**: Manages global styling concerns, including themes, color palettes, and typography definitions.
*   **`types/`**: Defines global TypeScript interfaces and types for consistent data structures.
*   **`utils/`**: Provides pure, helper functions that are not directly tied to React components or state, such as mathematical operations.

**ADR Log:**

*   **Decision:** Adopted a modular, component-based folder structure with clear separation of concerns (e.g., `components`, `screens`, `hooks`, `utils`).
*   **Context:** PRD specifies a single-screen calculator but emphasizes maintainability and user-friendliness.
*   **Consequence:** Enhances code organization, reusability, and scalability for future (though currently out-of-scope) feature additions, while remaining manageable for a simple app. Aligns with standard React Native project best practices.

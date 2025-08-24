### 2. Pages and Routes

The Calculator App is designed as a single-screen application, strictly adhering to the Product Requirements Document (PRD). Consequently, there are no internal routes or navigation mechanisms within the application.

*   **Main Screen**: `CalculatorScreen`
    *   **Purpose**: This is the sole user interface of the application. It will house all interactive elements including number buttons, operator buttons, clear/equals functions, and the display area for calculations. All user interactions and application state changes will occur entirely within this single view.
    *   **Location**: `src/screens/CalculatorScreen/CalculatorScreen.tsx`

The application's `App.tsx` component will directly render the `CalculatorScreen`, ensuring that the user immediately lands on the calculator interface upon launch, without any navigation overhead.

**ADR Log:**

*   **Decision:** No internal routing or multiple pages; the application will consist solely of `CalculatorScreen`.
*   **Context:** PRD explicitly states a "single-screen UI" and outlines no additional features requiring separate views (e.g., history, settings).
*   **Consequence:** Simplifies application architecture, reduces development overhead, and ensures direct compliance with the PRD. Any future expansion requiring multiple views would necessitate a significant architectural change to introduce a navigation library.
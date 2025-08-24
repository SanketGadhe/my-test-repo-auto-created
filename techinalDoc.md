### 3. Core Shared Components

Based on the single-screen UI and core functional requirements, the following minimal set of reusable UI components are proposed:

#### 3.1. Button
*   **Purpose**: A generic, interactive element for all calculator keys (numbers, operators, clear, equals).
*   **Key Props**:
    *   `label: string` (e.g., "7", "+", "C")
    *   `onPress: (value: string) => void`
    *   `type?: 'number' | 'operator' | 'action'` (for styling variations)
    *   `variant?: 'normal' | 'large'` (for size/spanning)
*   **Location**: `src/components/Button/Button.tsx`

#### 3.2. Display
*   **Purpose**: Renders the current input or calculation result.
*   **Key Props**:
    *   `value: string` (the number or result to show)
*   **Location**: `src/components/Display/Display.tsx`

#### 3.3. Keypad (Composite Component)
*   **Purpose**: Arranges and orchestrates multiple `Button` components into the calculator's grid layout, centralizing input handling.
*   **Key Props**:
    *   `onButtonPress: (value: string) => void` (callback for any button press within the keypad)
*   **Location**: `src/components/Keypad/Keypad.tsx`

These components promote modularity, reusability, and a clear separation of concerns, contributing to a maintainable and scalable frontend architecture for the single-screen calculator application.

**ADR Log:**

*   **Decision:** Identified and defined `Button`, `Display`, and `Keypad` as core shared components.
*   **Context:** PRD requires a single-screen UI with various input types (numbers, operators, clear, equals) and a display for input/results.
*   **Consequence:** Promotes component reusability, modularity, and a clear separation of UI concerns. This design allows for flexible styling based on button type and efficient management of user input within the `CalculatorScreen`.
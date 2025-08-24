### 4. State Management Approach

The state management for the Calculator App will be entirely centralized within the `useCalculator` custom hook (`src/hooks/useCalculator.ts`). This hook will encapsulate all core state variables and the logic required to update them based on user interactions.

#### 4.1. Key State Variables

The `useCalculator` hook will manage the following primary state variables using React's `useState`:

*   **`displayValue: string`**: The current value shown on the calculator's display (e.g., "0", "123.45", "Error").
    *   *Initial Value*: `"0"`
*   **`firstOperand: number | null`**: Stores the first number of a binary operation, or the result of a previous operation.
    *   *Initial Value*: `null`
*   **`operator: string | null`**: Stores the pending mathematical operation (e.g., "+", "-", "x", "÷").
    *   *Initial Value*: `null`
*   **`waitingForSecondOperand: boolean`**: A flag indicating if the next numerical input should start a new second operand (`true`) or append to the current `displayValue` (`false`).
    *   *Initial Value*: `false`

#### 4.2. Management and Update Mechanics

1.  **`useCalculator` Hook**:
    *   This hook will internally manage the above state variables.
    *   It will expose the current `displayValue` to be consumed by the `Display` component.
    *   It will expose a single public function, `handleButtonPress: (label: string) => void`, which `CalculatorScreen` will pass down to the `Keypad` component.

2.  **`CalculatorScreen` Integration**:
    *   The `CalculatorScreen` will import and invoke `useCalculator()`.
    *   It will destructure `displayValue` and `handleButtonPress` from the hook.
    *   The `displayValue` will be passed as a prop to the `Display` component.
    *   The `handleButtonPress` function will be passed as a prop to the `Keypad` component, allowing `Keypad` to relay all button presses directly to the central logic.

3.  **State Update Logic within `useCalculator`**:
    The `handleButtonPress` function will contain the core logic to parse the `label` of the pressed button and update the internal state accordingly:

    *   **Number/Decimal Input**: Appends digits or a decimal point to `displayValue`. Manages `waitingForSecondOperand` to start new numbers after an operator or equals.
    *   **Operator Input**: If `firstOperand` is `null`, the current `displayValue` becomes `firstOperand`. If an operator is already present, the pending calculation is performed first. The new operator is set, and `waitingForSecondOperand` is set to `true`.
    *   **Clear ("C")**: Resets `displayValue` to "0" and all other state variables to their initial `null`/`false` values.
    *   **Equals ("=")**: Parses the `displayValue` as the second operand, performs the calculation using `firstOperand`, `operator`, and the second operand. Updates `displayValue` with the result, sets `firstOperand` to the result, `operator` to `null`, and `waitingForSecondOperand` to `true` for subsequent operations.

This architecture ensures a clear separation between UI (rendering components) and business logic (calculator operations and state management), promoting maintainability and testability.

**ADR Log:**

*   **Decision:** Centralized state management within a `useCalculator` custom hook.
*   **Context:** PRD requires a single-screen calculator with complex input sequences and order-of-operations evaluation. A dedicated hook allows for clean separation of UI and business logic.
*   **Consequence:** Enhances modularity, testability, and readability of the `CalculatorScreen`. It provides a single source of truth for calculator state and a controlled mechanism for state updates in response to user input. Potential challenges with floating-point precision and advanced chained operations are noted for future consideration if PRD evolves.
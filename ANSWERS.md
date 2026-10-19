# ANSWERS.md — IT 120 Flutter Lab (Architecture, Widgets, and Basic UI)

**Student:** Ashlee R. Dotillos  
**Section:** ILGX3  
**Course:** IT 120 Integrative Programming and Technologies 2  
**Date:** October 19, 2026

---

## GitHub Repository Link
https://github.com/ashleedotillos-pixel/flutter_basic_lab


## Review Questions

### 1. Difference between StatelessWidget and StatefulWidget?
- **StatelessWidget:** A static widget whose properties cannot be altered once rendered on the screen. *Lab Example:* `ProfileCard` in Activity 1.
- **StatefulWidget:** A dynamic widget that can change its appearance while running because it manages data that updates. *Lab Example:* `WaterTrackerPage` in Activity 2.

### 2. Why is a StatefulWidget written as two classes?
- **First Class (`StatefulWidget`):** Acts as the immutable configuration layer whose primary task is instantiating the state via `createState()`.
- **Second Class (`State`):** Holds the mutable variables and contains the `build()` method. Triggering `setState()` inside this class alerts Flutter to re-run `build()` and reflect new values on screen.

### 3. Activity 2 — What happened when you changed `_glasses` outside `setState()`?
The variable value increased internally, but because `setState()` was omitted, Flutter did not register the change. As a result, `build()` was never triggered, leaving the user interface unchanged.

### 4. When is `build()` called?
It executes whenever `setState()` is called—such as every time a user taps the increment, decrement, or reset buttons. Each invocation logs a fresh message in the Debug Console.

### 5. Main axis vs cross axis of Row and Column?
- **Row:** Main axis runs horizontally (left-to-right), while the cross axis runs vertically (top-to-bottom).
- **Column:** Main axis runs vertically (top-to-bottom), while the cross axis runs horizontally (left-to-right).
- `MainAxisAlignment` arranges items along their primary layout direction, whereas `CrossAxisAlignment` aligns them perpendicularly.

### 6. Activity 3 — What happened when you removed `Expanded` from a StatBox?
The un-expanded box contracted to fit only its immediate contents, causing the remaining `Expanded` boxes to stretch unequally. `Expanded` ensures that children divide up the available row space evenly without layout overflows.

### 7. Why use `GridView.builder` instead of a `Column` with many children?
`GridView.builder` utilizes lazy loading to build only the elements currently visible on screen, keeping memory usage efficient. A standard `Column` attempts to render all items simultaneously without built-in scrolling, leading to layout overflow errors.

### 8. How do Stack and Positioned create the Best seller badge?
`Stack` layers widgets on top of one another from bottom to top. `Positioned` then anchors the badge widget using offset coordinates (e.g., `top` and `left`), placing it directly above the card's main contents.

### 9. Difference between customizing with ThemeData and a style on one widget?
- **ThemeData:** Applies global styling rules across all matching components in the entire application (e.g., setting `elevatedButtonTheme` to round all `ElevatedButton` shapes uniformly).
- **Widget-level Style:** Targets a specific instance locally (e.g., attaching a custom `TextStyle` directly to a single `Text` widget).

### 10. Dark-mode switch — which widget holds state, and how does the change reach MaterialApp?
The `_ThemeDemoAppState` class manages the `_isDark` boolean state. Toggling the switch triggers `_setDark`, which executes `setState()` to update `_isDark`. This re-evaluates `MaterialApp`'s `themeMode` parameter, causing the updated theme (light or dark) to propagate across the entire app.
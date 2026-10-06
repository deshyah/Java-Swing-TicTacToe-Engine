# Java Swing Tic-Tac-Toe Engine

A desktop GUI implementation of two-player Tic-Tac-Toe built with Java Swing. This project demonstrates Model-View-Controller (MVC) architectural principles by grafting an interactive graphical user interface onto underlying console game rules.

## 📌 Overview

This application transitions standard terminal-based Tic-Tac-Toe logic into a native desktop window. By decoupling presentation logic from game state management, the system enforces official game rules, handles turn transitions between Player X and Player O, and continuously evaluates board positions for wins and ties without relying on console outputs.

---

## ✨ Key Features

* **Subclassed UI Components (`TicTacToeTile`):** Extends standard `JButton` instances to encapsulate grid coordinate state (`row` and `col`), enabling direct integration between button UI events and board array indices.
* **Unified Event Handling:** Implements a shared `ActionListener` across the 3x3 grid matrix to capture user interactions cleanly and update game state efficiently.
* **Dynamic Win & Tie Detection:** Evaluates win paths after move 5 and evaluates tie states after move 7, recognizing both full-board ties and unachievable win scenarios.
* **Modal Dialog Feedback (`JOptionPane`):** Delivers instantaneous visual feedback for illegal move attempts, game wins, board ties, and play-again prompts using native GUI dialog boxes.
* **Separation of Concerns:** Organizes program architecture into clean view frames, reusable tile components, and execution entry points.

---

## 🛠️ Tech Stack & Architecture

* **Language:** Java 17+
* **GUI Framework:** Java Swing (`JFrame`, `JPanel`, `JButton`, `JOptionPane`, `GridLayout`)
* **Design Pattern:** Model-View-Controller (MVC)
* **IDE:** JetBrains IntelliJ IDEA

---

## 📁 Repository Structure

```text
├── TicTacToeRunner.java        # Application entry point that initializes and displays the GUI frame
├── TicTacToeFrame.java         # Main JFrame housing the 3x3 board matrix, quit button, and game logic
├── TicTacToeTile.java          # Custom JButton subclass maintaining matrix row and column indices
└── TicTacToeTileTester.java    # Diagnostic test suite for verifying tile component initialization
```

---

## 🚀 How to Run

### Prerequisites
* Java Development Kit (JDK 17 or higher installed)
* An IDE such as IntelliJ IDEA or VS Code

### Execution Steps
1. Clone the repository to your local system:
   ```bash
   git clone [https://github.com/deshyah/Java-Swing-TicTacToe-Engine](https://github.com/deshyah/Java-Swing-TicTacToe-Engine.git)
   ```
2. Open the project directory in your Java IDE.
3. Locate `src/TicTacToeRunner.java`.
4. Run the `main` method in `TicTacToeRunner.java` to launch the application frame.

---

## 💡 Key Engineering Takeaways

* **Model-View-Controller (MVC):** Isolating UI visual rendering (`View`) from game evaluation rules (`Model`) makes application components modular, maintainable, and extensible.
* **Component Subclassing:** Extending framework components like `JButton` allows custom objects to hold domain-specific data, eliminating the need for complex lookups or parallel data structures.
* **Event-Driven Programming:** Leveraging event listeners ensures the interface remains responsive while managing user input and state verification seamlessly in real-time.

# CSD121 Developer Journal

## 
Lab 4 - Build Automation and Testing

###
BOARD class encapsulate state and operations hence the use for the game (tictactoe)
PACKAGES organize code, keeping classes together and avoiding conflicts
each CLASS should have a single work i.e Calculator handles aritimetic, while MathUtils handles utility methods
STATIC METHODS - like "MathUtils.factorial()" can be 'static' so dont need to instantiate the class
ITERATIVE LOOPS are simple and effective for factorial or exponent calculations
JUNIT tests to ensure the expected results
ASSERTIONS to verify correctness and handle exceptions in tests (i.e assertEquals() and assertThrows()
JAVADOC to detail the code as in purpose, parameters, values, etc


## 
Lab 5 - Generalization and Polymorphism

###
Polymorphism lets different objects respond to the same method call in different ways.
The Player abstract class defines a common interface for all player types.
Subclasses implement strategy-specific logic inside pickNextMove.
The game engine doesn't care which player type is used, only that it has pickNextMove.
Abstraction hides unnecessary details and exposes only essential methods.
Inheritance allows reuse of the name property and constructor logic.
Board is a model class responsible only for game state, not player behavior.
Testing requires isolating logic inside each Player implementation.
LinusPlayer uses a deterministic strategy → always first empty cell.
Omola looks ahead one move using a copied board to avoid mutating state.
Copy constructor is essential for safe simulation of future moves.
The design follows the Single Responsibility Principle.
Adding new AI players requires no changes to existing game engine code.
Strategy pattern is visible: each Player is a different strategy object.
Good separation of concerns makes the code more maintainable and extensible.

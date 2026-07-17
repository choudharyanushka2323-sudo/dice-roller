# Dice Roller

A command-line dice rolling application written in Java. Generates a random roll between 1 and 6 and renders the result as an ASCII-art representation of a physical die face.



## Overview

Dice Roller is a lightweight, single-file Java utility designed to simulate a standard six-sided die roll. It combines Java's `Random` class with modern text block syntax to render clean, readable die faces directly in the terminal.

## Features

- Simulates a fair, random roll of a standard six-sided die
- Renders results as formatted ASCII-art die faces
- Zero external dependencies
- Single-file implementation for easy portability and review

## Requirements

| Requirement | Version |
|---|---|
| Java Development Kit (JDK) | 15 or later |

Java 15+ is required due to the use of [text blocks](https://docs.oracle.com/en/java/javase/15/text-blocks/index.html) (`"""`) for multi-line string literals.

Verify your installed version:

```bash
java -version
```

## Installation

Clone or download this repository, then navigate to the project directory:

```bash
cd dice-roller
```

## Usage

### Compilation

Compile the source file, specifying UTF-8 encoding to ensure correct rendering of the die's dot characters (`●`):

```bash
javac -encoding UTF-8 Main.java
```

### Execution

Run the compiled program:

```bash
java Main
```

### Sample Output

```
You rolled a 4:
| ●      ● |
|          |
| ●      ● |
```

## Project Structure

```
dice-roller/
├── Main.java     # Application entry point and core logic
└── README.md     # Project documentation
```

## Implementation Details

1. An instance of `java.util.Random` generates an integer in the range 1–6, inclusive.
2. Each of the six possible outcomes maps to a corresponding ASCII-art die face, defined using Java text blocks.
3. A `switch` statement selects the die face matching the generated roll.
4. The result is written to standard output.

## Roadmap

Planned enhancements under consideration:

- [ ] Support for rolling multiple dice in a single execution
- [ ] Interactive "roll again" loop
- [ ] Configurable die type (e.g., d4, d8, d20)
- [ ] Unit tests validating roll distribution and randomness

## Contributing

Contributions are welcome. Please open an issue to discuss proposed changes before submitting a pull request.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

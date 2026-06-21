# 🧮 Calculatrice

A console-based Java calculator supporting unary and binary operations, built with OOP abstraction and polymorphism.

## Features

- **Binary operations**: addition, subtraction, multiplication, division
- **Unary operations**: cosine, sine, logarithm, exponential, square root
- Input validation (rejects non-numeric input)
- Error handling (e.g. division by zero)
- Interactive loop — perform multiple calculations in one session

## Design

- `CalculMath` — interface defining a common `Calculer()` contract for every operation
- `OperationBinaire` / `OperationUnaire` — abstract base classes for two-operand and single-operand operations
- Each operation (`Addition`, `Division`, `Cos`, `Log`, ...) is its own class implementing the shared interface, accessed polymorphically through `CalculMath`

## Tech Stack

- **Java** (Java Platform Module System — `module-info.java`)

## Project Structure

```
Calculatrice/
└── src/
    ├── module-info.java
    └── Calculatrice/
        ├── Calculatrice.java         # Entry point / menu
        ├── CalculMath.java            # Operation interface
        ├── OperationBinaire.java      # Abstract: two-operand operations
        ├── OperationUnaire.java       # Abstract: single-operand operations
        ├── Addition.java
        ├── Soustraction.java
        ├── Multiplication.java
        ├── Division.java
        ├── Cos.java
        ├── Sin.java
        ├── Log.java
        ├── Exp.java
        └── Sqrt.java
```

## Run

```bash
cd src
javac -d ../bin module-info.java Calculatrice/*.java
java -cp ../bin Calculatrice.Calculatrice
```

## Author

**Naila** — [@BkNaila](https://github.com/BkNaila)

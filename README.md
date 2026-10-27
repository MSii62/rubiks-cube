# Rubik's Cube Solver

C++ Rubik's Cube solver with multiple cube representations, classic search solvers, a corner pattern database, and an OpenCV webcam scanner.

## Requirements

- C++14 compiler
- CMake 3.20+
- OpenCV (including video and highgui modules)
- A webcam for the scanner workflow

## Build

```bash
cmake -S . -B build
cmake --build build --config Release
```

## Run

Run from the project root so the bundled database is found:

```bash
./build/rubiks_cube_solver
```

A different pattern database can be supplied as the first argument:

```bash
./build/rubiks_cube_solver path/to/cornerDepth5V1.txt
```

Use `--help` to display usage. The scanner captures the faces in the order **U, L, F, R, B, D**. Keep the cube orientation consistent while scanning.

The database file is binary data despite its `.txt` extension.

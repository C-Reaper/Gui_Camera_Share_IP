# Project README

## Overview
This project is a camera test application that captures video from a webcam, displays it on the screen, and shares the video feed using OpenGL. It supports building for Linux, Windows, Wine, and WebAssembly.

## Features
- Captures video from a webcam.
- Displays the captured video in real-time.
- Shares the video feed using OpenGL.
- Supports debugging with a debugger like GDB for Linux and Wine for Windows.

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed: X11 (for GUI), png (for image handling), jpeg (for JPEG compression)

## Build & Run
- **Linux**:
  ```bash
  make -f Makefile.linux all
  ```
  To run the application:
  ```bash
  make -f Makefile.linux exe
  ```

- **Windows**:
  ```bash
  make -f Makefile.windows all
  ```
  To run the application:
  ```bash
  make -f Makefile.windows exe
  ```

- **Wine**:
  Cross-compiles for Windows using Wine.
  ```bash
  make -f Makefile.wine all
  ```
  To run the application:
  ```bash
  make -f Makefile.wine exe
  ```

- **WebAssembly** (Emscripten):
  Compiles to WebAssembly for browsers.
  ```bash
  make -f Makefile.web all
  ```
  To serve and run in a web browser:
  ```bash
  make -f Makefile.web exe
  ```

The build process compiles the source code using specific flags optimized for each platform, including AVX2 instructions for performance. The resulting executable is placed in the `build` directory.
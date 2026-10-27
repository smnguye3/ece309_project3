# ECE 309: Project 3 — Tool Use and Tool Registry
# Scarlett Nguyen
# smnguye3

This project is a C++ conversation harness that lets an "AI" model read and write files, list directories, and perform calculations. It has a custom hash table to manage tools and a two-stack calculator to evaluate arithmetics. 

## Build and Test
Open the terminal and enter: 
```bash
wsl
```

Install the build tools for a C++ compiler and CMake as needed using: 
```bash
sudo apt update
sudo apt install build-essential cmake
```

Change the directory to the current project folder:
```bash
cd .\<project_location>
```

Build and test the project by running the command lines in terminal:
```bash
rm -rf build-linux
cmake -S . -B build-linux -DMH_WERROR=ON
cmake --build build-linux -j
ctest --test-dir build-linux --output-on-failure
```

## Run
```bash
./build-linux/miniharness --script scripts/tools_demo.script --save transcript.txt
```

The replies are scripted due to it not being a live AI service. 
Enter the following in the exact order when prompted for user input:
1. show my todo
2. what is (12+30)*2/7
3. save a summary
4. bye


## Implementation and documentation
The following files were edited from the starter project folder:
- include/tools/tool_registry.h
- src/tools/tool_registry.cpp
- src/tools/workspace.cpp
- src/tools/calculator_eval.cpp
- tests/p3/test_p3.cpp
- docs/design-log-p3.md
- README.md

The following files were added from project 2: 
- include/core/conversation.h
- include/core/sentinel_scanner.h
- src/core/conversation.cpp
- src/core/sentinel_scanner.cpp
# llvm-function-pass
LLVM compiler pass that prints function names

Standalone/out-of-tree CMake project

My `llvm-function-pass` is outside of `llvm-project` source treee. Documentation says passes can be developed out of source against installed LLVM. I used `find_package(LLVM REQUIRED CONFIG)` to point my standalone pass at my source-built LLVM installation.

The CMake file tells your machine how to build the `FunctionNamePass.cpp` pass into a plugin that LLVM's `opt` tool can load. 


Workflow: 

`FunctionNamePass.cpp` = LLVM pass code

`CMakeLists.txt` = instructions for building pass

cmake command = reads `CMakeLists.txt` and creates build files

`cmake --build` = compiles `FunctionNamePass.cpp` into a plugin

`opt` = loads plugin and runs pass on LLVM IR


To copy files into commit directory: 

ditto /Users/daniel/llvm-from-source/llvm-project/FunctionNamePass \
      /Users/daniel/llvm-from-source/llvm-function-pass/

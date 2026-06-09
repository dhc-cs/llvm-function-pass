# llvm-function-pass
LLVM compiler pass that prints function names

Standalone/out-of-tree CMake project

My 'llvm-function-pass' is outside of 'llvm-project' source treee. Documentation says passes can be developed out of source against installed LLVM. I used find_package(LLVM REQUIRED CONFIG) to point my standalone pass at my source-built LLVM installation.

# C++ Environment Setup & Quickstart

This directory is configured for C++ development. It contains instructions for setting up the native compilation toolchain on macOS and running basic single-file programs.

---

## 🛠️ macOS Toolchain Setup

macOS utilizes the **Clang** compiler provided by Apple's command-line developer tools. 

### 1. Install Command Line Tools
Open your terminal and run the following command:
```bash
xcode-select --install
```
*A system dialog will appear asking for confirmation. Click **Install** and accept the license terms.*

### 2. Verify the Installation
Ensure the compiler is accessible by checking its version:
```bash
clang++ --version
```
You should see output indicating Apple LLVM/Clang is installed.

---

## 🚀 Running a Single-File Program

For simple, single-file scripts (like `main.cpp`), you can compile and execute directly from the terminal without complex build systems.

### 1. Sample Code (`main.cpp`)
Ensure your source file looks similar to this:
```cpp
#include <iostream>

int main() {
    std::cout << "C++ Toolchain is working perfectly!" << std::endl;
    return 0;
}
```

### 2. Compile and Run
Navigate to this directory in your terminal and execute the following commands:

```bash
# 1. Compile the source file into an executable named 'myprogram'
clang++ -std=c++17 main.cpp -o myprogram

# 2. Run the compiled executable
./myprogram
```

### 📝 Flag Breakdown
* `-std=c++17`: Specifies the C++ standard version to use (e.g., C++17, C++20).
* `-o myprogram`: Specifies the output binary name. If omitted, the compiler defaults to naming the output `a.out`.

---

## 📖 Documentation & References

For deeper customization, optimization flags, and standard library references, consult the official documentation links below:

* **[Clang Compiler User's Manual](https://clang.llvm.org/docs/UsersManual.html)** – Detailed guide on Clang diagnostics, target architectures, and compilation flags.
* **[LLVM Command Guide](https://llvm.org/docs/CommandGuide/index.html)** – Comprehensive reference for the underlying LLVM tool suite.
* **[Cppreference (C++ Reference)](https://en.cppreference.com/)** – The definitive community wiki for the C++ standard library (`std::cout`, containers, algorithms).
* **[ISO C++ Official Website](https://isocpp.org/)** – Current news, status, and FAQs regarding the ISO C++ Standard.

---

> [!NOTE]
> **Future Scope:** As this project grows beyond a single file, this directory will be updated to include a `Makefile` or `CMakeLists.txt` configuration to manage multi-file compilation, header dependencies, and build automation.

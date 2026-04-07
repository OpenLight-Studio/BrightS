# Project Structure

## Directory Layout

```
BrightS/
├── include/                # Public header files
│   └── kernel/            # Kernel public API headers
├── sys/                   # System source code
│   ├── kernel/            # Kernel core implementation
│   │   ├── core/          # Core kernel functions
│   │   ├── fs/            # Filesystem implementations
│   │   ├── dev/           # Device drivers
│   │   ├── net/           # Network stack
│   │   └── platform/      # Platform specific code (x86_64, etc)
│   └── user/              # Userspace libraries and utilities
├── tests/                 # Unit tests and integration tests
├── tools/                 # Build and utility scripts
├── docs/                  # Documentation
│   ├── api/               # API documentation
│   ├── build/             # Build instructions
│   └── design/            # Design documents
├── build/                 # Build output directory (not in git)
├── .github/               # GitHub Actions workflows
├── CMakeLists.txt         # Main CMake build configuration
├── LICENSE                # License file
└── README.md              # Project main readme
```

## File Naming Conventions

- Header files: `.h`
- Source files: `.c`
- Assembly files: `.S`

## Coding Standards

- Use 4 spaces for indentation, no tabs
- All public functions prefixed with `brights_` or component specific prefix
- Static functions do not use prefixes
- Use snake_case for function and variable names
- Use UPPER_CASE for macros and constants
- Header files have proper include guards
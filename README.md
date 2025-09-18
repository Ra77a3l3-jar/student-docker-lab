# 🚀 Academic Docker Environments

> **Complete containerized development environments for academic projects and learning**

[![My Skills](https://skillicons.dev/icons?i=docker,linux,py,c,bash&theme=dark)](https://skillicons.dev)

## 🎯 Overview

This repository contains a collection of Docker environments specifically designed for academic use, providing consistent and portable development setups for various programming languages and tools commonly used in computer science education.

## 🛠️ Supported Technologies

### Programming Languages
- **C/C++** - Complete GCC toolchain with debugging support
- **Java** - OpenJDK with Maven/Gradle build tools
- **Python** - Latest Python with pip and common libraries

### Additional Tools
- **Networking Tools** - Essential utilities for network programming and analysis
- **Development Utilities** - Code editors, debuggers, and productivity tools

## 📖 Use Cases

- **🎓 School Projects** - Ready-to-use environments for coursework
- **🧬 Learning Labs** - Isolated spaces for experimentation
- **🛠️ Development Environments** - Consistent setups across different machines
- **📝 Assignment Submission** - Reproducible environments for grading

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Containers
   ```

2. **Choose your environment**
   ```bash
   # Example: Start C++ development environment
   docker-compose up cpp-dev
   
   # Example: Start Python environment
   docker-compose up python-dev
   ```

3. **Start coding!**
   Your development environment is ready with all necessary tools pre-installed.

## 📁 Repository Structure

```
Containers/
├── README.md                    # This file
├── docker-compose.yml          # Multi-service orchestration
├── environments/               # Individual Docker environments
│   ├── cpp/                   # C/C++ development setup
│   ├── java/                  # Java development setup
│   ├── python/                # Python development setup
│   └── networking/            # Network tools and utilities
├── projects/                  # Sample projects and templates
└── docs/                      # Additional documentation
```

## 🐳 Container Features

### 🔧 Pre-configured Tools
- **Development**: Compilers, interpreters, build systems
- **Debugging**: GDB, debuggers, profiling tools
- **Networking**: Wireshark, netcat, curl, ping utilities
- **Utilities**: Git, vim, nano, htop, and more

### 📦 Isolated Environments
- No dependency conflicts between projects
- Clean slate for each assignment
- Consistent behavior across different host systems

### 🚀 Easy Setup
- One-command environment launch
- Persistent storage for project files
- Port forwarding for web applications

## 🎓 Educational Benefits

- **Consistency**: Same environment for all students
- **Portability**: Works on Windows, macOS, and Linux
- **Isolation**: No impact on host system
- **Reproducibility**: Exact same setup every time

## 🤝 Contributing

Feel free to contribute additional environments or improvements:

1. Fork the repository
2. Create a feature branch
3. Add your Docker environment
4. Submit a pull request

## 📚 Documentation

For detailed setup instructions and environment-specific documentation, check the `docs/` directory or individual environment README files.

## 🏷️ Tags

[![Tags](https://skillicons.dev/icons?i=docker,linux,py,c,bash,git&theme=dark)](https://skillicons.dev)

---

<div align="center">

**Happy Coding! 🎉**

*Made with ❤️ for academic excellence*

</div>

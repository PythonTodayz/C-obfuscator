PyToday - Python Obfuscation Tool

A powerful Python obfuscation and compilation tool that converts Python scripts into native executables with advanced protection features.

Features

· 🔒 Code Obfuscation: Multiple layers of obfuscation to protect source code
· 🏗️ Native Compilation: Compiles Python to C and then to native binary
· ⏰ Expiry System: Add time-based expiration to your scripts
· 🐍 Version Locking: Restrict execution to specific Python versions
· 🔧 Cross-Platform: Supports multiple architectures including arm64
· 🎨 Professional Output: Clean, branded executable packages

Requirements

System Requirements

· Python: 3.11+ (recommended 3.11 for best compatibility)
· GCC: C compiler for native binary generation
· Cython: For Python to C compilation

Python Dependencies

```text
cython>=3.0.0
```

Installation

1. Install System Dependencies

Ubuntu/Debian:

```bash
sudo apt update
sudo apt install python3 python3-pip gcc build-essential
```

CentOS/RHEL:

```bash
sudo yum update
sudo yum install python3 python3-pip gcc make
```

macOS:

```bash
brew install python3 gcc
```

2. Install Python Dependencies

```bash
pip3 install cython
```

3. Download PyToday

```bash
git clone https://github.com/PythonTodayz/C-obfuscator.git
cd pytoday
```

Usage

Basic Usage

```bash
python3 pytoday_obf.py
```

Command Line Options

The tool provides an interactive interface:

1. Input File: Enter the path to your Python script
2. Expiry Date: Optional - Add time-based expiration
   · Examples: 10min, 2h, 1d, 1month, 2y
   · Combinations: 1h 30min, 2month 15d
3. Python Version Lock: Optional - Restrict to specific Python version
   · Options: 3.11, 3.12, 3.13

Example Workflow

```bash
# Run the encoder
python3 pytoday_obf.py

# Follow the interactive prompts:
# [+] Enter file path to encode: /path/to/your/script.py
# [+] Add expiry date? (y/n): y
# [+] Expiry time: 30d
# [+] Add specific Python version? (y/n): y
# [+] Choose option (1/2/3): 1
```

Output

The tool generates:

· Encrypted file: compiled [ pytoday]_82827.py (final distributable)
· Temporary files: Automatically cleaned up after processing

Supported Python Versions

· ✅ Python 3.11 (Primary supported version)
· ✅ Python 3.12
· ✅ Python 3.13

Expiry System

```python
# Example expiry formats supported:
"10min"    # 10 minutes
"2h"       # 2 hours  
"1d"       # 1 day
"1month"   # 1 month
"1y"       # 1 year
"1h 30min" # Combined format
```

Architecture Support

· arm64 (Apple Silicon Macs)
· aarch64 (Linux ARM systems)
· x86_64 systems

How It Works

1. Obfuscation: Applies multiple encryption layers to source code
2. C Compilation: Uses Cython to convert Python to C code
3. Binary Generation: Compiles C code to native executable
4. Packaging: Creates self-extracting Python package
5. Cleanup: Removes temporary files automatically

Troubleshooting

Common Issues

1. Cython Installation Failed
   ```bash
   pip3 install --upgrade pip
   pip3 install cython --no-cache-dir
   ```
2. GCC Not Found
   ```bash
   # Ubuntu/Debian
   sudo apt install build-essential
   
   # macOS
   xcode-select --install
   ```
3. Permission Denied
   ```bash
   chmod +x pytoday_obf.py
   ```
4. Python Version Mismatch
   ```bash
   python3 --version  # Check version
   # Use Python 3.11 for best compatibility
   ```

Error Messages

· "Cython compilation failed": Check Cython installation
· "GCC not found": Install GCC compiler
· "File not found": Verify script path is correct
· "Unsupported architecture": Currently supports arm64/aarch64

Security Notes

· 🔐 Obfuscation ≠ Encryption: Code is obfuscated, not encrypted
· ⚠️ No Absolute Protection: Determined attackers can reverse engineer
· ✅ Best For: Deterring casual copying and basic protection

License

This tool is provided for educational and legitimate protection purposes only.

Support

For issues and questions:

1. Check troubleshooting section
2. Verify all dependencies are installed
3. Ensure Python 3.11+ is being used

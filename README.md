# KeyLogger 2nd Semester Project
# Keylogger Project - README

## Overview

This project is a simple keylogger implemented using x86 Assembly language and the Microsoft Macro Assembler (MASM). The keylogger captures keystrokes and logs them to a file. It utilizes the Windows API for capturing keyboard events and managing files.

## Prerequisites

- **Operating System**: Windows
- **Assembler**: MASM (Microsoft Macro Assembler)
- **Libraries**: Windows `.inc` files

## Files in the Project

- `keylogger.asm`: Main assembly source code file.
- `keylogger.inc`: Include file containing constant definitions and macros.
- `keylogger.def`: Definition file for linking.
- `keylogger.exe`: Compiled executable of the keylogger (provided for convenience, ensure you trust the source).

## Setup and Compilation

1. **Install MASM**:
   Ensure MASM is installed on your system. It is usually included with Microsoft Visual Studio as part of the "Build Tools".

2. **Directory Structure**:
   Organize your project directory as follows:
   ```
   Keylogger/
   ├── keylogger.asm
   ├── keylogger.inc
   ├── keylogger.def
   └── keylogger.exe (optional)
   ```

3. **Compile the Project**:
   Open the Developer Command Prompt for Visual Studio and navigate to the project directory. Run the following commands to assemble and link the project:
   ```sh
   ml /c /coff keylogger.asm
   link /subsystem:windows /defaultlib:user32.lib /defaultlib:kernel32.lib keylogger.obj /out:keylogger.exe
   ```

## Running the Keylogger

To run the keylogger, simply execute the compiled `keylogger.exe` file. The keylogger will start capturing keystrokes and log them to a file named `log.txt` in the same directory as the executable.

**Note**: Running a keylogger can be illegal and unethical if used without proper authorization. Ensure you have explicit permission to run this software on any computer.

## Source Code Overview

### keylogger.asm

This file contains the main logic of the keylogger. Key sections include:

- **Data Segment**: Definitions of data storage, including the buffer for keystrokes and the log file path.
- **Code Segment**: The main executable code, including initialization, message loop for capturing keystrokes, and file writing procedures.

### keylogger.inc

This include file contains constant definitions and macros used in `keylogger.asm`. It helps in organizing the code and making it more readable.

### keylogger.def

The definition file for linking, specifying the entry point and libraries to link against.

## Key Functions

- **WinMain**: The entry point of the application, initializing the keylogger and entering the message loop.
- **Message Loop**: Captures keyboard events and processes them.
- **WriteLog**: Writes captured keystrokes to `log.txt`.

## Legal and Ethical Considerations

This keylogger is intended for educational purposes only. Unauthorized use of keyloggers is illegal and unethical. Always obtain explicit permission from the owner of the computer system before running this software.

## Support

For any issues or questions, please contact the project maintainer at `raoumair554@gmail.com`.


**Disclaimer**: This software is provided "as-is" without any warranties. Use at your own risk. The author is not responsible for any misuse of this software.

---

By using this software, you agree to adhere to all applicable laws and regulations regarding the use of keylogging software.

---

This README provides a high-level overview of the keylogger project. For more detailed information, please refer to the comments within the source code files.

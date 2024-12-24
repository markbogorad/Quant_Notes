up:: [[Python MOC]]
tags:: #Programming 
# Sys Library
- It's a standard utility library that offers various tools to manipulate the Python runtime environment.
- Think of this as operating on your system enviroment
### Key Features of the `sys` Library

1. **System-Specific Parameters and Functions:**
   - **`sys.argv`:** A list of [[Command Line Arguments]] passed to a Python script. `sys.argv[0]` is the script name, and the subsequent values are the arguments provided to the script.
   - **`sys.exit()`:** Allows you to exit from Python. You can pass an optional argument, usually an integer, to indicate an exit status (0 for success, non-zero for an error).
   - **`sys.version`:** A string containing the version number of the Python interpreter and some additional information like build number and compiler details.
   - **`sys.platform`:** A string that gives a platform identifier, which can be useful when writing platform-specific code.

2. **Standard Input, Output, and Error Streams:**
   - **`sys.stdin`:** A file object corresponding to the standard input stream (usually the keyboard input).
   - **`sys.stdout`:** A file object corresponding to the standard output stream (usually the console output).
   - **`sys.stderr`:** A file object corresponding to the standard error stream (used for error messages).
   - These streams can be redirected, which is useful for logging or when running scripts that interact with files instead of the console.

3. **Python Path and Modules:**
   - **`sys.path`:** A list of strings that specifies the search path for modules. When you import a module, Python searches the directories in `sys.path` for the module. You can modify `sys.path` to include additional directories.
   - **`sys.modules`:** A dictionary that maps module names to the module objects that have already been loaded. This can be useful for checking if a module is already loaded or for reloading a module.

4. **Interpreter Information:**
   - **`sys.executable`:** The path to the Python interpreter executable. This can be useful for finding out which Python interpreter is running the script, especially in virtual environments.
   - **`sys.getsizeof()`:** Returns the size of an object in bytes. This is useful for memory management and understanding the memory footprint of Python objects.

5. **Exception Handling:**
   - **`sys.exc_info()`:** Returns information about the most recent exception caught by an except clause in the current thread. This includes the type, value, and traceback of the exception, which can be useful for debugging.

6. **Runtime Control:**
   - **`sys.setrecursionlimit()`:** Allows you to set the maximum depth of the Python interpreter stack, which is useful for controlling the depth of recursive functions.
   - **`sys.getrecursionlimit()`:** Returns the current value of the recursion limit.

7. **Memory Management:**
   - **`sys.getrefcount()`:** Returns the reference count for an object, which can help in understanding how many references to an object exist, aiding in memory management.
   - **`sys.getsizeof()`:** Returns the size of an object in bytes, helping to monitor memory usage.

8. **Interactive Interpreter:**
   - **`sys.ps1` and `sys.ps2`:** The primary and secondary prompts used in the interactive interpreter. You can customize these prompts in a Python session.

9. **Thread and Garbage Collection:**
   - **`sys.setswitchinterval()` and `sys.getswitchinterval()`:** Control how often the Python interpreter switches between threads. This can be useful for fine-tuning performance in multi-threaded applications.
   - **`sys.gettrace()` and `sys.settrace()`:** Allows you to set a trace function, which will be called on various events during program execution, primarily used for debugging.

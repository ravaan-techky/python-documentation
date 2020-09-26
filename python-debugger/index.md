## Python

### Python Debugger:
 - For python dbugger you need to import pdb module.
 - pdb module is help to debug python code with followinf methods:

 | method | description |
 | --- | --- |
 | pdb.run(statement, globals=None, locals=None) | Execute the statement (given as a string or a code object) under debugger control. The debugger prompt appears before any code is executed; you can set breakpoints and type continue, or you can step through the statement using step or next (all these commands are explained below). The optional globals and locals arguments specify the environment in which the code is executed; by default the dictionary of the module __main__ is used. (See the explanation of the built-in exec() or eval() functions.) |
 | pdb.runeval(expression, globals=None, locals=None) | Evaluate the expression (given as a string or a code object) under debugger control. When runeval() returns, it returns the value of the expression. Otherwise this function is similar to run(). |
 | pdb.runcall(function, *args, **kwds) | Call the function (a function or method object, not a string) with the given arguments. When runcall() returns, it returns whatever the function call returned. The debugger prompt appears as soon as the function is entered. |
 | pdb.set_trace(*, header=None) | Enter the debugger at the calling stack frame. This is useful to hard-code a breakpoint at a given point in a program, even if the code is not otherwise being debugged (e.g. when an assertion fails). If given, header is printed to the console just before debugging begins. |
 | pdb.post_mortem(traceback=None) | Enter post-mortem debugging of the given traceback object. If no traceback is given, it uses the one of the exception that is currently being handled (an exception must be being handled if the default is to be used). |
 | pdb.pm() | Enter post-mortem debugging of the traceback found in sys.last_traceback. |

 **Note:** Most of the time we use set_trace method from pdb module to debug and check value of current function which is in execution.
 
 Example:
 
 Before setting debugging, -
 
 ![python_debugger_operations](../../images/python_debugger_1.png)
 
 After setting debugging, -
 ![python_debugger_operations](../../images/python_debugger_2.png)


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)

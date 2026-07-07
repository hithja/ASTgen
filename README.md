# ASTgen
Abstract Syntax Tree generator on Python for C++
## Usage
First, create JSON config.
Example:
```JSON
{
    "name": "Expr",
    "sys_includes": ["vector",],
    "user_includes": ["Token.hpp"],
    "types": {
        "Binary": "Expr left, Token oper, Expr right",
        "Unary": "Token oper, Expr right",
        "Literal": "Object value",
        "Grouping": "Expr expr"
    }
}
```
- `name` - name of base class
- `sys_includes` - system header files import (`#include <LIB>`)
- `user_includes` - user header files import (`#include "LIB.hpp"`)
- `types` - AST types and their fields

You can check my config ![here](https://github.com/hithja/ASTgen/blob/main/Expr.json). <br>
Enter `python3 ./ASTgen.py CONFIG_NAME.json <output directory>` to generate AST header.

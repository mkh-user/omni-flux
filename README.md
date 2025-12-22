# OmniFlux
OmniFlux is a high-level programming language that combines the simplicity of scripting languages with advanced control and powerful features.  

> [!Important]  
> This is currently more of a concept than a fully developed project. See the License and Markdown files for more information.

## Introduction

### Design
OmniFlux is designed to be a versatile and flexible language that makes programming easier for everyone. With the rise of AI-assisted coding (including Vibe Coding), OmniFlux aims to simplify code generation, review, and modification. It is highly adaptable, capable of compiling into multiple languages, and allows for easy implementation of custom features.

### Philosophy
OmniFlux is extremely simple yet highly powerful in practice. The philosophy behind OmniFlux is to achieve goals with minimal effort while still offering full control when needed. In short: everything is infinitely simple until you switch to manual mode—then the control is entirely yours.  

OmniFlux is suitable both for learning programming and for building complex systems.

### Comparison
OmniFlux learns from other languages to improve itself, while maintaining a unified environment where all features are consistent and aligned with its core vision. As a high-level language, it offers simple syntax and manages many operations by default.

## Name
OmniFlux blends **“Omni”**—meaning universal—with **“Flux,”** representing flow and flexibility. The name reflects the vision of a language that is comprehensive yet adaptable, evolving fluidly while offering broad versatility.

## Inspiration
OmniFlux is inspired by Python, GDScript, C++, Java, and others. It attempts to overcome their limitations by combining their strengths. At the same time, it remains a standalone language with unique features and structures rarely seen elsewhere, most of which focus on enhanced code control—a major advantage for a scripting language.

## Features

### Syntax
OmniFlux uses English keywords (often abbreviated) and standard symbols from other languages. Its syntax is similar to Python and GDScript: keywords and declarations define expressions, and indentation separates code blocks.

### Special Features
> [!Note]  
> For more details on special features, see the sample files and syntax guide.

OmniFlux offers unique features focused on simplicity and programmer quality of life (common features from Python and others are omitted here):
- Built-in docstring formatter  
- Keywords for navigation and code organization  
- Expression validation wherever possible  
- Dynamic typing by default  
- Optional setters & getters for variables  
- Rich, dynamic, and composite data types:  
  - States  
  - Sets  
  - Pairs  
  - Triplets  
  - Char  
  - Multi-dimensional arrays  
  - Tables  
  - Queues  
  - Callable  
  - Color  
- Full optional support for static typing  
- Simple public & private access modifiers  
- Variable argument functions  
- Named parameters  
- Lambda functions  
- Signals  
- Powerful enums:  
  - Anonymous enums  
  - Anonymous shadow  
  - Named enums  
  - Enums as types  
- `switch` / `case` / `default`  
- Advanced loops with monitoring  
- Bitwise operations  
- `in` / `not in`  
- `try` / `except` / `else` / `finally`  
- `raise` / `assert`  
- Internal logging  
- Simple I/O  
- `with` environment manager  
- Internal file management  
- Object-oriented programming  
- `class` / `extends`  
- `import` / `exclude`  
- Static variables and functions  
- Static constructors  
- Constructors with overloading  
- `static` blocks  
- Inner classes  

## Install
OmniFlux is not yet implemented and currently has no public interpreter or compiler.

## Examples

### Hello World
```omni
print("Hello World!")
```

### Constructor Overloading
```omni
class User

var name: string
var age: int

constructor(): # Simple constructor
    self.name = "Unknown"
    self.age = 0

constructor(name: string): # Constructor with parameter
    self.name = name
    self.age = 0

constructor(name: string, age: int): # Overloading
    self.name = name
    self.age = age

constructor(copy: User): # Copy constructor
    self.name = copy.name
    self.age = copy.age
```

### Advanced Loop Monitoring
```omni
for i in range(1, 10):
    for j in range(1, 10) as inner_status: # optional advanced loop monitoring
        if i == j:
            break(2) # breaks two loops
        if i == 9 and j == 9:
            continue(2) # skips this iteration and the next one
        if i == 10:
            continue(loops=2) # skips this iteration and the current iteration in outer loop
    match inner_status.status:
        case LOOP_STATUS_COMPLETE:
            print("Inner loop completed successfully.")
        case LOOP_STATUS_FULL_SKIP:
            print("Inner loop was never executed.")
        case LOOP_STATUS_HAS_SKIP:
            print(f"Inner loop was skipped {inner_status.skip_count} times.")
        case LOOP_STATUS_BREAK:
            print(f"Inner loop broke at iteration {inner_status.break_iteration}.")
    print(f"Inner loop executed: {inner_status.iter_executed} of {inner_status.iter_count} ({inner_status.iter_completely_executed} iterations completed)")
else:
    print("Nothing") # when loop count is 0 (e.g. for i in []), same as LOOP_STATUS_FULL_SKIP
```

## Project Status
This project is currently a concept. The most active area of development is design.

### Future Improvements
- **Design:**  
  - Decide whether OmniFlux will be a compiler, interpreter, or both  
  - Plan for async functionality  
- **Core:**  
  - Choose the primary implementation language  
  - Implement interpreter/compiler  

## Contribution
Since OmniFlux is currently just a concept without even an experimental interpreter or compiler, contributions are more valuable in improving the concept rather than implementation. Contributions can be made via PRs and issues.

## License
```text
OmniFlux Proprietary Draft License
Copyright © 2025 Mahan Khalili

1. Ownership
All rights related to the design, innovations, syntax, and features described in this project
are the intellectual property of the OmniFlux project. No part of this project or its
innovations may be used, modified, or redistributed without written permission from the owner.

2. Usage Restrictions
- Use of this project and its innovations is permitted exclusively within the OmniFlux project.
- Any use in other projects, whether commercial or non-commercial, is strictly prohibited
  until the official release of OmniFlux stable version 2.0.
- Reverse engineering, copying, or reproducing parts of this project outside OmniFlux
  constitutes a violation of this license.

3. Distribution
- Redistribution of this project or any part of it without written permission from the owner
  is prohibited.
- Public release is only permitted in the official OmniFlux project form.

4. Liability
This project and its innovations are provided "as is." The owner assumes no responsibility
for errors, defects, or damages resulting from unauthorized use.

5. Term
This license remains valid until the official release of OmniFlux stable version 2.0.
After the release of version 2.0, new licensing terms may replace this license.

6. Governing Law
This license is governed by international intellectual property and copyright laws,
as well as the local laws of the owner’s jurisdiction.
```

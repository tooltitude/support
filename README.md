# Tooltitude for Go

[Tooltitude for Go](https://www.tooltitude.com) is a productivity extension for the Go programming language.

## Features

### CodeLens Providers in Project Modules
Gain insights into your codebase, and understand usage patterns for functions, methods, fields, and interfaces.
We have CodeLens providers which help you navigate code and see what's going on in the code base
<p>
<img src="images/lenses.webp" alt="demonstration of CodeLens"  style="padding: 2px" width="540" height="339">
</p>

### Code Inspections
From unused initializations and writes to shadowed variables, unhandled errors, and deprecated symbols, our inspections help you enhance your code.

<p>
<img src="images/inspections.webp" alt="demonstration of code inspections"  style="padding: 2px" width="540" height="339">
</p>

### References View
Get more information than the built-in references popup. References view allows you to see not only the file where the reference is located, but its package, function. Note: it works only with Tooltitude CodeLens providers.

<p>
<img src="images/refs-view.webp" alt="demonstration of references view"  style="padding: 2px" width="540" height="339">
</p>

### Debug Individual Table Driven Tests
Debug Individual table driven tests with our debugging CodeLens.

<p>
<img src="images/table-driven.webp" alt="demonstration of table driven test debug"  style="padding: 2px" width="540" height="339">
</p>

### Postfix Completions
Write code faster by using familiar dot notation to generate boilerplate code: generate statements, call library functions, iterate collections and more.

<p>
<img src="images/postfix.webp" alt="demonstration of postfix completion"  style="padding: 2px" width="540" height="339">
</p>

### Code Actions
Make common code changes with confidence: handle errors, manipulate variables, transform expressions and more.

<p>
<img src="images/code-actions.webp" alt="demonstration of code actions"  style="padding: 2px" width="540" height="339">
</p>

## Premium Features
We have a set of premium features which are available for a license fee:
Learn more about them https://www.tooltitude.com/pricing

### ⭐ CodeLens Providers in Dependencies
Gain insights into your dependencies, understand usage patterns for functions, methods, fields, and interfaces.

<p>
<img src="images/lenses.webp" alt="demonstration of CodeLens"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Inline Values In The Debugger
See variable and parameter values right in your editor

<p>
<img src="images/inline-values.webp" alt="demonstration of inline values"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Workspace Wide Unused Symbols Report
Find entities with no source code reference in the whole workspace

<p>
<img src="images/unused-ws.webp" alt="demonstration of workspace wide unused symbols report"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Inlay Reference Counters
Save vertical space with inlay reference counters

<p>
<img src="images/inlay-refs.webp" alt="demonstration of inlay reference counters"  style="padding: 2px" width="540" height="339">
</p>

### Full LSP mode
Tooltitude for Go could act not only as a productivity extension, but as a language server which provides basic LSP functionality. We use it internally to debug code when it doesn't behave as expected. It could also be used in a resource constrained environment where running both gopls and Tooltitude isn't feasible.

This mode is activated only if the official Go extension is disabled. It's possible to disable it either globally or on a per-workspace basis. Then, reload the editor to activate the mode.

## Feature list
Features with ⭐ require a subscription. Features may have limitations. Software is subject to EULA.

- CodeLens Providers
  - Reference counts for functions, methods, interfaces, fields, and interface methods in project modules (⭐ in deps)
  - Implementers count for interfaces and interface methods in project modules (⭐ in deps)
  - Implemented intefaces counts for types and methods in project modules (⭐ in deps)
  - ⭐ Package imports
  - ⭐ Reference counts for fields (turned off by default, use tooltitude.overlays.refs.fields)
  - Method counts for non interface types
  - Run or debug project packages
  - Debug table driven tests
  - Implement interface
  - Move declaration (within the same package)
  - ⭐ Move declaration (between packages)
  - Change signature (for private functions, and non interface methods)
  - ⭐ Change signature (for public functions, and non interface methods)
  - Protobuf support
    - Navigation from protobuf files to generated elements for messages, services, and enums
    - ⭐ Go reference counts for messages, enums, and client call counts for rpc methods in protobuf files
    - ⭐ Go implementation counts for gRPC server implementations of services, and rpc methods
- Inlay Hints
  - Build tag diagnostics
  - ⭐ Option to show reference counts in inlay hints (turned off by default, use tooltitude.inlay.refs)
- Helpers
  - ⭐ Automatic update of imports on folder moves and renames
  - ⭐ Automatic update of references on file moves
- Debugging
  - ⭐ Inline values in the debugger
- Inspections
  - Unused assignments/initializations
  - Unused symbols for files and paths
  - ⭐ Unused symbols for the workspace
  - Unreachable code
  - Unhandled errors
  - Variable shadows
  - Deprecated symbols (only if vscode-go isn't installed)
- Postfix Completions
  - Completion for builtin types to invoke standard functions involving these types. As an example, you could write "abc".ToLower and transform it to strings.ToLower("abc)
  - .if for "if expr { }"; .ifn for "if !expr { }" 
  - .ifnil for "if expr == nil { }"; .ifnnil for "if expr != nil { }"
  - .ifempty for "if len(expr) == 0 { }"; .ifnempty for "if len(expr) != 0 { }"
  - .parens for "(expr)"
  - .print, .println, .panic, .len, .cap, .close, .new, .delete, .append or .make to call the corresponding standard library functions
  - .for, .switch, .return, and .defer to complete the corresponding statements
  - .for_range for automatic creation of iteration variables based on expression type
  - .&, .!, .*, .<- for &expr, !expr, *expr, <-expr
  - .var and .const for "var/const id = expr"
  - .=/:= for "id = expr" / "id := expr"
- Code Actions
  - Inline function for package private functions
  - ⭐ Inline function for public functions
  - Inline method for package private methods
  - ⭐ Inline method for public methods
  - Handle error (with panic, return err, wrapped error)
  - Show references in project modules (⭐ in deps)
  - Show implementations/implementers for methods/interfaces in project modules (⭐ in deps)
  - Show implemented interfaces/implementing types in project modules (⭐ in deps)
  - Show type methods in project modules (⭐ in deps)
  - ⭐ Show package imports
  - Move declaration
  - Change signature (for functions and non interface methods)
  - Rename
  - Extract variable
  - Inline variable
  - ⭐ Extract embedded type
  - ⭐ Inline embedded struct/interface 
  - ⭐ Synchronize receiver names
  - Run/debug a main method
  - Run/debug a test method
  - Apply De Morgan laws
  - Merge string literals
  - Flip comma
  - Invert if conditions
  - Convert else { if {to else if {
  - Unwrap else code action (return in the if-true block)
  - Iterate over collection
  - Convert raw string <-> string literal
  - Convert separated decimal integer literal <-> non separated integer decimal literal (i.e. 1000000 <-> 1_000_000)
  - Add/remove octal prefix in octal literals (i.e. 0100 <-> 0o100)
  - Convert defer to “multiline” defer (via closure)
  - Add else to if
  - Add channel receive result to assignment
  - Remove redundant parenthesis
  - Convert interface { } to any
  - Convert assignment to unresovled variable to short var decl
  - Flip binary operation, i.e. a + b -> b + a and a > b to b < a
  - Convert x += a to x = x + a and back, as well as with other operations
  - Anonymous func single line to/from multiline func
  - Add var type
  - Create unresolved var
  - Rune literal to/from string literal
  - Var to/from short var declaration
  - Split field
  - Rewrite dot import
  - Remove unused import
  - Remove unused imports
  - Remove broken import
  - Remove broken imports
  - Sort imports
  - Merge imports
  - Organize imports
  - Generate getter/setter
  - Generate stub interface for a type
  - Move declaration up/down
  - Remove all tags
  - Add json tag
  - Add import
  - Add missing return statement (the full lsp mode only)
- Language Services
  - Code completion
  - Code navigation
    - Go to definition
    - Go to implementation
    - Go to type (if a variable type is a slice, an array, a pointer, a or combination of thereof, go to type definition goes to the first navigatable component type)
  - Find references
  - Parameter hints
  - Limited error checking
  - Formatting
  - Workspace symbol navigation
  - Selection range (navigate up/down)
  - Documentation in hover
  - Documentation in completion
  - Outline + related features
  - Local var and parameter rename
  - ⭐ Incoming/outgoing calls (we overapproximate by including all function/methods refs as calls)
- Build Tags (Only the `//go:build` form, and inferred tags based on a file name are supported. The `//+build` form isn't supported)
  - Go env based tags, i.e. tags for os, cpu architecutre, go version, and others
  - ⭐ Custom tag aware language server (via the `tooltitude.build.tags` setting)
  - ⭐ Custom tag aware Run/Debug actions (via the `tooltitude.build.tags` setting)
  - Inferring the `tooltitude.build.tags` setting from the vscode for Go configuration if the setting value is null
  
## Data
We collect anonymous usage data. To opt-out of data collections, set the `telemetry.telemetryLevel` setting to `off` as directed by the Visual Studio Code documentation before installing the extension, or at any time after the installation: https://code.visualstudio.com/docs/supporting/faq#_how-to-disable-telemetry-reporting 
You could read more about our privacy policy here: https://www.tooltitude.com/privacy

## Support Resources
* You could ask for help or suggest a feature by creating an issue in this repository: https://github.com/tooltitude/support/issues/new/choose
* You could join our Discord community: https://discord.gg/f9MHBXsVwr

## Other Links
* Visit our site: https://www.tooltitude.com/
* Follow us on X: https://twitter.com/tooltitude

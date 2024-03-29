# Tooltitude for Go

[Tooltitude for Go](https://www.tooltitude.com) is a productivity extension for the Go programming language. It helps you write better code faster. The extension is being actively developed so stay tuned for new features (Twitter is the best place to do so https://twitter.com/tooltitude). 

## Features

### CodeLens providers
Gain insights into your codebase, and understand usage patterns for functions, methods, fields, and interfaces.
We have CodeLens providers which help you navigate code and see what's going on in the code base
<p>
<img src="images/lenses.webp" alt="demonstration of code lens"  style="padding: 2px" width="540" height="339">
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
Debug Individual test driven tests with our debugging code lens.

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

### ⭐ Keyboard navigation for Tooltitude CodeLens providers
Use code actions to navigate to methods, implementing interfaces/methods, implemented interfaces/methods. Don't break your flow by using a mouse or touchpad.

<p>
<img src="images/nav-kb.webp" alt="demonstration of navigation via keyboard"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Inline Values In The Debugger
See variable and parameter values right in your editor

<p>
<img src="images/inline-values.webp" alt="demonstration of inline values"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Workspace Wide Unused Symbols Report
Fine entities with no source code reference in the whole workspace

<p>
<img src="images/unused-ws.webp" alt="demonstration of workspace wide unused symbols report"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Inlay Reference Counters
Save vertical space with inlay reference counters

<p>
<img src="images/inlay-refs.webp" alt="demonstration of inlay reference counters"  style="padding: 2px" width="540" height="339">
</p>

### ⭐ Run/Debug from a Keyboard
Run and Debug tests, and main methods from a keyboard. Don't break your flow by using a mouse or touchpad.

<p>
<img src="images/run-debug-kb.webp" alt="demonstration of running and debuggin using only keyboard"  style="padding: 2px" width="540" height="339">
</p>

## Feature list
Features with ⭐ require a subscription. Features may have limitations. Software is subject to EULA.

- CodeLens Providers
  - Reference counts for functions, method, interfaces, fields, and interface methods
  - Implementers count for interfaces and interface methods
  - Implemented intefaces for types and methods
  - ⭐ Package imports
  - ⭐ Reference counts for fields (turned off by default, use tooltitude.overlays.refs.fields)
  - ⭐ Option to show reference counts in inlay hints (turned off by default, use tooltitude.inlay.refs)
  - Method counts for non interface types
  - Run or debug main packages
  - Debug table driven tests
  - Implement interface
  - Move declaration (within the same package)
- Helpers
  - ⭐ Automatic update of imports on folder moves and renames
- Debugging
  - ⭐ Inline values in the debugger
- Inspections
  - Unused assignments/initializations
  - Unused symbols for files and paths
  - ⭐ Unused symbols for workspace
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
  - Handle error (with panic, return err, wrapped error)
  - Show references
  - ⭐ Show implementations/implementers for methods/interfaces
  - ⭐ Show implemented interfaces/implementing types
  - ⭐ Show type methods
  - ⭐ Show package imports
  - ⭐ Move declaration (within the same package)
  - Rename
  - Extract variable
  - Inline variable
  - ⭐ Extract embedded type
  - ⭐ Inline embedded struct/interface 
  - ⭐ Synchronize receiver names
  - ⭐ Run/debug a main method
  - ⭐ Run/debug a test method
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
  - Rune literal to/from string literal
  - Var to/from short var declaration
  - Split field
  - Rewrite dot import
  - Remove unused import
  - Remove unused imports
  - Merge imports
  - Generate getter/setter
  - Generate stub interface for a type
  - Move declaration up/down

## Data
We collect anonymous usage data in order to improve our products. To opt-out of data collections, turn off application-wide telemetry setting in VS Code as directed by the VS Code documentation before installing the extension, or at any time after the installation: https://code.visualstudio.com/docs/supporting/faq#_how-to-disable-telemetry-reporting Our extension respects this global setting as directed by extension guidelines published by Microsoft. You could read more about our privacy policy here: https://www.tooltitude.com/privacy

## Support Resources
* You could ask for help or suggest a feature by creating an issue in this repository: https://github.com/tooltitude/support/issues/new/choose
* You could join our Discord community: https://discord.gg/f9MHBXsVwr

## Other Links
* Visit our site: https://www.tooltitude.com/
* Follow us on Twitter: https://twitter.com/tooltitude

-mackle code style
==================

Somewhat arbitrary, especially when it comes to prefixes, but:

1. Make liberal use of aliases like `Macro` in lieu of `groff`'s overly
   terse defaults.
2. Use long-form, descriptive names for macros, strings and registers -
   with the only exception of registers meant to hold temporary results,
   which can be named `r` (possibly under the module's namespace).
3. Use `PascalCase` for macro names, and `serpent-case` for registers.
4. Divide the macros in meaningful modules, and namespace anything that
   should not be used directly by the user by prefixing it with the
   module name and one asterisk.  
5. Prefix internal-only macros/variables with a `@`.

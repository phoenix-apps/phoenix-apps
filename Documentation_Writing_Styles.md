# Documentation Writing Styles

This document contains the language styles for the documentation in all Phoenix libraries.
Use XML wherever possible in public libraries (such as Phnx libraries) to document the library, and use wherever the purpose of the code (or the range of argument or exceptions) is not obvious in internal libraries, and make sure to update the documentation for the code you're editing whenever you're editing something.

You can read more about how to write XML documentation for C# [here](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/documentation-comments)

* Our documentation follows closely to the language, semantic styles and specification used by Microsoft. You can read their specification [here](https://docs.microsoft.com/en-us/style-guide/developer-content/), and we recommend reading it through if you haven't seen it before, prior to working on any of our projects

* Never refer to an extension method's first parameter as `this` in comments or documentation, always use `paramref` to refer to it

* Use `<see cref>` and `<see langword>` wherever appropriate, including for `null`, `true` and `false` in XML comments

* Self-close XML tags whenever possible (such as `see cref`, `paramref`, `typeparamref` and more)

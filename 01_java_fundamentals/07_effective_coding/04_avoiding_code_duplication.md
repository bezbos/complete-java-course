# Avoiding Code Duplication

Maintaining a clean and efficient codebase involves careful management of technical debt. Code duplication is a common source of technical debt, where developers often resort to copying and pasting code blocks instead of creating reusable methods and classes. This practice complicates code maintenance and updates.

In a previous lesson, we demonstrated the extraction of common logic for order calculation, highlighting the risks of duplicating the same logic across different code sections. Manual updates to all duplicates increase the chances of inconsistencies and errors.

Inconsistencies can result in unpredictable behavior, where a feature works correctly in some instances but remains bugged in others. Fixing a bug in one part may not propagate to all occurrences, causing confusion among team members.

Striking a balance is crucial; not every piece of code should be reused everywhere. Reusing methods or classes excessively can introduce problems, especially when modifying the logic affects unexpected areas.

A general guideline is to avoid reusing a method or class when adding new functionality significantly complicates the existing code. If handling multiple conditions or responsibilities overwhelms the method or class, reconsider reusability.

In essence, when a method or class becomes too complex or takes on too many responsibilities, it's time to stop reusing it.

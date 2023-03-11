# Refactoring

Refactoring is an ongoing editing process in software development. As time goes on, code changes and grows. This can cause issues if it isn't updated to clean up after those changes and make space for future growth.

## When to Refactor?

### Indicators that refactoring is needed

- Code smell: Code smells are patterns in the code that indicate a problem with the design or implementation of the code.
- Difficulty maintaining or modifying code: Without routine refactoring, code becomes harder and harder to work with. Things like time constraints can cause devs to take reasonable shortcuts, or business needs may change.
- Code reuse: Follow DRY (Don't Repeat Yourself). If there's a lot of duplicated code in your codebase, that can indicate that refactoring is needed. It may be worth including a bit of code twice, but it's time to refactor if the same code is used three or more times.
- Performance issues: Optimization is often skipped in an initial build because it can be challenging to predict where performance issues will arise. Once a feature has been out for some time, refactor any spots where the application is slow or consuming more resources than necessary.
- Inconsistent or non-standard code: Sometimes, a previous dev wanted to use something other than the language's standard naming schemes. There may have been a hacky workaround to deal with a bug in an underlying library. Whatever the reason, a lot of code has temporary patches that will hurt in the long run if not addressed.

### Risks of not refactoring

### Balancing refactoring with feature development

- Technical debt: Not refactoring can lead to accumulating technical debt. Technical debt refers to the cost of maintaining and improving software caused by short-term solutions or neglecting to refactor.
- Decreased productivity: Code that is hard to read or understand can reduce productivity. Developers may spend more time trying to understand the code or fixing bugs caused by the complexity of the code.
- Increased bugs: Not refactoring can lead to an increase in bugs. If the code is not well-designed, it can lead to unexpected behavior, bugs, and crashes.
- Difficulty adding new features: If the codebase is well-designed, it can be easier to add new features. Adding new features to poorly designed code can create even more complex code, leading to a vicious cycle of technical debt.
- Reduced code quality: Over time, code that is not refactored can become cluttered and difficult to understand.

## Challenges of Refactoring

- Fear of breaking code: Refactoring can be risky because it involves changing code that is already working. There's a risk of introducing new bugs or breaking existing functionality, leading to delays and additional work.
- Time and resources: Refactoring can be time-consuming and require significant resources, especially if the codebase is large or complex. Developers may need to balance the time spent on refactoring with other development tasks and priorities.
- Resistance from team members: Refactoring can be challenging when team members have different opinions about the best approach. Resistance to refactoring can be caused by various factors, including the fear of change, a lack of understanding of the benefits of refactoring, or concerns about the impact on project timelines.
- Business pressure: There may be pressure to deliver new features quickly, making it difficult to prioritize refactoring. It can be challenging to balance the need to maintain the codebase with the need to provide new features and meet business objectives.

## Common Refactoring Techniques

- Extract Method: When a method becomes large, it becomes harder to understand. Breaking chunks out into seperate functions makes the larger process more manageable, even if the new function is only used in that one place. Depending on the testing strategy, this can also create an opportunity to test that code in isolation.
- Rename Method/Variable/Class: This involves renaming a method, variable, or class to better reflect its purpose or functionality.
- Replace Magic Number with Symbolic Constant: This replaces hardcoded values in the code (known as magic numbers) with named constants.
- Move Method/Field: Sometimes, a method has changed so much that it no longer makes sense to keep it where it is. Another time this could be useful is if you've added something like a service class to centralize bits of logic.
- Introduce Parameter Object: The number of parameters for a method sometimes gets quite large. Grouping all the parameters into a specialized object makes it easier to understand what the options are for the method and keeps the function definition tidy. Having a large number of parameters can also indicate code smell, so balance this technique with possibly rearranging code into separate pieces.
- Replace Conditional with Polymorphism: Sometimes conditional statements have many options (think something like a case statement). Instead, creating subclasses that encapsulate the conditional logic may be better.
- Extract Class: This technique involves creating a new class to encapsulate related functionality.
- Simplify Method: When a feature is no longer used, it should be removed from the codebase. It's also important to watch for code that may get missed in the initial cleanup. Use version control history to keep track of old code "just in case" rather than having blocks of commented-out code.
- Remove Duplication: This technique identifies and removes duplicated code in the codebase.

## Refactoring Best Practices

- Write tests first: Writing tests before refactoring can help ensure that the code still works as expected after refactoring. Tests can also provide a safety net and help detect any regressions caused by refactoring.
- Take small steps: Refactoring in small, incremental steps can help reduce the risk of breaking the code and make it easier to track changes. It also allows developers to verify that the code works as expected after each step.
- Code review: Code reviews can help identify potential issues and provide feedback on refactoring changes. They can also help ensure the code remains maintainable and adheres to coding standards.
- Refactor frequently: Refactoring should be a regular part of the development process rather than a one-time event.
- Document changes: Documenting refactoring changes can help other developers understand the reasoning behind them and how they affect the codebase. It can also help track changes and provide a record of the refactoring process.

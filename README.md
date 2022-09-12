# Code Review Checklist

## Implementation

-   [ ] Does this code change cover all feature requirements?
-   [ ] Is this code change safe? What is being done to ensure that?
-   [ ] What the potential risks that this change introduces?
-   [ ] Is the PR sized correctly? Can it have been broken up into smaller pieces?

## Design and Performance

-   [ ] Is the code at the right abstraction level? For example, is business logic in the right place?
-   [ ] Are there any best practices, design patterns or language-specific patterns that could substantially improve this code?
-   [ ] Does this code follow Object-Oriented Analysis and Design Principles, like the Single Responsibility Principle, Open-Close Principle, Liskov Substitution Principle, Interface Segregation, Dependency Injection?
-   [ ] Are objects being needlessly mutated?
-   [ ] Are operations done in this change performant?

## Database

-   [ ] Are queries effecient? Do they avoid n+1 problems?

## Logic Errors and Bugs

-   [ ] Are all edge cases covered? Different data types, null cases.
-   [ ] Are there any inputs or external events that could break the code?
-   [ ] Is data retrieved from external APIs or libraries checked accordingly? What happens if there are errors? Timeouts? SSL issues?

## Error Handling and Logging

-   [ ] Is error handling done the correct way?
-   [ ] Should any logging or debugging information be added or removed?
-   [ ] Are error messages user-friendly?
-   [ ] Do error cases warrant an alert or a page?

## Dependencies

-   [ ] Will this code change impact different teams?
-   [ ] Has a Subject Matter Expert looked over the code before it can be committed? If so, did they leave their approval?
-   [ ] Is there any public/private documentation or README's that need to be updated?
-   [ ] Are there any external smoke tests that should run to validate this change on its dependencies?

## Security and Data Privacy

-   [ ] Is authorization/authentication handled correctly?
-   [ ] Is user input validated, sanitized, and escaped to prevent security attacks such as cross-site scripting, SQL injection?
-   [ ] Is sensitive data like user data, credit card information securely handled and stored?
-   [ ] Is there data that needs to be encrypted? Or hidden from logs?
-   [ ] Does this code change reveal some secret information like keys, passwords, or usernames?

## Testing and Testability

-   [ ] Are there unit tests?
-   [ ] Are there integration tests?
-   [ ] Are there API/contract specs?
-   [ ] Is there code coverage for all the new changes?

## Readability

-   [ ] Is the code easy to understand?
-   [ ] Did the code follow coding style guidelines?
-   [ ] Are variable/function/class names accurately described?
-   [ ] Can the readability of the code be improved by smaller methods?
-   [ ] Is the code located in the right file/folder/package?
-   [ ] Is the data flow understandable?
-   [ ] Are there comments? Are they well justified? Can some comments be removed by making the code itself more readable?

## CI/CD

-   [ ] Did it pass all CI builds?

## Housekeeping

-   [ ] Are commit messages meaningful? Do they need to be squashed?

**Big thanks to https://github.com/mgreiler/code-review-checklist where this list was heavily inspired from.**

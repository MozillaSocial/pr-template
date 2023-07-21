# Mozilla Social Pull Request Review Guidelines

PR reviews are we get to share and discuss code before we deliver features to our users. The review step should be meaningful, informative, interesting, and a key element of the continuous improvement of both our codebase and our relations with each other as a team.

## Goals of PR review

PR review should enhance the following goals and values:

- Code Quality: Code reviews help identify and address logic errors, bugs, code style departures, and security vulnerabilities. It helps to both ensure that code being merged meets our quality standards, and helps us to evolve those standards.
- Knowledge Sharing: Reviews are the main forum for discussions of real code, and should facilitate elevated conversations across the team. PR reviews provide an opportunity for develops to learn from one another, share best practices, and gain insights into the different parts of the codebase. 
- Consistency: Reviews help ensure that the whole team follows the same conventions and coding standards, leading to a more readable and maintainable codebase.
- Collaboration and Feedback: Code reviews provide a platform for constructive feedback, discussions, and ideas that can lead to better solutions and continuous improvement.
- Codebase Health: Code reviews can help us prevent technical debt and help identify both risky low-quality code, and areas for improvement in our developmebt process and tooling.
- Onboarding and Knowledge Transfer: Reviews help us onboard new team members by exposing them to our codebass and practices.

## PR Expectations 

### PR Description 

- PR naming conventions
- Title
- Link to ticket
- What's Here: Describe what you did and why, before and after
- Steps to test
- Questions/What I'd Like Feedback On
- Other References

### Code Expectations

- PRs should be small both so that reviews are digestible and to reduce deployment risks
- Code should conform to linting/style expectations
- All functions/methods should have comment blocks in the standard documentation format for the language (generally docblock) 
- Unit test coverage is expected

### Review Etiquette and Expectations

- Spend the time to read, understand, and preferably test what's in the PR -- time spent here benefits all of us and our users.
- Ask questions - don't assume that you know why the author made the choices they did.
- Try to understand the big picture -- where this code is going, how it's meant to serve users and how it will fit into our codebase.
- Use the PR forum for contructive discussion
- Always consider perfomance, security, and adherence to existing mental models and patterns. 
- An approval means you're confident that this PR will both do what it's supposed to do, improve the Mozilla Social codebase, and not introduce technical debt. 
- Expect to complete your review within 1 business day of the PR going to review. If you can't do that, please tell the author early on. 

### Reviewer Expectations
- Most reviews will require one 👍🏼 
- Initial reviewer is populated from an appropriate per-domain set of reviewers

Some reviews will require 2 👍🏼, based on the characteristics of the review. Some of these include:

- Does this PR introduce new infrastructure or significant new components?
- Does this PR cross domains, teams or component areas?
- Does the author want extra 👀 for any other reason, like complexity, questions, mentoring, etc.

When a second reviewer is added, it's expected that this reviewer will be a member of a senior engineering group. The sr-eng review may add other reviewers as per their discretion.

### Automated Checks 

PRs are expected to pass the following

- Linter
- Docblock check
- Unit test coverage
- CI 

### Next Steps
- Write the PR Description Template
- Stub out the reviewer groups
- Implement the automated checks and thumb policies


# Mozilla Social Pull Request Review Guidelines

PR reviews are we get to share and discuss code before we deliver features to our users. The review step should be meaningful, informative, interesting, and a key element of the continuous improvement of both our codebase and our relationships with each other as a team.

> Note that all interactions within these repositories must adhere to the
> [Mozilla Community Participation Guidelines](https://www.mozilla.org/en-US/about/governance/policies/participation/),
> which broaden and supercede all guidelines and expectations here.


## Goals of PR review

We review code in order to:

- __Maintain code quality and correctness:__ Code reviews help identify and address logic errors, bugs, departures from code standards, and security vulnerabilities. It ensures that code being merged meets our quality standards and helps us to evolve those standards.
- __Share knowledge:__ Reviews are the main forum for discussions of real code and should facilitate elevated conversations across the team. PR reviews provide an opportunity for engineers to learn from one another, share best practices, and gain insights into the different parts of the codebase.
- __Consistency:__ Reviews help ensure that the whole team follows the same conventions and coding standards, leading to a more readable and maintainable codebase.
- __Collaboration and feedback:__ Code reviews provide a platform for constructive feedback, discussions, and ideas that can lead to better solutions and continuous improvement.
- __Codebase health:__ Code reviews can help us prevent technical debt, identify risky code patterns, and discover areas for improvement in our development process and tooling.
- __Onboarding and knowledge transfer:__ Reviews help us onboard new team members by exposing them to our codebases and practices.

## PR Expectations

### Code Expectations

- PRs should be small. Meaningful reviews require digestible changes. Small changes also reduce deployment risks.
- Code should conform to linting/style expectations.
- All functions/methods should have comment blocks in the standard documentation format for the language (generally docblock).
- Ideally, all code should be checked in alongside tests that validate its
  correctness. These should include unit tests, at a minimum. 
    - Test guidelines, including when to introduce larger component or
      cross-component tests will be forthcoming.
- Use semantic commit messages. Commit messages should be short, imperative descriptions of
  _what_ is done in the commit:

  > Unhelpful: "fix bug"

  > Helpful: "prevent OOB error when key is +infinity"

### PR Format

PRs should include:

- __A meaningful and descriptive title, chosen according to naming conventions.__ (TBD)
- __Links to any relevant tickets or issues.__
- __A description of "What's Here."__ Describe what you did and _why_. This
  description should include the previous behavior of the code and how the new
  behavior differs.
- __Steps to test.__ Reviewers should be able to run the code themselves in
  order to explore and validate its behavior.
- __Questions/What you'd like feedback on.__ Call out any specific areas of the
  code or concepts that you would like people to focus on.
- __References.__ Include links to design docs/PRDs, runs of tests/benchmarks,
  etc.

### Review Etiquette and Expectations

- __First and foremost: use the PR forum for _constructive_ discussion.__ Discuss
  and critique __the code, not the author.__
- Try to understand the big picture. Where this code is going? How is it meant to serve users? How will it fit into our codebase?
- Spend the time to read, understand, and preferably test what's in the PR--time
  spent here benefits all of us and our users. Don't rubber-stamp code, even if
  it is a small change. Detailed and thorough code review improves our codebase
  over time.
- Consider performance, security, and adherence to existing mental models and patterns.
- Assume the best intentions of the author. Likewise, as an author, assume the
  best intentions of reviewers.
- Ask questions. Don't assume that you know why the author made the choices they
  did. If you see an alternative approach, or might prefer code to be written
  differently, __ask__ the author why they structured something the way that
  they did--there might be a reason that you don't see. Remember that there's
  always _multiple ways to write correct code_--try to balance _your
  preferences_ against _style requirements_.
- If you require a change to be made or see an issue that should be addressed,
  __explain__ the _whys_ and your suggested _hows_.

  > __Unhelpful:__ "This is a bug; use `int` or at least make this `unsigned`." 

  > __Helpful:__ "Can this overflow? I believe that a player might have more
  > than 127 lives. Lets use `int` or at least `unsigned` here. What do you
  > think?"

- An approval means you're confident that this PR will both do what it's supposed to do, improve the Mozilla Social codebase, and not introduce technical debt.
- Ideally, a review should be completed within one business day of the request. 
   If, as the reviewer, you can't do that, proactively communicate with the author to figure out if your timeframe works.
   If, as the author, your PR is urgent, proactively communicate with your reviewer(s) to see if review can be expedited.
   A meaningful review takes time. As an author, you can help your reviewers provide good feedback faster by committing small, well-documented changesets.
   Collaboration while coding can also help to both expedite, and deepen, the code review stage.


### Process Expectations

- All reviews require at least one 👍. 
- Select an appropriate reviewer for your code. If there is no one specific
  person that you would like feedback from, allow the reviewer to be
  auto-populated from the team.
- One 👍 is sufficient for most code, but make sure to include everyone that you
  want meaningful feedback from or you think needs to be aware of the change.

Some reviews will require 2 👍, based on the characteristics of the PR. Some of these include:

- Does this PR introduce new infrastructure, dependencies, or new components?
- Does this PR cross domains, teams, or component areas?
- Does the author want extra 👀 for any other reason, like complexity, questions, mentoring, etc.?

When a second reviewer is added, it's expected that this reviewer will be a member of a senior engineering group. The sr-eng review may add other reviewers as per their discretion.

### Request and response expectations

- Where will we make PR requests?
- What is the expected response times?
- How do we escalate requests?


### Automated Checks

PRs are expected to pass the following across the organization

- Linter
- Docblock check
- Unit test coverage
- CI
- PR Line size check
- Commit Linting

### Next Steps

- Circulate for review and comments
- Stub out the reviewer groups
- Implement the automated checks and thumb policies

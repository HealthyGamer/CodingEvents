# Why Testing Is Important

## Why people don't want to write tests

- Boring and tedious to write
- Time-consuming and expensive
  - (estimates anywhere from 15%-50% of total dev costs)
- Not a user-facing feature
- Difficult to define what "enough" tests looks like
- If there's a QA team, it can make devs defensive
- Bugs will still happen

## Why do it

- Bugs have consequences, and sometimes, they even cause people to get hurt
- Issues erode user trust in the software
  - If you don't currently have competitors, that can change quickly
- Bug fixes take longer than testing and mess up timelines since it is unplanned work. It's ultimately more expensive.
- Tests help enforce code quality standards.

## Convincing people

- Create a plan
  - What types of tests to focus on: unit, system, integration, end-to-end, acceptance, and performance
    - Adding tests to an existing system usually rules out unit tests initially
- Create a strategy for implementation.
  - New dev first
  - Riskiest code first
  - Tests as part of bug fixes
- Decide on metrics for success
  - Code coverage is a problematic metric.
  - The number of bugs is more valuable, but it takes time to measure
  - There are plenty of others, but they can be harder to measure: <https://www.practitest.com/resource-center/blog/test-coverage-metrics/>
- Find evidence for why testing is valuable
  - <https://web.archive.org/web/20091026154339/http://biblio.gdinwiddie.com/biblio/StudiesOfTestDrivenDevelopment> These are for TDD specifically, but the principles apply elsewhere.
  - <https://www.it-cisq.org/the-cost-of-poor-software-quality-in-the-us-a-2020-report/> "This report seeks to quantify the impact of poor software quality on the United States economy referencing publicly available source material. For 2020, we estimate that figure to be approximately $2.08 trillion."
  - <https://www.nist.gov/system/files/documents/director/planning/report02-3.pdf> 4.9 hours to fix a bug in dev, 15.3 hours after release.
- Better code quality, better work/life balance
  - Fewer nights and weekend emergencies
  - Improvements in code quality make it easier to do the job
  
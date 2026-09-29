# Cornell Data Strategy

**Cornell Data Strategy (DSA)** is a student-led organization at Cornell University that works with companies and organizations to solve real-world problems through **data science, machine learning, software engineering, and analytics**.

Our GitHub organization contains the technical work behind DSA client engagements, internal tools, research initiatives, and engineering infrastructure.

## What We Build

DSA teams work across the full data and software lifecycle, from understanding a client's problem to designing, implementing, and deploying a production-ready solution.

Projects may include:

- Machine learning and predictive modeling
- Data pipelines and ETL systems
- Full-stack web applications
- Data visualization and interactive dashboards
- Forecasting and optimization
- Natural language processing
- Statistical analysis and experimentation
- Cloud infrastructure and deployment
- Internal developer and analytics tooling

Our goal is not simply to produce an analysis, but to build solutions that are technically rigorous, maintainable, and useful to our partners.

## Organization Structure

Repositories generally fall into several categories:

### Client Projects

Private repositories containing work completed for DSA partners. These may include source code, modeling pipelines, dashboards, documentation, and deployment infrastructure.

Client repositories may contain confidential or proprietary information and should only be accessed by authorized team members.

### Internal Tools

Software and infrastructure used to improve how DSA teams develop, collaborate, analyze data, and deliver projects.

### Training & Resources

Technical resources, examples, templates, and onboarding material used by DSA analysts and engineers.

### Open-Source Projects

Public tools, research, or educational projects developed by DSA members and made available to the broader community.

## Repository Standards

Individual repositories may have project-specific requirements, but DSA projects should generally include:

```text
project/
├── README.md
├── src/
├── tests/
├── data/
├── notebooks/
├── docs/
├── requirements.txt / pyproject.toml
└── .gitignore
```

Not every project will follow this exact structure. Teams should choose an architecture appropriate for the technology and scope of the engagement.


## Development Workflow

Unless otherwise specified by a repository, contributors should avoid developing directly on `main`.

A typical workflow is:

```bash
git checkout main
git pull

git checkout -b feature/your-feature
```

Make your changes, commit them with a descriptive message, and push your branch:

```bash
git add .
git commit -m "Add demand forecasting pipeline"
git push origin feature/your-feature
```

Then open a pull request for review.

### Branch Naming

Use descriptive branch names such as:

```text
feature/dashboard-filters
feature/model-training
fix/api-authentication
refactor/data-pipeline
docs/setup-guide
```

### Commits

Prefer concise commits that explain the change being made.

Good:

```text
Add API endpoint for forecast results
Fix missing values in preprocessing pipeline
Refactor authentication middleware
```

Avoid:

```text
changes
update
stuff
final
final-final
```

## Pull Requests

Pull requests should clearly explain:

1. **What changed**
2. **Why the change was necessary**
3. **How the implementation works**
4. **How the change was tested**

Large changes should be broken into smaller, reviewable pull requests when possible.

At least one other team member should review significant changes before they are merged.

## Code Quality

DSA projects should prioritize:

- Readability
- Modularity
- Reproducibility
- Documentation
- Testing
- Maintainability

Prefer clear code over unnecessarily complex implementations.

When possible, projects should use automated formatting, linting, and testing tools appropriate for their technology stack.

Examples include:

```text
Python:      Ruff, Black, Pytest
JavaScript:  ESLint, Prettier, Jest
TypeScript:  ESLint, Prettier, Vitest
```

## Data & Security

Client data must be handled carefully.

**Never commit:**

- API keys
- Passwords
- Access tokens
- Private keys
- Database credentials
- Personally identifiable information
- Confidential client datasets

Secrets should be stored using environment variables or an approved secrets-management system.

For example:

```bash
DATABASE_URL=...
API_KEY=...
```

Files containing secrets should be excluded through `.gitignore`.

```text
.env
.env.local
credentials.json
```

If a secret is accidentally committed, assume it has been compromised and notify the project lead immediately.

## Data Files

Large datasets should generally **not** be committed directly to Git.

Depending on the project, data may instead be stored in:

- Cloud object storage
- Databases
- Client-managed systems
- Shared approved storage
- External datasets with documented retrieval instructions

Repositories should contain instructions explaining how authorized developers can obtain required data.

## Documentation

Documentation is part of the deliverable.

Code should be understandable to someone who did not originally write it.

Document:

- Important system behavior
- Non-obvious implementation decisions
- Model assumptions
- Data schemas
- API interfaces
- Environment configuration
- Deployment processes

For ML projects, teams should also document model inputs, outputs, evaluation methodology, and important limitations.

## Reproducibility

Analyses and models should be reproducible whenever possible.

Projects should specify:

- Dependency versions
- Environment setup
- Random seeds where appropriate
- Data preprocessing procedures
- Training procedures
- Evaluation metrics

A new contributor should be able to clone a repository, follow its README, and reproduce the project's primary results.

## Collaboration

DSA projects are multidisciplinary. Engineers, analysts, project managers, and client stakeholders may all interact with the same work.

Keep communication clear and document important technical decisions.

When making architectural changes that affect the broader team, discuss them with the project lead before implementation.

## Confidentiality

Many DSA projects are completed for external partners.

Materials contained within private repositories may be subject to confidentiality agreements or client restrictions.

Do not:

- Share private repositories externally
- Publish client data
- Copy proprietary code into public repositories
- Discuss confidential project information outside authorized channels

When in doubt, ask your project lead before sharing project materials.

## Getting Started

If you're joining an existing DSA project:

1. Clone the repository.
2. Read the project README completely.
3. Configure your local environment.
4. Run the existing application or pipeline.
5. Run the project's tests.
6. Review open issues and pull requests.
7. Ask your project lead which task to begin with.

Understanding the existing system before modifying it will save time and reduce unnecessary regressions.

## About Cornell Data Strategy

Cornell Data Strategy brings together students interested in **technology, data, business, and strategy** to build solutions for real organizations.

Our teams combine technical implementation with an understanding of the underlying business problem, allowing us to take projects from raw data and ambiguous requirements to actionable, deployable systems.

---

**Cornell Data Strategy**  
Cornell University

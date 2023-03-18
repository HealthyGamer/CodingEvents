# Documentation

Everyone wants good docs available, but no one wants to take the time to write them. "The code is the documenation" might sometimes work for a small project with only a few devs or users. However, as code scales, the documentation requirements expand along with it.

## Audience

Depending on the project, there may be several different audiences to consider. Each audience may need its own docs to support them.

- User documentation: This layer is typically aimed at end-users and provides information on how to use the software. It may include user guides, tutorials, and online help.
- Developer documentation: This layer is aimed at developers and provides information on how to work with the codebase. It may include API references, code samples, and architectural diagrams.
- System documentation: This layer provides an overview of the system architecture and its components, including servers, databases, and network infrastructure.
- Deployment documentation: This layer provides information on deploying the software in various environments, including development, testing, and production.
- Maintenance documentation: This layer provides information on maintaining the software over time, including troubleshooting, bug fixing, and updating.

The rest of this content will focus on developer docs, but similar principles also apply to other types.

## Inside the Codebase

- Code comments: Inline comments in the code that explain what the code is doing and why it's doing it.
- Function and method documentation: This includes documentation for individual functions or methods that explains their purpose, inputs, outputs, and any assumptions or constraints they have.
- API documentation: If your code exposes an API, documentation for the API should be included in the codebase. This can include information on how to authenticate, access different endpoints, and the expected responses.
- Readme files: A readme file should be included in the codebase that provides an overview of the project, how to set it up, and how to get started.
- Contribution guidelines: If the codebase is open source and accepting contributions, there should be documentation on how to contribute to the project.
- Issue tracking and bug reports: Teams often use issue tracking systems to manage tasks, bugs, and feature requests. This internal documentation includes detailed issue descriptions, steps to reproduce, and any related discussions.
- Release notes: These documents detail the changes and updates in each new project version. They may include information about new features, bug fixes, performance improvements, and known issues.

## External Docs

- Getting started guide: A guide that provides an overview of the project, how to set up the development environment, and how to run the code.
- Architecture and design documents: High-level documentation that describes the overall architecture of the project, including components, dependencies, and interactions between them.
- Data model documentation: If the project involves working with a database, documentation on the data model, including the schema, relationships between tables, and any constraints, should be provided.
- API reference documentation: If the project exposes an API, documentation on the API endpoints, inputs, outputs, and authentication mechanisms should be provided.
- Samples and tutorials: In addition to the getting started guide, there are other common scenarios that your users may run into. Sample code for those scenarios can help with adoption.
- Troubleshooting guide: A guide that provides solutions to common problems developers may encounter while working on the project.

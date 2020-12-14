# Micro-service Management

With lots of services comes lots of repositories in various lifecycle stages and teams. It is important to be able to quickly report on those repositories, and make changes across them in an efficient manor.

## Tasks

Find a suitable solution to the following scenarios, this can be github tooling, 3rd party tooling or custom created tools (in whatever language/scripting you want) that can be useful in the following scenarios. Assume that there are approximately 100 Github repositories that are being managed when considering solutions.

1. _A developer (`user-jo1`) recently left the company, we need to find all the repositories that they were responsible for maintaining._

    List repositories in which a specified user appears in either the `.github/CODEOWNERS`, or `VULNERABILITY_TEMPLATE.md`.

1. _A security audit requires a complete list of base images used for containers._

    List the repository, directory, and images specified in the `FROM` line(s) of `Dockerfile`s.

1. _A vulnerability has been discovered in a common npm package (`lodash.get`), determine if our projects use it._

   List the repository, directory and version of the package found in either dependency or devDependency of `package.json`.

1. _Not all project have been updated to have a `.github/CODEOWNERS` file_

    List repositories without a `.github/CODEOWNERS` file.

1. _A Github action workflow was added that is incorrect for some repository configurations, find the misconfigurations._

    List repositories with a mismatch between the path specified in `.github/workflows/docker-scan.yml` at `on.pull_request.paths[0]` and the location of the Dockerfile(s) in the repo. `src/Dockerfile` vs `Dockerfile`.

1. _Update the minor version of Node.js because of a recently discovered vulnerability (`12.0` → `12.1`)._

    Automated creation of Pull Requests that update `package.json` and `Dockerfile` `FROM` lines if they match a specified version to a new specified version.

## Example Repositories

For this test 2 example repositories have been created. They can be modified and committed against, ideally on new branches.

1. https://github.com/bluedrop-learning-networks/ztest-simple-api

    A simple api with lots of npm dependencies.

2. https://github.com/bluedrop-learning-networks/ztest-set-of-services

   A repository holding both the api and client of a particular project, each having their own `Dockerfile` and `package.json`.

## Answering

Answers can be documented in the repository https://github.com/bluedrop-learning-networks/ztest-candidate, in whatever form (text, html, or markdown, code, github issues).

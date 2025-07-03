# Finoid Maven Parent

A Maven parent POM that centralizes plugin configurations and build conventions used
across Finoid projects. It provides a consistent setup for building, testing, and deploying Maven artifacts as
part of the Finoid developer experience.

<div align="center">
  <img src=".github/assets/finoid-maven-parent.jpg" width="256">
</div>

## Features
- **Dependency convergence and enforcer**: Clean up and fail fast on dependency issues
- **Static analysis**: ErrorProne, NullAway, Checkstyle, and (optionally) Checker Framework
- **Jacoco** for code coverage
- **Ready for Maven Central publishing**: GPG signing, source and Javadoc JARs, central publishing setup
- **Configurable via properties** for individual project needs


## Included Plugins

| Plugin                          | Purpose                                 |
|---------------------------------|-----------------------------------------|
| codequality-maven-plugin        | Code quality checks and static analysis |
| jacoco-maven-plugin             | Code coverage reporting                 |
| maven-compiler-plugin           | Java compilation with parameter names   |
| maven-enforcer-plugin           | Build rule enforcement                  |
| maven-source-plugin             | Source JAR generation                   |
| maven-javadoc-plugin            | JavaDoc generation                      |
| maven-gpg-plugin                | Artifact signing                        |
| central-publishing-maven-plugin | Maven Central deployment                |

## Bash configuration

To simplify running the Code Quality Maven Plugin, you can add the following alias to your shell configuration (e.g. ~
/.bashrc or ~/.zshrc):

```bash
alias cq='./mvnw clean generate-sources io.github.finoid:codequality-maven-plugin:code-quality@maven-code-quality'
```
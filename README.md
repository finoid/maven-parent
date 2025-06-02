# Finoid Maven Parent

A Maven parent POM that centralizes plugin configurations and build conventions used
across Finoid projects. It provides a consistent setup for building, testing, and deploying Maven artifacts as
part of the Finoid developer experience.

<div align="center">
  <img src=".github/assets/finoid-maven-parent.jpg" width="256">
</div>

The following plugins are used:

## Bash configuration
To simplify running the Code Quality Maven Plugin, you can add the following alias to your shell configuration (e.g. ~/.bashrc or ~/.zshrc):

```bash
alias cq='./mvnw clean generate-sources io.github.finoid:codequality-maven-plugin:code-quality@maven-code-quality'
```
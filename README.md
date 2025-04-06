# 🧪 Pre-commit Hooks for Spring Boot Projects

This repository provides reusable `pre-commit` hooks written in `.sh` (Bash) format, specifically for **Spring Boot** projects using **Gradle** or **Maven**. These hooks help enforce code quality by running tests before every commit.

---

## ✨ Features

- ✅ Automatically runs tests before commits
- 🔍 Detects whether the project uses **Gradle** or **Maven**
- ⚙️ Works on **Windows (via Git Bash)**, **Linux**, and **macOS**
- 🧪 Easy integration with the [`pre-commit`](https://pre-commit.com) framework

---

## 📦 Installation Guide

### [Install Pre-commit (Once Per Machine)](https://pre-commit.com/)

Required on all operating systems

```bash
brew install pre-commit
```

### Paste .pre-commit-config.yaml into your root project path
```yml
repos:
  - repo: local
    hooks:
      - id: spring-boot-test
        name: Run Tests
        entry: .githooks/precommit/run-tests.sh
        language: script
        always_run: true
```

### Paste .githooks/precommit/run-tests.sh file into root proejct path

Recommended Project Structure

```
your-spring-boot-project/
├── .pre-commit-config.yaml
├── .githooks/
│   └── precommit/
│       └── run-tests.sh
├── build.gradle / pom.xml
```


###  Install Git Hooks (Once Per Project)

Run this inside your Spring Boot project root:

```bash
pre-commit install
```

### 🧪 Run Hooks Manually

```bash
pre-commit run --all-files
```


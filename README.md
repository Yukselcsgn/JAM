# JAM (Java Moderator) - Java Code Hygiene Toolkit

JAM is a comprehensive Java code hygiene toolkit designed to improve code quality, enforce best practices, and maintain security across Java projects. JAM combines static analysis, formatting, import management, security scanning, Javadoc validation, and pre-commit hooks into a modular and extensible framework.

---

## 🚀 Features

* **Linting:** Enforce coding conventions, detect anti-patterns, and find potential bugs.
* **Formatting:** Automatic code formatting using configurable styles (Google, Eclipse, or custom).
* **Import Management:** Detect and remove unused imports, optimize import order, and fix wildcard imports.
* **Security Scanning:** Identify hardcoded secrets, vulnerable dependencies, and known security issues.
* **Javadoc Validation:** Ensure public APIs are documented correctly and all Javadoc tags are valid.
* **Pre-commit Hooks:** Automate checks and formatting before commits to maintain code hygiene.
* **Live Agent:** Monitor project files, integrate with IDEs, and automatically trigger JAM plugins on changes.
* **Plugin System:** Easily extend JAM with custom plugins for frameworks, libraries, or project-specific rules.

---

## 📦 Project Structure

```
packages/
├── jam-core/        # Core framework with plugin system, configuration, reporting, and AST parsing
├── jam-cli/         # Command-line interface for executing JAM plugins
├── jam-lint/        # Linting module with rules and engine
├── jam-format/      # Code formatting module with Java and style-specific formatters
├── jam-imports/     # Import management module to optimize and fix imports
├── jam-security/    # Security scanning module for secrets and dependency vulnerabilities
├── jam-javadoc/     # Javadoc validation module for public API documentation
├── jam-hooks/       # Pre-commit and pre-push hook management module
├── jam-agent/       # Live monitoring agent for IDE and filesystem integration
└── jam-plugins-examples/  # Example plugins demonstrating custom rules for Spring and Android
```

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/jam.git
cd jam
```

2. Build the project using Gradle:

```bash
./gradlew build
```

3. Run CLI commands:

```bash
java -jar jam-cli/build/libs/jam-cli.jar <command>
```

---

## 💻 Usage

### CLI Commands

* **Linting:** `jam lint [options]`
* **Formatting:** `jam format [options]`
* **Imports:** `jam imports [options]`
* **Security:** `jam security [options]`
* **Javadoc:** `jam javadoc [options]`
* **Hooks:** `jam hooks install|remove`
* **Fix All:** `jam fix-all`

### Agent

* Start the agent for live monitoring:

```bash
java -jar jam-agent/build/libs/jam-agent.jar --project <path>
```

* Integrate with IDEs like IntelliJ using `IntelliJAdapter`.

### Pre-commit Hooks

* Install hooks for automated checks before commit:

```bash
jam hooks install
```

* Remove hooks:

```bash
jam hooks remove
```

---

## 🛠 Extending JAM

* Create custom plugins by implementing the `JamPlugin` interface.
* Example plugins can be found in `jam-plugins-examples/`.
* Plugins can define rules for linting, formatting, or project-specific checks.
* Load plugins via configuration in `JamConfig`.

---

## 📄 Reporting

* JAM generates reports in JSON or human-readable formats.
* Reports include details of lint violations, formatting issues, security findings, Javadoc problems, and import optimizations.

---

## 🤝 Contributing

* Fork the repository and create your branch.
* Write tests for your features and changes.
* Submit a pull request with detailed description and references.

---

## 📜 License

* MIT License. See `LICENSE` file for details.

---

## 📞 Contact

* Maintainer: **Yüksel COŞGUN**
* GitHub: [https://github.com/yourusername/jam](https://github.com/yourusername/jam)

---

JAM helps teams maintain high code quality, security, and consistency in Java projects through automation and best practices.

# Create CLI Template

A starter kit generator for CLI applications. This tool helps you quickly scaffold a new command-line interface application with configurations.

[![Tests](https://github.com/richardgaunt/cli-maker/actions/workflows/test.yml/badge.svg)](https://github.com/richardgaunt/cli-maker/actions/workflows/test.yml)


## Features

- Generates a complete CLI application structure
- Sets up testing with Jest
- Configures ESLint for code quality
- Initializes Git repository
- Sets up Command parsing with Commander.js
- User input handling with Inquirer

## Installation

```bash
# Install globally
npm install -g create-cli-template

# Or use directly with npx
npx create-cli-template my-cli-app

# For development
git clone <repository-url>
cd create-cli-template
npm install
npm link
```

## Usage

```bash
# Create a new CLI application with interactive prompts
create-cli-template my-cli-app

# Skip prompts and use defaults
create-cli-template my-cli-app --yes

# Skip git initialization
create-cli-template my-cli-app --no-git

# Skip dependency installation
create-cli-template my-cli-app --no-install
```

## CLI Options

- `[name]` - Project directory/package name (optional)
- `-y, --yes` - Skip all prompts and use defaults
- `--no-git` - Skip git initialization
- `--no-install` - Skip dependency installation

## Configuration steps

When creating a new CLI application, you'll be asked for:

1. **Package/directory name**: The npm package name and directory name (lowercase with hyphens)
2. **Human-readable title**: A prettier title for display in README and CLI output
3. **Project description**: A brief description of what your CLI does
4. **Author**: Your name (defaults to Git config)
5. **License**: The license to use (MIT, ISC, Apache-2.0, GPL-3.0)

## Generated Project Structure

```
my-cli-app/
├── bin/
│   └── index.mjs        # CLI entry point
├── src/
│   ├── index.mjs        # Main module exports
│   └── index.test.js    # Tests for main module
├── tests/
│   └── index.test.mjs   # Additional tests
├── .gitignore
├── eslint.config.mjs
├── jest.config.mjs
├── package.json
└── README.md
```

## Development

```bash
# Clone this repository
git clone <repository-url>
cd create-cli-template

# Install dependencies
npm install

# Link the package locally for testing
npm link

# Run the CLI
create-cli-template test-app

# Run tests
npm test

# Run specific test suites
npm run test:timing
npm run test:errors
npm run test:features
npm run test:all

# Run linting
npm run lint
```

## License

MIT © Richard Gaunt

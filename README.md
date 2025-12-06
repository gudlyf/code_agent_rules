# Cursor Rules Repository

This repository contains a collection of coding standards and conventions formatted as rule files for use with AI coding assistants.

## Included Rules

- **000-cursorRulesLocation.mdc** - Standards for placing and organizing Cursor rule files
- **010-documentationStandards.mdc** - Documentation maintenance standards
- **020-shellScriptStandards.mdc** - Shell script formatting, indentation, and color-coded messaging conventions
- **030-pythonStandards.mdc** - Python coding standards including indentation, type hints, docstrings, and code organization
- **040-conventionalCommits.mdc** - Git conventional commits format for automated commits
- **050-terraformFormatting.mdc** - Terraform/OpenTofu HCL formatting standards and conventions
- **060-gitCommitFormatting.mdc** - Git commit message formatting standards using conventional commits with full file path scopes

## Installation

### For Cursor

Cursor reads rule files from the `.cursor/rules/` directory. You can install these rules either globally (for all projects) or per-project.

#### Global Installation (Recommended)

Place the rule files in your home directory's `.cursor/rules/` folder:

```bash
# Create the directory if it doesn't exist
mkdir -p ~/.cursor/rules

# Copy all rule files
cp *.mdc ~/.cursor/rules/
```

**Location:** `$HOME/.cursor/rules/`

#### Project-Specific Installation

Place the rule files in your project's `.cursor/rules/` directory:

```bash
# From your project root
mkdir -p .cursor/rules

# Copy all rule files
cp /path/to/this/repo/*.mdc .cursor/rules/
```

**Location:** `PROJECT_ROOT/.cursor/rules/`

**Note:** Project-specific rules take precedence over global rules.

### For Cline

Cline uses the same rule file format and directory structure as Cursor. Follow the same installation instructions as above.

**Location:** `$HOME/.cursor/rules/` (global) or `PROJECT_ROOT/.cursor/rules/` (project-specific)

### For Claude Code

Claude Code (in Cursor) uses the same rule system. The installation is identical to Cursor.

**Location:** `$HOME/.cursor/rules/` (global) or `PROJECT_ROOT/.cursor/rules/` (project-specific)

## File Format

All rule files use the `.mdc` extension and follow the Markdown format with frontmatter metadata. Each file includes:

- A `description` field in the frontmatter
- `globs` patterns to specify which file types the rule applies to
- Rule content in Markdown format

## Usage

Once installed, these rules will automatically be applied by your AI coding assistant when working with relevant file types. The rules guide code generation, formatting, and documentation to match your specified standards.

## Customization

Feel free to modify these rules to match your team's specific coding standards. You can:

- Edit existing rules to adjust standards
- Add new rule files following the same format
- Remove rules that don't apply to your workflow

## Contributing

When adding or modifying rules:

1. Follow the naming convention: `NNN-descriptive-name.mdc` (numbered prefix in increments of 10 for ordering, e.g., 010, 020, 030)
2. Include proper frontmatter with `description` and `globs` fields
3. Use clear, actionable rule descriptions
4. Test rules in your environment before committing

## License

See individual rule files for license information.


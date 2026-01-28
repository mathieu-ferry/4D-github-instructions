# 4D GitHub Copilot Instructions

A collection of GitHub Copilot custom instructions designed to enhance 4D application development. These instruction files help GitHub Copilot understand 4D-specific syntax, conventions, and best practices, resulting in better code suggestions and assistance.

## 📋 What's Included

| File | Purpose |
|------|---------|
| `4d.instructions.md` | Core 4D development guidelines: syntax, variables, types, operators, commands, and best practices |
| `4d.forms.instructions.md` | 4D Forms architecture: form-class binding, event handling, and UI patterns |
| `4d.errors.instructions.md` | Error handling guidance and common issues with the 4D syntax checker |
| `4d.catalog.instructions.md` | Guide for editing `catalog.4DCatalog` XML files (database structure) |
| `4dtest.md.instructions.md` | Instructions for running 4D tests with tool4d |
| `formsSchema.json` | JSON schema for 4D form validation |

## 🚀 Installation

### Step 1: Create the Instructions Directory

In your 4D project root, create the `.github` folder with an `instructions` subfolder:

```
YourProject.4DProject/
├── Project/
│   ├── Sources/
│   ├── DerivedData/
│   └── ...
├── .github/
│   └── instructions/          ← Create this folder
│       ├── 4d.instructions.md
│       ├── 4d.forms.instructions.md
│       ├── 4d.errors.instructions.md
│       ├── 4d.catalog.instructions.md
│       ├── 4dtest.md.instructions.md
│       └── formsSchema.json
└── ...
```

### Step 2: Copy the Instruction Files

Copy all `.instructions.md` files and `formsSchema.json` from this repository into your project's `.github/instructions/` directory.

### Step 3: Verify the Setup

Open your 4D project in VS Code with GitHub Copilot enabled. The instructions will automatically apply to matching file patterns:

- `**/*.4dm` → 4D methods and classes
- `**/Forms/**/*.4DForm` → 4D form files
- `**/Forms/**/*.4dm` → Form-related methods

## 📁 Alternative: Global Instructions

If you want these instructions to apply to **all** your 4D projects, you can place them in your VS Code user settings:

**macOS:**
```
~/Library/Application Support/Code/User/globalStorage/github.copilot-chat/.github/instructions/
```

**Windows:**
```
%APPDATA%\Code\User\globalStorage\github.copilot-chat\.github\instructions\
```

## 🎯 How It Works

GitHub Copilot custom instructions use YAML frontmatter to specify which files they apply to:

```yaml
---
applyTo: '**/*.4dm'
---
```

When you're editing a file that matches the pattern, Copilot will automatically include the relevant instructions in its context, providing:

- ✅ Correct 4D syntax suggestions
- ✅ Proper variable declarations with `$` prefix
- ✅ Type-safe code with explicit declarations
- ✅ 4D-specific patterns and idioms
- ✅ Form architecture best practices
- ✅ Proper error handling

## 🔧 Customization

Feel free to modify these instruction files to match your team's conventions:

1. **Add project-specific patterns** - Include your own naming conventions or architectural patterns
2. **Reference your classes** - Add examples from your actual codebase
3. **Extend the guidelines** - Add rules for specific components or libraries you use

## 📚 Resources

- [4D Documentation](https://developer.4d.com/docs/)
- [4D Language Reference](https://developer.4d.com/docs/Concepts/quick-tour)
- [GitHub Copilot Custom Instructions](https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot)

## 📄 License

See [LICENSE](LICENSE) for details.
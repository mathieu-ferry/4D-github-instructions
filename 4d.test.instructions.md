---
applyTo: '**/*.4dm'
---

# 4D Test Instructions

## Running Tests

```bash
<tool4dbin> --project <projectfile> --dataless --skip-onstartup --startup-method <testmethod>
```

## tool4d Location

Check in order:
1. `tool4d.app/Contents/MacOS/tool4d` in project
2. `tool4d` in $PATH
3. `$TOOL4DBIN` environment variable
4. `$HOME/Library/Application Support/Code/User/globalStorage/4D.4d-analyzer/tool4d/` (use `find` to locate)
